<script setup>
import { useLayoutStore } from "~/stores/layout";
import { useWindowSize } from "vue-window-size";
import RSChildItem from "~/components/layouts/sidemenu/ItemChild.vue";
import { useUserStore } from "~/stores/user";

const layoutStore = useLayoutStore();
const mobileWidth = layoutStore.mobileWidth;
const { width } = useWindowSize();

const user = useUserStore();
const route = useRoute();
const props = defineProps({
  items: {
    type: Array,
    default: () => [],
    required: true,
  },
});

const username = user.username;
const roles = user.roles;

const menuItem = props.items ? props.items : [];

// validate userExist on meta.auth.user
function userExist(item) {
  if (item.meta?.auth?.user) {
    if (item.meta?.auth?.user.some((e) => e === username)) {
      return true;
    } else {
      return false;
    }
  }
  return true;
}

// validate roleExist on meta.auth.role
function roleExist(item) {
  if (item.meta?.auth?.role) {
    if (item.meta?.auth?.role.some((e) => roles?.includes(e))) {
      return true;
    } else {
      return false;
    }
  }
  return true;
}

// Toggle show and hide menu content
function openMenu(event) {
  const target = event.currentTarget;
  try {
    target.querySelector("a").classList.toggle("nav-open");
    target.querySelector("ul").classList.toggle("hide");
  } catch (e) {
    // console.log(e);
    return;
  }
}

// Active menu
function activeMenu(routePath) {
  return route.path == routePath
    ? ` shadow-lg
            shadow-primary/50
            dark:shadow-primary/10
            text-white
            bg-gradient-to-r
            from-primary
            to-primary/90
            active-menu`
    : `transition-all	duration-300 hover:ml-4`;
}

function toggleMenu() {
  document.querySelector(".v-layout").classList.toggle("menu-hide");
  document.getElementsByClassName("menu-overlay")[0].classList.toggle("hide");
}

function navigationPage(path, external) {
  if (width.value <= mobileWidth) toggleMenu();

  // Check if the path is external
  if (!external) external = path.includes("http") ? true : false;
  navigateTo(path, {
    external: external,
  });
}
</script>

<template>
  <div v-for="(item, index) in menuItem" :key="index">
    <div
      v-if="
        !item.meta || !item.meta?.auth || (userExist(item) && roleExist(item))
      "
      class="navigation-wrapper"
    >
      <div
        v-if="item.header"
        class="text-left font-normal text-xs mx-6 mt-5 mb-2"
      >
        <span class="uppercase text-primary dark:text-primary">
          {{ item.header ? item.header : "" }}
        </span>
        <p class="text-gray-500 dark:text-gray-500">
          {{ item.description ? item.description : "" }}
        </p>
      </div>
      <ul class="navigation-menu">
        <li
          class="navigation-item"
          v-for="(item2, index2) in item.child"
          :key="index2"
          @click.stop="
            item2.child !== undefined ||
            (item2.child && item2.child.length !== 0)
              ? openMenu($event)
              : ''
          "
        >
          <div
            v-if="
              !item2.meta ||
              !item2.meta?.auth ||
              (userExist(item2) && roleExist(item2))
            "
            class="navigation-item-wrapper"
          >
            <NuxtLink
              v-if="
                item2.child === undefined ||
                (item2.child && item2.child.length === 0)
              "
              class="flex items-center px-4 py-3 mx-3 rounded-lg cursor-pointer"
              @click="navigationPage(item2.path, item2.external)"
              :class="activeMenu(item2.path)"
            >
              <Icon v-if="item2.icon" :name="item2.icon" size="18"></Icon>
              <Icon v-else name="mdi:circle-slice-8" size="18"></Icon>
              <span class="mx-3 font-normal">{{ item2.title }}</span>
              <Icon
                v-if="item2.child && item2.child.length > 0"
                class="ml-auto side-menu-arrow"
                name="material-symbols:chevron-right-rounded"
                size="18"
              ></Icon>
            </NuxtLink>
            <a
              v-else
              class="flex items-center px-4 py-3 mx-3 rounded-lg cursor-pointer"
              :class="activeMenu(item2.path)"
            >
              <Icon v-if="item2.icon" :name="item2.icon" size="18"></Icon>
              <Icon v-else name="mdi:circle-slice-8" size="18"></Icon>
              <span class="mx-3 font-normal">{{ item2.title }}</span>
              <Icon
                v-if="item2.child && item2.child.length > 0"
                class="ml-auto side-menu-arrow"
                name="material-symbols:chevron-right-rounded"
                size="18"
              ></Icon>
            </a>
            <RSChildItem
              v-if="item2.child"
              :items="item2.child"
              @openMenu="openMenu"
              @activeMenu="activeMenu"
            ></RSChildItem>
          </div>
        </li>
      </ul>
    </div>
  </div>
</template>
