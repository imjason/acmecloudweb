<!-- ~/components/Header.vue -->
<template>
    <header
        class="flex flex-wrap md:justify-start md:flex-nowrap z-50 w-full py-7"
      >
        <nav
          class="relative max-w-7xl w-full flex flex-wrap md:grid md:grid-cols-12 basis-full items-center px-4 md:px-6 md:px-8 mx-auto"
          aria-label="Global"
        >
          <div class="md:col-span-3">
            <!-- Logo -->
            <a
              class="flex-none rounded-xl text-xl inline-block font-semibold focus:outline-none focus:opacity-80"
              href="/"
              aria-label="Acmecloud"
            >
              <img
                class="h-8"
                src="https://bbs.acmecloud.cn/data/attachment/common/template/boardimg_20240115efehkfwk.png"
                alt="Acmecloud"
              />
            </a>
            <!-- End Logo -->
          </div>

          <!-- Button Group -->
          <div
            class="flex items-center gap-x-2 ms-auto py-1 md:ps-6 md:order-3 md:col-span-3"
          >
            <button
              type="button"
              onclick="window.location.href='/login'"
              class="py-2 px-3 inline-flex items-center gap-x-2 text-sm font-medium rounded-xl border border-gray-200 text-black hover:bg-gray-100 disabled:opacity-50 disabled:pointer-events-none dark:border-neutral-700 dark:hover:bg-white/10 dark:text-white dark:hover:text-white"
            >
              Sign in
            </button>
            <button
              type="button"
              onclick="window.location.href='/register'"
              class="py-2 px-3 inline-flex items-center gap-x-2 text-sm font-medium rounded-xl border border-transparent bg-lime-400 text-black hover:bg-lime-500 transition disabled:opacity-50 disabled:pointer-events-none focus:outline-none focus:bg-lime-500"
            >
              Sign up
            </button>

            <div class="hs-dropdown">
              <button
                type="button"
                class="hs-dropdown-toggle hs-dark-mode group flex items-center text-gray-600 hover:text-blue-600 font-medium dark:text-neutral-400 dark:hover:text-neutral-500"
              >
                <svg
                  class="hs-dark-mode-active:hidden block size-4"
                  xmlns="http://www.w3.org/2000/svg"
                  width="24"
                  height="24"
                  viewBox="0 0 24 24"
                  fill="none"
                  stroke="currentColor"
                  stroke-width="2"
                  stroke-linecap="round"
                  stroke-linejoin="round"
                >
                  <path d="M12 3a6 6 0 0 0 9 9 9 9 0 1 1-9-9Z"></path>
                </svg>
                <svg
                  class="hs-dark-mode-active:block hidden size-4"
                  xmlns="http://www.w3.org/2000/svg"
                  width="24"
                  height="24"
                  viewBox="0 0 24 24"
                  fill="none"
                  stroke="currentColor"
                  stroke-width="2"
                  stroke-linecap="round"
                  stroke-linejoin="round"
                >
                  <circle cx="12" cy="12" r="4"></circle>
                  <path d="M12 2v2"></path>
                  <path d="M12 20v2"></path>
                  <path d="m4.93 4.93 1.41 1.41"></path>
                  <path d="m17.66 17.66 1.41 1.41"></path>
                  <path d="M2 12h2"></path>
                  <path d="M20 12h2"></path>
                  <path d="m6.34 17.66-1.41 1.41"></path>
                  <path d="m19.07 4.93-1.41 1.41"></path>
                </svg>
              </button>

              <div
                id="selectThemeDropdown"
                class="hs-dropdown-menu hs-dropdown-open:opacity-100 mt-2 hidden z-10 transition-[margin,opacity] opacity-0 duration-300 mb-2 origin-bottom-left bg-white shadow-md rounded-lg p-2 space-y-1 dark:bg-neutral-800 dark:border dark:border-neutral-700 dark:divide-neutral-700"
              >
                <button
                  type="button"
                  @click="open = false"
                  class="w-full flex items-center gap-x-3.5 py-2 px-3 rounded-lg text-sm text-gray-800 hover:bg-gray-100 dark:text-neutral-400 dark:hover:bg-neutral-700 dark:hover:text-neutral-300"
                  data-hs-theme-click-value="default"
                >
                  Default (Light)
                </button>
                <button
                  type="button"
                  @click="open = false"
                  class="w-full flex items-center gap-x-3.5 py-2 px-3 rounded-lg text-sm text-gray-800 hover:bg-gray-100 dark:text-neutral-400 dark:hover:bg-neutral-700 dark:hover:text-neutral-300"
                  data-hs-theme-click-value="dark"
                >
                  Dark
                </button>
                <button
                  type="button"
                  @click="open = false"
                  class="w-full flex items-center gap-x-3.5 py-2 px-3 rounded-lg text-sm text-gray-800 hover:bg-gray-100 dark:text-neutral-400 dark:hover:bg-neutral-700 dark:hover:text-neutral-300"
                  data-hs-theme-click-value="auto"
                >
                  Auto (System)
                </button>
              </div>
            </div>

            <div class="md:hidden">
              <button
                type="button"
                class="hs-collapse-toggle size-[38px] flex justify-center items-center text-sm font-semibold rounded-xl border border-gray-200 text-black hover:bg-gray-100 disabled:opacity-50 disabled:pointer-events-none dark:text-white dark:border-neutral-700 dark:hover:bg-neutral-700"
                data-hs-collapse="#navbar-collapse-with-animation"
                aria-controls="navbar-collapse-with-animation"
                aria-label="Toggle navigation"
              >
                <svg
                  class="hs-collapse-open:hidden flex-shrink-0 size-4"
                  xmlns="http://www.w3.org/2000/svg"
                  width="24"
                  height="24"
                  viewBox="0 0 24 24"
                  fill="none"
                  stroke="currentColor"
                  stroke-width="2"
                  stroke-linecap="round"
                  stroke-linejoin="round"
                >
                  <line x1="3" x2="21" y1="6" y2="6" />
                  <line x1="3" x2="21" y1="12" y2="12" />
                  <line x1="3" x2="21" y1="18" y2="18" />
                </svg>
                <svg
                  class="hs-collapse-open:block hidden flex-shrink-0 size-4"
                  xmlns="http://www.w3.org/2000/svg"
                  width="24"
                  height="24"
                  viewBox="0 0 24 24"
                  fill="none"
                  stroke="currentColor"
                  stroke-width="2"
                  stroke-linecap="round"
                  stroke-linejoin="round"
                >
                  <path d="M18 6 6 18" />
                  <path d="m6 6 12 12" />
                </svg>
              </button>
            </div>
          </div>
          <!-- End Button Group -->

          <!-- Collapse -->
          <div
            id="navbar-collapse-with-animation"
            class="hs-collapse hidden overflow-hidden transition-all duration-300 basis-full grow md:block md:w-auto md:basis-auto md:order-2 md:col-span-6"
          >
            <div
              class="flex flex-col gap-y-4 gap-x-0 mt-5 md:flex-row md:justify-center md:items-center md:gap-y-0 md:gap-x-7 md:mt-0"
            >
              <div>
                <a
                  class="relative inline-block text-black before:absolute before:bottom-0.5 before:start-0 before:-z-[1] before:w-full before:h-1 before:bg-lime-400 dark:text-white"
                  href="/"
                  aria-current="page"
                  >首页</a
                >
              </div>
              <div>
                <a
                  class="inline-block text-black hover:text-gray-600 dark:text-white dark:hover:text-neutral-300"
                  href="/product"
                  >产品</a
                >
              </div>
              <div>
                <a
                  class="inline-block text-black hover:text-gray-600 dark:text-white dark:hover:text-neutral-300"
                  href="#"
                  >服务</a
                >
              </div>
              <div>
                <a
                  class="inline-block text-black hover:text-gray-600 dark:text-white dark:hover:text-neutral-300"
                  href="/contact"
                  >支持</a
                >
              </div>
              <div>
                <a
                  class="inline-block text-black hover:text-gray-600 dark:text-white dark:hover:text-neutral-300"
                  href="/about"
                  >关于</a
                >
              </div>
            </div>
          </div>
          <!-- End Collapse -->
        </nav>
      </header>
      <!-- Gradients -->
      <div aria-hidden="true" class="flex -z-[1] absolute -top-48 start-0">
        <div class="bg-purple-200 opacity-30 blur-3xl w-[1036px] h-[600px] dark:bg-purple-900 dark:opacity-20"></div>
        <div class="bg-gray-200 opacity-90 blur-3xl w-[577px] h-[300px] transform translate-y-32 dark:bg-neutral-800/60"></div>
      </div>
      <!-- End Gradients -->
  </template>