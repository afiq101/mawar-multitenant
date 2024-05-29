<script setup>
import { useTenant } from "#imports";

definePageMeta({
  title: "Site",
  layout: "empty",
});

const tenant = useTenant();

useSeoMeta({
  title: tenant,
  description: "",
  ogSiteName: tenant,
  ogTitle: tenant,
  ogDescription: `This is a description of ${tenant}`,
  ogImage: `https://${tenant}.example.com/images/logo.png`,
  ogImageAlt: tenant,
  ogType: "website",
  ogUrl: `https://${tenant}.example.com`,
  twitterTitle: tenant,
  twitterSite: `@${tenant}`,
  twitterCard: "summary_large_image",
  twitterDescription: `This is a description of ${tenant}`,
  twitterImage: `https://${tenant}.example.com/images/logo.png`,
  twitterImageAlt: tenant,
});

useHead({
  link: [
    {
      rel: "icon",
      type: "image/x-icon",
      href: "/site.ico",
    },
  ],
});
</script>
<template>
  <div>
    <div
      class="fixed top-0 left-0 w-full h-fit md:h-[65px] py-4 md:py-0 shadow-md bg-slate-900 z-50 text-slate-200"
    >
      <div class="max-w-[1280px] mx-auto">
        <div class="flex flex-col md:flex-row justify-between items-center">
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
    <div class="pt-[180px] md:pt-[90px] pb-8">
      <TenantTypeA v-if="tenant == 'company-a'" :site="tenant" />
      <TenantTypeB v-else-if="tenant == 'company-b'" :site="tenant" />
      <div v-else class="flex flex-col justify-center items-center">
        <h1>404</h1>
        <p>Company not found</p>
      </div>
    </div>
  </div>
</template>
