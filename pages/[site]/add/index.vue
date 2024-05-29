<script setup>
import { useTenant } from "#imports";

definePageMeta({
  title: "Add Site",
  layout: "empty",
});

const tenant = useTenant();

const form = ref({
  storeName: "",
  storeDomain: "",
  storeType: "",
  storeIndustryType: "",
  agreement: false,
});

const storeIndustryTypeList = ref([
  {
    label: "Select Industry Type",
    value: "",
  },
  {
    label: "Apparel & Accessories",
    value: 1,
  },
  {
    label: "Arts & Entertainment",
    value: 2,
  },
  {
    label: "Baby & Toddler",
    value: 3,
  },
  {
    label: "Business & Industrial",
    value: 4,
  },
  {
    label: "Cameras & Optics",
    value: 5,
  },
  {
    label: "Electronics",
    value: 6,
  },
  {
    label: "Food, Beverages & Tobacco",
    value: 7,
  },
  {
    label: "Furniture",
    value: 8,
  },
  {
    label: "Hardware",
    value: 9,
  },
  {
    label: "Health & Beauty",
    value: 10,
  },
]);

const onInputHandlerStore = (value) => {
  // Generate store domain with dash (-) instead of space and lowercase and escape special characters
  form.value.storeDomain = value.toLowerCase().replace(/[^a-zA-Z0-9-]/g, "-");
};

const submitForm = async () => {};
</script>

<template>
  <div>
    <!-- HEADER -->
    <div
      class="fixed top-0 left-0 w-full h-[65px] shadow-md bg-slate-900 z-50 text-slate-200"
    >
      <div class="max-w-[1280px] mx-auto">
        <div class="flex justify-between items-center">
          <nuxt-link
            to="http://localhost:3000/"
            :external="true"
            target="_blank"
          >
            <img
              src="@/assets/img/logo/logo-full-transparent-white.png"
              alt="logo"
              class="h-[65px]"
            />
          </nuxt-link>
          <div class="flex justify-center items-center gap-5">
            <Icon
              name="ph:facebook-logo"
              class="w-6 h-6 cursor-pointer hover:scale-110"
            />
            <Icon
              name="ph:linkedin-logo"
              class="w-6 h-6 cursor-pointer hover:scale-110"
            />
            <Icon
              name="ph:github-logo"
              class="w-6 h-6 cursor-pointer hover:scale-110"
            />
            <VDropdown placement="bottom-end" distance="13" name="profile">
              <button
                class="flex justify-center items-center border rounded-md py-2 px-4 bg-slate-700"
              >
                <div class="">
                  {{ tenant }}
                </div>
                <Icon name="ic:outline-keyboard-arrow-down" class="ml-3" />
              </button>
              <template #popper>
                <ul class="header-dropdown w-full md:w-52">
                  <li>
                    <a
                      href="http://company-a.localhost:3000/"
                      class="flex items-center cursor-pointer py-2 px-4 hover:bg-[rgb(var(--bg-1))]"
                    >
                      <Icon name="ph:app-store-logo-fill" class="mr-2" />
                      Company A
                    </a>
                  </li>
                  <li>
                    <a
                      href="http://company-b.localhost:3000/"
                      class="flex items-center cursor-pointer py-2 px-4 hover:bg-[rgb(var(--bg-1))]"
                    >
                      <Icon name="ph:bug-fill" class="mr-2" />
                      Company B
                    </a>
                  </li>
                </ul>
              </template>
            </VDropdown>
          </div>
        </div>
      </div>
    </div>
    <!-- BODY -->
    <div class="pt-[90px] pb-8 max-w-[1280px] mx-auto px-4">
      <rs-card class="p-5">
        <div class="flex mb-5">
          <nuxt-link to="/" class="mx-4">
            <Icon name="ph:arrow-circle-left" class="cursor-pointer mt-2" />
          </nuxt-link>

          <div>
            <h3>Add New Site (STORE)</h3>
            <p class="text-slate-400">Form to add new site.</p>
          </div>
        </div>
        <hr class="my-8" />

        <FormKit type="form" :actions="false" @submit="submitForm">
          <!-- 1nd Step (Store Info) -->
          <section>
            <FormKit
              v-model="form.storeName"
              type="text"
              label="Store Name"
              label-class="text-left"
              validation="required|length:0,200"
              @input="onInputHandlerStore"
            />
            <FormKit
              v-model="form.storeDomain"
              type="text"
              label="Store Domain"
              label-class="text-left"
              :validation="[
                ['matches', /^[A-Za-z0-9-]+$/],
                ['required'],
                ['length', 0, 200],
              ]"
              validation-visibility="dirty"
            >
              <template #suffix>
                <div class="px-4 py-2 bg-gray-100 text-slate-400">
                  .example.com
                </div>
              </template>
            </FormKit>

            <FormKit
              v-model="form.storeIndustryType"
              type="select"
              label="Industry Type"
              label-class="text-left"
              :options="storeIndustryTypeList"
              validation="required"
              validation-visibility="dirty"
            />

            <rs-button btn-type="submit" class="w-full" variant="secondary">
              Add Store Site
            </rs-button>
          </section>
        </FormKit>
      </rs-card>
    </div>
  </div>
</template>
