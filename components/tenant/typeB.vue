<script setup>
const props = defineProps({
  site: {
    type: String,
    default: "",
    required: true,
  },
});
</script>
<template>
  <div>
    <div class="max-w-[1280px] mx-auto px-4">
      <section
        class="min-h-96 relative flex flex-1 shrink-0 items-center justify-center overflow-hidden rounded-lg bg-gray-100 py-16 shadow-lg md:py-20 xl:py-48"
      >
        <!-- image - start -->
        <img
          src="https://images.unsplash.com/photo-1618004652321-13a63e576b80?auto=format&q=75&fit=crop&w=1500"
          loading="lazy"
          alt="Photo by Fakurian Design"
          class="absolute inset-0 h-full w-full object-cover object-center"
        />
        <!-- image - end -->

        <!-- overlay - start -->
        <div class="absolute inset-0 bg-indigo-500 mix-blend-multiply"></div>
        <!-- overlay - end -->

        <!-- text start -->
        <div class="relative flex flex-col items-center p-4 sm:max-w-xl">
          <p
            class="mb-4 text-center text-lg text-indigo-200 sm:text-xl md:mb-8"
          >
            Very proud to introduce
          </p>
          <h1
            class="mb-8 text-center text-4xl font-bold text-white sm:text-5xl md:mb-12 md:text-6xl"
          >
            Revolutionary way to build the web
          </h1>

          <div
            class="flex w-full flex-col gap-2.5 sm:flex-row sm:justify-center"
          >
            <a
              href="#"
              class="inline-block rounded-lg bg-indigo-500 px-8 py-3 text-center text-sm font-semibold text-white outline-none ring-indigo-300 transition duration-100 hover:bg-indigo-600 focus-visible:ring active:bg-indigo-700 md:text-base"
              >Start now</a
            >

            <a
              href="#"
              class="inline-block rounded-lg bg-gray-200 px-8 py-3 text-center text-sm font-semibold text-gray-500 outline-none ring-indigo-300 transition duration-100 hover:bg-gray-300 focus-visible:ring active:text-gray-700 md:text-base"
              >Take tour</a
            >
          </div>
        </div>
        <!-- text end -->
      </section>

      <hr class="my-8" />

      <!-- First Content -->
      <div class="mx-auto max-w-screen-xl">
        <!-- text - start -->
        <div class="mb-10 md:mb-10">
          <h2 class="mb-4 text-2xl font-bold text-gray-800 md:mb-6 lg:text-3xl">
            Blog
          </h2>

          <p class="max-w-screen-md text-gray-500 md:text-lg">
            This is a section of some simple filler text, also known as
            placeholder text. It shares some characteristics of a real written
            text but is random or otherwise generated.
          </p>
        </div>
        <!-- text - end -->

        <div
          class="grid gap-4 sm:grid-cols-2 md:gap-6 lg:grid-cols-2 xl:grid-cols-2 xl:gap-8"
        >
          <!-- article - start -->
          <div
            class="flex flex-col items-center overflow-hidden rounded-lg border md:flex-row"
          >
            <a
              href="#"
              class="group relative block h-48 w-full shrink-0 self-start overflow-hidden bg-gray-100 md:h-full md:w-32 lg:w-48"
            >
              <img
                src="https://images.unsplash.com/photo-1593508512255-86ab42a8e620?auto=format&q=75&fit=crop&w=600"
                loading="lazy"
                alt="Photo by Minh Pham"
                class="absolute inset-0 h-full w-full object-cover object-center transition duration-200 group-hover:scale-110"
              />
            </a>

            <div class="bg-white flex flex-col gap-2 p-4 lg:p-6">
              <span class="text-sm text-gray-400">July 19, 2021</span>

              <h2 class="text-xl font-bold text-gray-800">
                <a
                  href="#"
                  class="transition duration-100 hover:text-indigo-500 active:text-indigo-600"
                  >New trends in Tech</a
                >
              </h2>

              <p class="text-gray-500">
                This is a section of some simple filler text, also known as
                placeholder text.
              </p>

              <div>
                <a
                  href="#"
                  class="font-semibold text-indigo-500 transition duration-100 hover:text-indigo-600 active:text-indigo-700"
                  >Read more</a
                >
              </div>
            </div>
          </div>
          <!-- article - end -->

          <!-- article - start -->
          <div
            class="flex flex-col items-center overflow-hidden rounded-lg border md:flex-row"
          >
            <a
              href="#"
              class="group relative block h-48 w-full shrink-0 self-start overflow-hidden bg-gray-100 md:h-full md:w-32 lg:w-48"
            >
              <img
                src="https://images.unsplash.com/photo-1550745165-9bc0b252726f?auto=format&q=75&fit=crop&w=600"
                loading="lazy"
                alt="Photo by Lorenzo Herrera"
                class="absolute inset-0 h-full w-full object-cover object-center transition duration-200 group-hover:scale-110"
              />
            </a>

            <div class="bg-white flex flex-col gap-2 p-4 lg:p-6">
              <span class="text-sm text-gray-400">April 07, 2021</span>

              <h2 class="text-xl font-bold text-gray-800">
                <a
                  href="#"
                  class="transition duration-100 hover:text-indigo-500 active:text-indigo-600"
                  >Working with legacy stacks</a
                >
              </h2>

              <p class="text-gray-500">
                This is a section of some simple filler text, also known as
                placeholder text.
              </p>

              <div>
                <a
                  href="#"
                  class="font-semibold text-indigo-500 transition duration-100 hover:text-indigo-600 active:text-indigo-700"
                  >Read more</a
                >
              </div>
            </div>
          </div>
          <!-- article - end -->

          <!-- article - start -->
          <div
            class="flex flex-col items-center overflow-hidden rounded-lg border md:flex-row"
          >
            <a
              href="#"
              class="group relative block h-48 w-full shrink-0 self-start overflow-hidden bg-gray-100 md:h-full md:w-32 lg:w-48"
            >
              <img
                src="https://images.unsplash.com/photo-1542759564-7ccbb6ac450a?auto=format&q=75&fit=crop&w=600"
                loading="lazy"
                alt="Photo by Magicle"
                class="absolute inset-0 h-full w-full object-cover object-center transition duration-200 group-hover:scale-110"
              />
            </a>

            <div class="bg-white flex flex-col gap-2 p-4 lg:p-6">
              <span class="text-sm text-gray-400">March 15, 2021</span>

              <h2 class="text-xl font-bold text-gray-800">
                <a
                  href="#"
                  class="transition duration-100 hover:text-indigo-500 active:text-indigo-600"
                  >10 best smartphones for devs</a
                >
              </h2>

              <p class="text-gray-500">
                This is a section of some simple filler text, also known as
                placeholder text.
              </p>

              <div>
                <a
                  href="#"
                  class="font-semibold text-indigo-500 transition duration-100 hover:text-indigo-600 active:text-indigo-700"
                  >Read more</a
                >
              </div>
            </div>
          </div>
          <!-- article - end -->

          <!-- article - start -->
          <div
            class="flex flex-col items-center overflow-hidden rounded-lg border md:flex-row"
          >
            <a
              href="#"
              class="group relative block h-48 w-full shrink-0 self-start overflow-hidden bg-gray-100 md:h-full md:w-32 lg:w-48"
            >
              <img
                src="https://images.unsplash.com/photo-1610465299996-30f240ac2b1c?auto=format&q=75&fit=crop&w=600"
                loading="lazy"
                alt="Photo by Martin Sanchez"
                class="absolute inset-0 h-full w-full object-cover object-center transition duration-200 group-hover:scale-110"
              />
            </a>

            <div class="bg-white flex flex-col gap-2 p-4 lg:p-6">
              <span class="text-sm text-gray-400">January 27, 2021</span>

              <h2 class="text-xl font-bold text-gray-800">
                <a
                  href="#"
                  class="transition duration-100 hover:text-indigo-500 active:text-indigo-600"
                  >8 High performance Notebooks</a
                >
              </h2>

              <p class="text-gray-500">
                This is a section of some simple filler text, also known as
                placeholder text.
              </p>

              <div>
                <a
                  href="#"
                  class="font-semibold text-indigo-500 transition duration-100 hover:text-indigo-600 active:text-indigo-700"
                  >Read more</a
                >
              </div>
            </div>
          </div>
          <!-- article - end -->
        </div>
      </div>

      <hr class="my-8" />

      <!-- Second Content -->
      <div class="mx-auto max-w-screen-xl">
        <div class="grid gap-8 md:grid-cols-2 lg:gap-12">
          <div>
            <div
              class="h-64 overflow-hidden rounded-lg bg-gray-100 shadow-lg md:h-auto"
            >
              <img
                src="https://images.unsplash.com/photo-1610465299996-30f240ac2b1c?auto=format&q=75&fit=crop&w=600&h=750"
                loading="lazy"
                alt="Photo by Martin Sanchez"
                class="h-full w-full object-cover object-center"
              />
            </div>
          </div>

          <div class="md:pt-8">
            <p class="text-center font-bold text-indigo-500 md:text-left">
              Who we are
            </p>

            <h1
              class="mb-4 text-center text-2xl font-bold text-gray-800 sm:text-3xl md:mb-6 md:text-left"
            >
              Our competitive advantage
            </h1>

            <p class="mb-6 text-gray-500 sm:text-lg md:mb-8">
              This is a section of some simple filler text, also known as
              placeholder text. It shares some characteristics of a real written
              text but is random or otherwise generated. It may be used to
              display a sample of fonts or generate text for testing. Filler
              text is dummy text which has no meaning however looks very similar
              to real text.<br /><br />

              This is a section of some simple filler text, also known as
              placeholder text. It shares some characteristics of a real written
              text but is
              <a
                href="#"
                class="text-indigo-500 underline transition duration-100 hover:text-indigo-600 active:text-indigo-700"
                >random</a
              >
              or otherwise generated. It may be used to display a sample of
              fonts or generate text for testing. Filler text is dummy text
              which has no meaning however looks very similar to real text.
            </p>

            <h2
              class="mb-2 text-center text-xl font-semibold text-gray-800 sm:text-2xl md:mb-4 md:text-left"
            >
              About us
            </h2>

            <p class="mb-6 text-gray-500 sm:text-lg md:mb-8">
              This is a section of some simple filler text, also known as
              placeholder text. It shares some characteristics of a real written
              text but is random or otherwise generated. It may be used to
              display a sample of fonts or generate text for testing. Filler
              text is dummy text which has no meaning however looks very similar
              to real text.
            </p>
          </div>
        </div>
      </div>

      <hr class="my-8" />

      <div class="mx-auto max-w-screen-xl">
        <!-- text - start -->
        <div class="mb-10 md:mb-10">
          <h2 class="mb-4 text-2xl font-bold text-gray-800 md:mb-6 lg:text-3xl">
            Meet our Team
          </h2>

          <p class="max-w-screen-md text-gray-500 md:text-lg">
            This is a section of some simple filler text, also known as
            placeholder text. It shares some characteristics of a real written
            text but is random or otherwise generated.
          </p>
        </div>
        <!-- text - end -->
        <rs-card class="py-8">
          <div
            class="grid grid-cols-2 gap-x-4 gap-y-8 md:grid-cols-4 lg:gap-x-8 lg:gap-y-12"
          >
            <!-- person - start -->
            <div class="flex flex-col items-center">
              <div
                class="mb-2 h-24 w-24 overflow-hidden rounded-full bg-gray-100 shadow-lg md:mb-4 md:h-32 md:w-32"
              >
                <img
                  src="https://images.unsplash.com/photo-1567515004624-219c11d31f2e??auto=format&q=75&fit=crop&w=256"
                  loading="lazy"
                  alt="Photo by Radu Florin"
                  class="h-full w-full object-cover object-center"
                />
              </div>

              <div>
                <div class="text-center font-bold text-indigo-500 md:text-lg">
                  John McCulling
                </div>
                <p
                  class="mb-3 text-center text-sm text-gray-500 md:mb-4 md:text-base"
                >
                  Founder / CEO
                </p>

                <!-- social - start -->
                <div class="flex justify-center">
                  <div class="flex gap-4">
                    <a
                      href="#"
                      target="_blank"
                      class="text-gray-400 transition duration-100 hover:text-gray-500 active:text-gray-600"
                    >
                      <svg
                        class="h-5 w-5"
                        width="24"
                        height="24"
                        viewBox="0 0 24 24"
                        fill="currentColor"
                        xmlns="http://www.w3.org/2000/svg"
                      >
                        <path
                          d="M19 0h-14c-2.761 0-5 2.239-5 5v14c0 2.761 2.239 5 5 5h14c2.762 0 5-2.239 5-5v-14c0-2.761-2.238-5-5-5zm-11 19h-3v-11h3v11zm-1.5-12.268c-.966 0-1.75-.79-1.75-1.764s.784-1.764 1.75-1.764 1.75.79 1.75 1.764-.783 1.764-1.75 1.764zm13.5 12.268h-3v-5.604c0-3.368-4-3.113-4 0v5.604h-3v-11h3v1.765c1.396-2.586 7-2.777 7 2.476v6.759z"
                        />
                      </svg>
                    </a>

                    <a
                      href="#"
                      target="_blank"
                      class="text-gray-400 transition duration-100 hover:text-gray-500 active:text-gray-600"
                    >
                      <svg
                        class="h-5 w-5"
                        width="24"
                        height="24"
                        viewBox="0 0 24 24"
                        fill="currentColor"
                        xmlns="http://www.w3.org/2000/svg"
                      >
                        <path
                          d="M24 4.557c-.883.392-1.832.656-2.828.775 1.017-.609 1.798-1.574 2.165-2.724-.951.564-2.005.974-3.127 1.195-.897-.957-2.178-1.555-3.594-1.555-3.179 0-5.515 2.966-4.797 6.045-4.091-.205-7.719-2.165-10.148-5.144-1.29 2.213-.669 5.108 1.523 6.574-.806-.026-1.566-.247-2.229-.616-.054 2.281 1.581 4.415 3.949 4.89-.693.188-1.452.232-2.224.084.626 1.956 2.444 3.379 4.6 3.419-2.07 1.623-4.678 2.348-7.29 2.04 2.179 1.397 4.768 2.212 7.548 2.212 9.142 0 14.307-7.721 13.995-14.646.962-.695 1.797-1.562 2.457-2.549z"
                        />
                      </svg>
                    </a>
                  </div>
                </div>
                <!-- social - end -->
              </div>
            </div>
            <!-- person - end -->

            <!-- person - start -->
            <div class="flex flex-col items-center">
              <div
                class="mb-2 h-24 w-24 overflow-hidden rounded-full bg-gray-100 shadow-lg md:mb-4 md:h-32 md:w-32"
              >
                <img
                  src="https://images.unsplash.com/photo-1532073150508-0c1df022bdd1?auto=format&q=75&fit=crop&w=256"
                  loading="lazy"
                  alt="Photo by christian ferrer"
                  class="h-full w-full object-cover object-center"
                />
              </div>

              <div>
                <div class="text-center font-bold text-indigo-500 md:text-lg">
                  Kate Berg
                </div>
                <p
                  class="mb-3 text-center text-sm text-gray-500 md:mb-4 md:text-base"
                >
                  CFO
                </p>

                <!-- social - start -->
                <div class="flex justify-center">
                  <div class="flex gap-4">
                    <a
                      href="#"
                      target="_blank"
                      class="text-gray-400 transition duration-100 hover:text-gray-500 active:text-gray-600"
                    >
                      <svg
                        class="h-5 w-5"
                        width="24"
                        height="24"
                        viewBox="0 0 24 24"
                        fill="currentColor"
                        xmlns="http://www.w3.org/2000/svg"
                      >
                        <path
                          d="M19 0h-14c-2.761 0-5 2.239-5 5v14c0 2.761 2.239 5 5 5h14c2.762 0 5-2.239 5-5v-14c0-2.761-2.238-5-5-5zm-11 19h-3v-11h3v11zm-1.5-12.268c-.966 0-1.75-.79-1.75-1.764s.784-1.764 1.75-1.764 1.75.79 1.75 1.764-.783 1.764-1.75 1.764zm13.5 12.268h-3v-5.604c0-3.368-4-3.113-4 0v5.604h-3v-11h3v1.765c1.396-2.586 7-2.777 7 2.476v6.759z"
                        />
                      </svg>
                    </a>

                    <a
                      href="#"
                      target="_blank"
                      class="text-gray-400 transition duration-100 hover:text-gray-500 active:text-gray-600"
                    >
                      <svg
                        class="h-5 w-5"
                        width="24"
                        height="24"
                        viewBox="0 0 24 24"
                        fill="currentColor"
                        xmlns="http://www.w3.org/2000/svg"
                      >
                        <path
                          d="M24 4.557c-.883.392-1.832.656-2.828.775 1.017-.609 1.798-1.574 2.165-2.724-.951.564-2.005.974-3.127 1.195-.897-.957-2.178-1.555-3.594-1.555-3.179 0-5.515 2.966-4.797 6.045-4.091-.205-7.719-2.165-10.148-5.144-1.29 2.213-.669 5.108 1.523 6.574-.806-.026-1.566-.247-2.229-.616-.054 2.281 1.581 4.415 3.949 4.89-.693.188-1.452.232-2.224.084.626 1.956 2.444 3.379 4.6 3.419-2.07 1.623-4.678 2.348-7.29 2.04 2.179 1.397 4.768 2.212 7.548 2.212 9.142 0 14.307-7.721 13.995-14.646.962-.695 1.797-1.562 2.457-2.549z"
                        />
                      </svg>
                    </a>
                  </div>
                </div>
                <!-- social - end -->
              </div>
            </div>
            <!-- person - end -->

            <!-- person - start -->
            <div class="flex flex-col items-center">
              <div
                class="mb-2 h-24 w-24 overflow-hidden rounded-full bg-gray-100 shadow-lg md:mb-4 md:h-32 md:w-32"
              >
                <img
                  src="https://images.unsplash.com/photo-1463453091185-61582044d556?auto=format&q=75&fit=crop&w=256"
                  loading="lazy"
                  alt="Photo by Ayo Ogunseinde"
                  class="h-full w-full object-cover object-center"
                />
              </div>

              <div>
                <div class="text-center font-bold text-indigo-500 md:text-lg">
                  Greg Jackson
                </div>
                <p
                  class="mb-3 text-center text-sm text-gray-500 md:mb-4 md:text-base"
                >
                  CTO
                </p>

                <!-- social - start -->
                <div class="flex justify-center">
                  <div class="flex gap-4">
                    <a
                      href="#"
                      target="_blank"
                      class="text-gray-400 transition duration-100 hover:text-gray-500 active:text-gray-600"
                    >
                      <svg
                        class="h-5 w-5"
                        width="24"
                        height="24"
                        viewBox="0 0 24 24"
                        fill="currentColor"
                        xmlns="http://www.w3.org/2000/svg"
                      >
                        <path
                          d="M19 0h-14c-2.761 0-5 2.239-5 5v14c0 2.761 2.239 5 5 5h14c2.762 0 5-2.239 5-5v-14c0-2.761-2.238-5-5-5zm-11 19h-3v-11h3v11zm-1.5-12.268c-.966 0-1.75-.79-1.75-1.764s.784-1.764 1.75-1.764 1.75.79 1.75 1.764-.783 1.764-1.75 1.764zm13.5 12.268h-3v-5.604c0-3.368-4-3.113-4 0v5.604h-3v-11h3v1.765c1.396-2.586 7-2.777 7 2.476v6.759z"
                        />
                      </svg>
                    </a>

                    <a
                      href="#"
                      target="_blank"
                      class="text-gray-400 transition duration-100 hover:text-gray-500 active:text-gray-600"
                    >
                      <svg
                        class="h-5 w-5"
                        width="24"
                        height="24"
                        viewBox="0 0 24 24"
                        fill="currentColor"
                        xmlns="http://www.w3.org/2000/svg"
                      >
                        <path
                          d="M24 4.557c-.883.392-1.832.656-2.828.775 1.017-.609 1.798-1.574 2.165-2.724-.951.564-2.005.974-3.127 1.195-.897-.957-2.178-1.555-3.594-1.555-3.179 0-5.515 2.966-4.797 6.045-4.091-.205-7.719-2.165-10.148-5.144-1.29 2.213-.669 5.108 1.523 6.574-.806-.026-1.566-.247-2.229-.616-.054 2.281 1.581 4.415 3.949 4.89-.693.188-1.452.232-2.224.084.626 1.956 2.444 3.379 4.6 3.419-2.07 1.623-4.678 2.348-7.29 2.04 2.179 1.397 4.768 2.212 7.548 2.212 9.142 0 14.307-7.721 13.995-14.646.962-.695 1.797-1.562 2.457-2.549z"
                        />
                      </svg>
                    </a>
                  </div>
                </div>
                <!-- social - end -->
              </div>
            </div>
            <!-- person - end -->

            <!-- person - start -->
            <div class="flex flex-col items-center">
              <div
                class="mb-2 h-24 w-24 overflow-hidden rounded-full bg-gray-100 shadow-lg md:mb-4 md:h-32 md:w-32"
              >
                <img
                  src="https://images.unsplash.com/photo-1529068755536-a5ade0dcb4e8?auto=format&q=75&fit=crop&w=256"
                  loading="lazy"
                  alt="Photo by Midas Hofstra"
                  class="h-full w-full object-cover object-center"
                />
              </div>

              <div>
                <div class="text-center font-bold text-indigo-500 md:text-lg">
                  Robert Greyson
                </div>
                <p
                  class="mb-3 text-center text-sm text-gray-500 md:mb-4 md:text-base"
                >
                  Creative Director
                </p>

                <!-- social - start -->
                <div class="flex justify-center">
                  <div class="flex gap-4">
                    <a
                      href="#"
                      target="_blank"
                      class="text-gray-400 transition duration-100 hover:text-gray-500 active:text-gray-600"
                    >
                      <svg
                        class="h-5 w-5"
                        width="24"
                        height="24"
                        viewBox="0 0 24 24"
                        fill="currentColor"
                        xmlns="http://www.w3.org/2000/svg"
                      >
                        <path
                          d="M19 0h-14c-2.761 0-5 2.239-5 5v14c0 2.761 2.239 5 5 5h14c2.762 0 5-2.239 5-5v-14c0-2.761-2.238-5-5-5zm-11 19h-3v-11h3v11zm-1.5-12.268c-.966 0-1.75-.79-1.75-1.764s.784-1.764 1.75-1.764 1.75.79 1.75 1.764-.783 1.764-1.75 1.764zm13.5 12.268h-3v-5.604c0-3.368-4-3.113-4 0v5.604h-3v-11h3v1.765c1.396-2.586 7-2.777 7 2.476v6.759z"
                        />
                      </svg>
                    </a>

                    <a
                      href="#"
                      target="_blank"
                      class="text-gray-400 transition duration-100 hover:text-gray-500 active:text-gray-600"
                    >
                      <svg
                        class="h-5 w-5"
                        width="24"
                        height="24"
                        viewBox="0 0 24 24"
                        fill="currentColor"
                        xmlns="http://www.w3.org/2000/svg"
                      >
                        <path
                          d="M24 4.557c-.883.392-1.832.656-2.828.775 1.017-.609 1.798-1.574 2.165-2.724-.951.564-2.005.974-3.127 1.195-.897-.957-2.178-1.555-3.594-1.555-3.179 0-5.515 2.966-4.797 6.045-4.091-.205-7.719-2.165-10.148-5.144-1.29 2.213-.669 5.108 1.523 6.574-.806-.026-1.566-.247-2.229-.616-.054 2.281 1.581 4.415 3.949 4.89-.693.188-1.452.232-2.224.084.626 1.956 2.444 3.379 4.6 3.419-2.07 1.623-4.678 2.348-7.29 2.04 2.179 1.397 4.768 2.212 7.548 2.212 9.142 0 14.307-7.721 13.995-14.646.962-.695 1.797-1.562 2.457-2.549z"
                        />
                      </svg>
                    </a>
                  </div>
                </div>
                <!-- social - end -->
              </div>
            </div>
            <!-- person - end -->

            <!-- person - start -->
            <div class="flex flex-col items-center">
              <div
                class="mb-2 h-24 w-24 overflow-hidden rounded-full bg-gray-100 shadow-lg md:mb-4 md:h-32 md:w-32"
              >
                <img
                  src="https://images.unsplash.com/photo-1522529599102-193c0d76b5b6?auto=format&q=75&fit=crop&w=256"
                  loading="lazy"
                  alt="Photo by Elizeu Dias"
                  class="h-full w-full object-cover object-center"
                />
              </div>

              <div>
                <div class="text-center font-bold text-indigo-500 md:text-lg">
                  John Roberts
                </div>
                <p
                  class="mb-3 text-center text-sm text-gray-500 md:mb-4 md:text-base"
                >
                  Investor Relations
                </p>

                <!-- social - start -->
                <div class="flex justify-center">
                  <div class="flex gap-4">
                    <a
                      href="#"
                      target="_blank"
                      class="text-gray-400 transition duration-100 hover:text-gray-500 active:text-gray-600"
                    >
                      <svg
                        class="h-5 w-5"
                        width="24"
                        height="24"
                        viewBox="0 0 24 24"
                        fill="currentColor"
                        xmlns="http://www.w3.org/2000/svg"
                      >
                        <path
                          d="M19 0h-14c-2.761 0-5 2.239-5 5v14c0 2.761 2.239 5 5 5h14c2.762 0 5-2.239 5-5v-14c0-2.761-2.238-5-5-5zm-11 19h-3v-11h3v11zm-1.5-12.268c-.966 0-1.75-.79-1.75-1.764s.784-1.764 1.75-1.764 1.75.79 1.75 1.764-.783 1.764-1.75 1.764zm13.5 12.268h-3v-5.604c0-3.368-4-3.113-4 0v5.604h-3v-11h3v1.765c1.396-2.586 7-2.777 7 2.476v6.759z"
                        />
                      </svg>
                    </a>

                    <a
                      href="#"
                      target="_blank"
                      class="text-gray-400 transition duration-100 hover:text-gray-500 active:text-gray-600"
                    >
                      <svg
                        class="h-5 w-5"
                        width="24"
                        height="24"
                        viewBox="0 0 24 24"
                        fill="currentColor"
                        xmlns="http://www.w3.org/2000/svg"
                      >
                        <path
                          d="M24 4.557c-.883.392-1.832.656-2.828.775 1.017-.609 1.798-1.574 2.165-2.724-.951.564-2.005.974-3.127 1.195-.897-.957-2.178-1.555-3.594-1.555-3.179 0-5.515 2.966-4.797 6.045-4.091-.205-7.719-2.165-10.148-5.144-1.29 2.213-.669 5.108 1.523 6.574-.806-.026-1.566-.247-2.229-.616-.054 2.281 1.581 4.415 3.949 4.89-.693.188-1.452.232-2.224.084.626 1.956 2.444 3.379 4.6 3.419-2.07 1.623-4.678 2.348-7.29 2.04 2.179 1.397 4.768 2.212 7.548 2.212 9.142 0 14.307-7.721 13.995-14.646.962-.695 1.797-1.562 2.457-2.549z"
                        />
                      </svg>
                    </a>
                  </div>
                </div>
                <!-- social - end -->
              </div>
            </div>
            <!-- person - end -->

            <!-- person - start -->
            <div class="flex flex-col items-center">
              <div
                class="mb-2 h-24 w-24 overflow-hidden rounded-full bg-gray-100 shadow-lg md:mb-4 md:h-32 md:w-32"
              >
                <img
                  src="https://images.unsplash.com/photo-1488426862026-3ee34a7d66df?auto=format&q=75&fit=crop&w=256"
                  loading="lazy"
                  alt="Photo by Matheus Ferrero"
                  class="h-full w-full object-cover object-center"
                />
              </div>

              <div>
                <div class="text-center font-bold text-indigo-500 md:text-lg">
                  Judy Amandez
                </div>
                <p
                  class="mb-3 text-center text-sm text-gray-500 md:mb-4 md:text-base"
                >
                  Senior Art Director
                </p>

                <!-- social - start -->
                <div class="flex justify-center">
                  <div class="flex gap-4">
                    <a
                      href="#"
                      target="_blank"
                      class="text-gray-400 transition duration-100 hover:text-gray-500 active:text-gray-600"
                    >
                      <svg
                        class="h-5 w-5"
                        width="24"
                        height="24"
                        viewBox="0 0 24 24"
                        fill="currentColor"
                        xmlns="http://www.w3.org/2000/svg"
                      >
                        <path
                          d="M19 0h-14c-2.761 0-5 2.239-5 5v14c0 2.761 2.239 5 5 5h14c2.762 0 5-2.239 5-5v-14c0-2.761-2.238-5-5-5zm-11 19h-3v-11h3v11zm-1.5-12.268c-.966 0-1.75-.79-1.75-1.764s.784-1.764 1.75-1.764 1.75.79 1.75 1.764-.783 1.764-1.75 1.764zm13.5 12.268h-3v-5.604c0-3.368-4-3.113-4 0v5.604h-3v-11h3v1.765c1.396-2.586 7-2.777 7 2.476v6.759z"
                        />
                      </svg>
                    </a>

                    <a
                      href="#"
                      target="_blank"
                      class="text-gray-400 transition duration-100 hover:text-gray-500 active:text-gray-600"
                    >
                      <svg
                        class="h-5 w-5"
                        width="24"
                        height="24"
                        viewBox="0 0 24 24"
                        fill="currentColor"
                        xmlns="http://www.w3.org/2000/svg"
                      >
                        <path
                          d="M24 4.557c-.883.392-1.832.656-2.828.775 1.017-.609 1.798-1.574 2.165-2.724-.951.564-2.005.974-3.127 1.195-.897-.957-2.178-1.555-3.594-1.555-3.179 0-5.515 2.966-4.797 6.045-4.091-.205-7.719-2.165-10.148-5.144-1.29 2.213-.669 5.108 1.523 6.574-.806-.026-1.566-.247-2.229-.616-.054 2.281 1.581 4.415 3.949 4.89-.693.188-1.452.232-2.224.084.626 1.956 2.444 3.379 4.6 3.419-2.07 1.623-4.678 2.348-7.29 2.04 2.179 1.397 4.768 2.212 7.548 2.212 9.142 0 14.307-7.721 13.995-14.646.962-.695 1.797-1.562 2.457-2.549z"
                        />
                      </svg>
                    </a>
                  </div>
                </div>
                <!-- social - end -->
              </div>
            </div>
            <!-- person - end -->

            <!-- person - start -->
            <div class="flex flex-col items-center">
              <div
                class="mb-2 h-24 w-24 overflow-hidden rounded-full bg-gray-100 shadow-lg md:mb-4 md:h-32 md:w-32"
              >
                <img
                  src="https://images.unsplash.com/photo-1566492031773-4f4e44671857?auto=format&q=75&fit=crop&w=256"
                  loading="lazy"
                  alt="Photo by Leilani Angel"
                  class="h-full w-full object-cover object-center"
                />
              </div>

              <div>
                <div class="text-center font-bold text-indigo-500 md:text-lg">
                  Rahul Williams
                </div>
                <p
                  class="mb-3 text-center text-sm text-gray-500 md:mb-4 md:text-base"
                >
                  Creative Director
                </p>

                <!-- social - start -->
                <div class="flex justify-center">
                  <div class="flex gap-4">
                    <a
                      href="#"
                      target="_blank"
                      class="text-gray-400 transition duration-100 hover:text-gray-500 active:text-gray-600"
                    >
                      <svg
                        class="h-5 w-5"
                        width="24"
                        height="24"
                        viewBox="0 0 24 24"
                        fill="currentColor"
                        xmlns="http://www.w3.org/2000/svg"
                      >
                        <path
                          d="M19 0h-14c-2.761 0-5 2.239-5 5v14c0 2.761 2.239 5 5 5h14c2.762 0 5-2.239 5-5v-14c0-2.761-2.238-5-5-5zm-11 19h-3v-11h3v11zm-1.5-12.268c-.966 0-1.75-.79-1.75-1.764s.784-1.764 1.75-1.764 1.75.79 1.75 1.764-.783 1.764-1.75 1.764zm13.5 12.268h-3v-5.604c0-3.368-4-3.113-4 0v5.604h-3v-11h3v1.765c1.396-2.586 7-2.777 7 2.476v6.759z"
                        />
                      </svg>
                    </a>

                    <a
                      href="#"
                      target="_blank"
                      class="text-gray-400 transition duration-100 hover:text-gray-500 active:text-gray-600"
                    >
                      <svg
                        class="h-5 w-5"
                        width="24"
                        height="24"
                        viewBox="0 0 24 24"
                        fill="currentColor"
                        xmlns="http://www.w3.org/2000/svg"
                      >
                        <path
                          d="M24 4.557c-.883.392-1.832.656-2.828.775 1.017-.609 1.798-1.574 2.165-2.724-.951.564-2.005.974-3.127 1.195-.897-.957-2.178-1.555-3.594-1.555-3.179 0-5.515 2.966-4.797 6.045-4.091-.205-7.719-2.165-10.148-5.144-1.29 2.213-.669 5.108 1.523 6.574-.806-.026-1.566-.247-2.229-.616-.054 2.281 1.581 4.415 3.949 4.89-.693.188-1.452.232-2.224.084.626 1.956 2.444 3.379 4.6 3.419-2.07 1.623-4.678 2.348-7.29 2.04 2.179 1.397 4.768 2.212 7.548 2.212 9.142 0 14.307-7.721 13.995-14.646.962-.695 1.797-1.562 2.457-2.549z"
                        />
                      </svg>
                    </a>
                  </div>
                </div>
                <!-- social - end -->
              </div>
            </div>
            <!-- person - end -->

            <!-- person - start -->
            <div class="flex flex-col items-center">
              <div
                class="mb-2 h-24 w-24 overflow-hidden rounded-full bg-gray-100 shadow-lg md:mb-4 md:h-32 md:w-32"
              >
                <img
                  src="https://images.unsplash.com/photo-1562904403-a5106bef8319?auto=format&q=75&fit=crop&w=256"
                  loading="lazy"
                  alt="Photo by Jernej Graj"
                  class="h-full w-full object-cover object-center"
                />
              </div>

              <div>
                <div class="text-center font-bold text-indigo-500 md:text-lg">
                  Ari Ferris
                </div>
                <p
                  class="mb-3 text-center text-sm text-gray-500 md:mb-4 md:text-base"
                >
                  Marketing Analyst
                </p>

                <!-- social - start -->
                <div class="flex justify-center">
                  <div class="flex gap-4">
                    <a
                      href="#"
                      target="_blank"
                      class="text-gray-400 transition duration-100 hover:text-gray-500 active:text-gray-600"
                    >
                      <svg
                        class="h-5 w-5"
                        width="24"
                        height="24"
                        viewBox="0 0 24 24"
                        fill="currentColor"
                        xmlns="http://www.w3.org/2000/svg"
                      >
                        <path
                          d="M19 0h-14c-2.761 0-5 2.239-5 5v14c0 2.761 2.239 5 5 5h14c2.762 0 5-2.239 5-5v-14c0-2.761-2.238-5-5-5zm-11 19h-3v-11h3v11zm-1.5-12.268c-.966 0-1.75-.79-1.75-1.764s.784-1.764 1.75-1.764 1.75.79 1.75 1.764-.783 1.764-1.75 1.764zm13.5 12.268h-3v-5.604c0-3.368-4-3.113-4 0v5.604h-3v-11h3v1.765c1.396-2.586 7-2.777 7 2.476v6.759z"
                        />
                      </svg>
                    </a>

                    <a
                      href="#"
                      target="_blank"
                      class="text-gray-400 transition duration-100 hover:text-gray-500 active:text-gray-600"
                    >
                      <svg
                        class="h-5 w-5"
                        width="24"
                        height="24"
                        viewBox="0 0 24 24"
                        fill="currentColor"
                        xmlns="http://www.w3.org/2000/svg"
                      >
                        <path
                          d="M24 4.557c-.883.392-1.832.656-2.828.775 1.017-.609 1.798-1.574 2.165-2.724-.951.564-2.005.974-3.127 1.195-.897-.957-2.178-1.555-3.594-1.555-3.179 0-5.515 2.966-4.797 6.045-4.091-.205-7.719-2.165-10.148-5.144-1.29 2.213-.669 5.108 1.523 6.574-.806-.026-1.566-.247-2.229-.616-.054 2.281 1.581 4.415 3.949 4.89-.693.188-1.452.232-2.224.084.626 1.956 2.444 3.379 4.6 3.419-2.07 1.623-4.678 2.348-7.29 2.04 2.179 1.397 4.768 2.212 7.548 2.212 9.142 0 14.307-7.721 13.995-14.646.962-.695 1.797-1.562 2.457-2.549z"
                        />
                      </svg>
                    </a>
                  </div>
                </div>
                <!-- social - end -->
              </div>
            </div>
            <!-- person - end -->
          </div>
        </rs-card>
      </div>
    </div>
  </div>
</template>
