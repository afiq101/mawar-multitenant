<script setup>
import { DateTime } from "luxon";

const props = defineProps({
  site: {
    type: String,
    default: "",
    required: true,
  },
});

const timeNow = ref(null);
const hour = ref(null);
const minute = ref(null);
const second = ref(null);
const dateNow = ref(null);

const setTimer = () => {
  const now = DateTime.now().setZone("Asia/Kuala_Lumpur");
  timeNow.value = now.toLocaleString(DateTime.DATETIME_MED);

  // make sure every timer has 0 if less than 10
  hour.value = now.hour < 10 ? `0${now.hour}` : now.hour;
  minute.value = now.minute < 10 ? `0${now.minute}` : now.minute;
  second.value = now.second < 10 ? `0${now.second}` : now.second;
};

onMounted(() => {
  let now = DateTime.now().setZone("Asia/Kuala_Lumpur");

  // Convert to dd/MM/YYYY
  dateNow.value = now.toLocaleString(DateTime.DATE_MED);

  setTimer();

  setInterval(() => {
    setTimer();
  }, 1000);
});
</script>

<template>
  <div>
    <div class="max-w-[1280px] mx-auto px-4">
      <div>
        <div class="flex justify-between">
          <h4 class="mb-4 uppercase">Dashboard</h4>
        </div>
      </div>

      <div class="grid grid-cols-1 md:grid-cols-12 gap-x-4">
        <div class="col-span-1 md:col-span-8">
          <rs-card class="p-5">
            <!-- STORE CATEGORY -->
            <div class="flex flex-col mb-5">
              <h5>Store</h5>
              <p class="text-sm text-zinc/60 font-medium">
                Lorem ipsum dolor sit amet consectetur adipisicing elit.
              </p>
              <hr class="my-3" />
              <div class="grid grid-cols-1 gap-4 mt-1">
                <nuxt-link to="/add">
                  <div
                    class="h-[100px] flex justify-center items-center border-[3px] border-dotted rounded-md hover:bg-zinc/5 transition duration-200 ease-in-out cursor-pointer"
                  >
                    <Icon name="ph:plus" />
                  </div>
                </nuxt-link>
                <div
                  class="flex shadow-md border rounded-md hover:shadow-lg transition duration-200 ease-in-out cursor-pointer"
                >
                  <div class="h-[100px] w-[150px]">
                    <img
                      src="@/assets/img/default-thumbnail.jpg"
                      alt="image"
                      class="h-full w-full object-cover"
                    />
                  </div>
                  <div class="p-4">
                    <div class="mb-1">
                      <h6 class="leading-none line-clamp-1">Trash Taste</h6>
                      <span class="text-sm font-medium text-zinc/60">
                        Simple Page
                      </span>
                    </div>

                    <p class="text-secondary">
                      <Icon name="ph:link-simple-horizontal" class="w-4 h-4" />
                      <span class="ml-2 text-xs">
                        https://simple-page.example.com
                      </span>
                    </p>
                  </div>
                </div>
                <div
                  class="flex shadow-md border rounded-md hover:shadow-lg transition duration-200 ease-in-out cursor-pointer"
                >
                  <div class="h-[100px] w-[150px]">
                    <img
                      src="@/assets/img/default-thumbnail.jpg"
                      alt="image"
                      class="h-full w-full object-cover"
                    />
                  </div>
                  <div class="p-4">
                    <div class="mb-1">
                      <h6 class="leading-none line-clamp-1">Bakery Store</h6>
                      <span class="text-sm font-medium text-zinc/60">
                        Single Product
                      </span>
                    </div>
                    <p class="text-secondary">
                      <Icon name="ph:link-simple-horizontal" class="w-4 h-4" />
                      <span class="ml-2 text-xs">
                        https://single-product.example.com
                      </span>
                    </p>
                  </div>
                </div>
              </div>
            </div>

            <!-- CROWDFUND CATEGORY -->
            <div class="flex flex-col mb-5">
              <h5>Crowdfunding</h5>
              <p class="text-sm text-zinc/60 font-medium">
                Lorem ipsum dolor sit amet consectetur adipisicing elit.
              </p>
              <hr class="my-3" />
              <div class="grid grid-cols-1 gap-4 mt-1">
                <nuxt-link to="/add">
                  <div
                    class="h-[100px] flex justify-center items-center border-[3px] border-dotted rounded-md hover:bg-zinc/5 transition duration-200 ease-in-out cursor-pointer"
                  >
                    <Icon name="ph:plus" />
                  </div>
                </nuxt-link>
                <div
                  class="flex shadow-md border rounded-md hover:shadow-lg transition duration-200 ease-in-out cursor-pointer"
                >
                  <div class="h-[100px] w-[150px]">
                    <img
                      src="@/assets/img/default-thumbnail.jpg"
                      alt="image"
                      class="h-full w-full object-cover"
                    />
                  </div>
                  <div class="p-4">
                    <div class="mb-1">
                      <h6 class="leading-none line-clamp-1">
                        Gaza Emergency Relief Fundraiser
                      </h6>
                      <span class="text-sm font-medium text-zinc/60">
                        Non Profit
                      </span>
                    </div>

                    <p class="text-secondary">
                      <Icon name="ph:link-simple-horizontal" class="w-4 h-4" />
                      <span class="ml-2 text-xs">
                        https://gaza-will-be-free.example.com
                      </span>
                    </p>
                  </div>
                </div>
              </div>
            </div>
          </rs-card>
        </div>
        <div class="col-span-1 md:col-span-4 flex flex-col">
          <rs-card class="p-5 relative">
            <div class="flex justify-center items-center text-4xl text-zinc/80">
              <div class="flex flex-col justify-between items-start">
                <div class="border-r-2 pr-4">
                  {{ hour }}
                </div>
                <span class="text-xs ml-[5px]">Hours</span>
              </div>
              <div class="flex flex-col justify-between items-start">
                <div class="border-r-2 px-4">
                  {{ minute }}
                </div>
                <span class="flex justify-center items-center text-xs mx-4">
                  Minutes
                </span>
              </div>
              <div class="flex flex-col justify-between items-start">
                <div class="pl-4">
                  {{ second }}
                </div>
                <span class="text-xs ml-3">Seconds</span>
              </div>
            </div>

            <div
              class="absolute bottom-1 right-1 text-xs text-zinc/60 font-medium"
            >
              {{ dateNow }}
            </div>
          </rs-card>
          <rs-card class="p-5">
            <h5>Quick Action</h5>
            <p class="text-sm text-zinc/60 font-medium">
              Lorem ipsum dolor sit amet consectetur adipisicing elit.
            </p>
            <hr class="my-3" />
            <div class="grid grid-cols-3 gap-4 mt-1">
              <div class="flex flex-col justify-center items-center gap-y-2">
                <nuxt-link
                  to="/"
                  class="flex justify-center items-center border w-[50px] h-[50px] rounded-md hover:bg-zinc/5 transition duration-200 ease-in-out shadow-sm hover:scale-105"
                >
                  <Icon
                    name="ph:user-circle-gear"
                    class="!w-6 !h-6 text-secondary"
                  />
                </nuxt-link>

                <span class="text-sm font-medium text-center text-secondary">
                  Account
                  <br />
                  Settings
                </span>
              </div>
              <div class="flex flex-col justify-center items-center gap-y-2">
                <nuxt-link
                  to="/"
                  class="flex justify-center items-center border w-[50px] h-[50px] rounded-md hover:bg-zinc/5 transition duration-200 ease-in-out shadow-sm hover:scale-105"
                >
                  <Icon
                    name="ph:credit-card"
                    class="!w-6 !h-6 text-secondary"
                  />
                </nuxt-link>

                <span class="text-sm font-medium text-center text-secondary">
                  Payment
                  <br />
                  Settings
                </span>
              </div>
              <div class="flex flex-col justify-center items-center gap-y-2">
                <nuxt-link
                  to="/"
                  class="flex justify-center items-center border w-[50px] h-[50px] rounded-md hover:bg-zinc/5 transition duration-200 ease-in-out shadow-sm hover:scale-105"
                >
                  <Icon
                    name="ph:arrow-clockwise"
                    class="!w-6 !h-6 text-secondary"
                  />
                </nuxt-link>

                <span class="text-sm font-medium text-center text-secondary">
                  Manage
                  <br />
                  Subscription
                </span>
              </div>
              <div class="flex flex-col justify-center items-center gap-y-2">
                <nuxt-link
                  to="/"
                  class="flex justify-center items-center border w-[50px] h-[50px] rounded-md hover:bg-zinc/5 transition duration-200 ease-in-out shadow-sm hover:scale-105"
                >
                  <Icon name="ph:browsers" class="!w-6 !h-6 text-secondary" />
                </nuxt-link>

                <span class="text-sm font-medium text-center text-secondary">
                  Manage
                  <br />
                  Sites
                </span>
              </div>
              <div class="flex flex-col justify-center items-center gap-y-2">
                <nuxt-link
                  to="/"
                  class="flex justify-center items-center border w-[50px] h-[50px] rounded-md hover:bg-zinc/5 transition duration-200 ease-in-out shadow-sm hover:scale-105"
                >
                  <Icon
                    name="ph:presentation-chart"
                    class="!w-6 !h-6 text-secondary"
                  />
                </nuxt-link>

                <span class="text-sm font-medium text-center text-secondary">
                  Sites
                  <br />
                  Analytics
                </span>
              </div>
            </div>
          </rs-card>
          <rs-card class="p-5">
            <h5>Notification</h5>
            <p class="text-sm text-zinc/60 font-medium">
              Lorem ipsum dolor sit amet consectetur adipisicing elit.
            </p>
            <hr class="my-3" />

            <div class="flex flex-col">
              <div class="flex items-center py-2">
                <img
                  src="@/assets/img/default-thumbnail.jpg"
                  alt="profile"
                  class="w-[50px] h-[50px] object-cover rounded-full"
                />
                <div class="ml-3">
                  <p class="text-sm font-medium text-secondary">John Doe</p>
                  <p class="text-xs text-zinc/60 line-clamp-2">
                    Lorem ipsum dolor sit amet, consectetur adipisicing elit.
                    Nemo eius hic aut voluptas voluptates quidem, aliquam ipsa
                    cum quas expedita tempore error dolorum culpa illum
                    accusantium laborum ad rerum! Beatae!
                  </p>
                </div>
              </div>
              <hr class="my-2" />
              <div class="flex items-center py-2">
                <img
                  src="@/assets/img/default-thumbnail.jpg"
                  alt="profile"
                  class="w-[50px] h-[50px] object-cover rounded-full"
                />
                <div class="ml-3">
                  <p class="text-sm font-medium text-secondary">
                    Kimmy Granger
                  </p>
                  <p class="text-xs text-zinc/60 line-clamp-2">
                    Lorem ipsum dolor sit amet, consectetur adipisicing elit.
                    Nemo eius hic aut voluptas voluptates quidem, aliquam ipsa
                    cum quas expedita tempore error dolorum culpa illum
                    accusantium laborum ad rerum! Beatae!
                  </p>
                </div>
              </div>
              <hr class="my-2" />
            </div>
          </rs-card>
        </div>
      </div>
    </div>
  </div>
</template>
