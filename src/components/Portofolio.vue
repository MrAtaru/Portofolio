<script setup>
import Navbar from "./Navbar.vue";
</script>

<script>
export default {
  data() {
    return {
      items: [
        '/project1.jpg',
        '/project2.jpg',
        '/project3.jpg',
        '/project4.jpg',
      ],
      currentIndex: 0,
    };
  },
  methods: {
    prev() {
      this.currentIndex = (this.currentIndex - 1 + this.items.length) % this.items.length;
    },
    next() {
      this.currentIndex = (this.currentIndex + 1) % this.items.length;
    },
    startAutoPlay() {
      this.timer = setInterval(() => {
        this.next();
      }, 6000); // Change slide every 3 seconds (adjust as needed)
    },
    stopAutoPlay() {
      clearInterval(this.timer);
    },
  },
  mounted() {
    this.startAutoPlay();
  },
  beforeDestroy() {
    this.stopAutoPlay();
  },
};
</script>

<template>
  <div>
    <Navbar />
  </div>
  <div>
    <section
      class="bg-white dark:bg-gray-900 bg-[url('https://flowbite.s3.amazonaws.com/docs/jumbotron/hero-pattern.svg')] dark:bg-[url('https://flowbite.s3.amazonaws.com/docs/jumbotron/hero-pattern-dark.svg')]"
    >
      <div class="py-8 px-4 mx-auto max-w-screen-xl lg:py-16 z-10 relative">
        <div class="foto grid grid-cols-2 md:grid-cols-1 gap-10">
          <div class="grid gap-3">
            <div class="py-8 px-4 mx-auto max-w-screen-xl lg:py-16 z-10 relative">
              <h1
                class="text-center mb-4 text-4xl font-extrabold tracking-tight leading-none text-gray-900 md:text-5xl lg:text-6xl dark:text-white"
              >
                Wilujeung Sumping!
              </h1>
            </div>
            <br /><br />
          </div>
        </div>
        <div class="grid grid-cols-2 md:grid-cols-1 gap-10">
          <div class="grid gap-3">
            <div>
              <h1 class="foto text-center mb-4 text-2xl tracking-tight leading-none text-gray-900 dark:text-white">Foto Gallery</h1>
            </div>
            <br />
          </div>
        </div>

        <div class="foto grid grid-cols-2 md:grid-cols-3 gap-10">
          <div class="grid gap-3">
            <div>
              <img class="h-auto max-w-xs mx-auto rounded-lg" src="/aerial4.jpg" alt="" />
            </div>
            <div>
              <img class="h-auto max-w-xs mx-auto rounded-lg" src="/rx-78-02_2.jpg" alt="" />
            </div>
            <div>
              <img class="h-auto max-w-xs mx-auto rounded-lg" src="/aerial1.jpg" alt="" />
            </div>
          </div>
          <div class="grid gap-3">
            <div>
              <img class="h-auto max-w-xs mx-auto rounded-lg" src="/rx-78-02.jpg" alt="" />
            </div>
            <div>
              <img class="h-auto max-w-xs mx-auto rounded-lg" src="/redAstray3.jpg" alt="" />
            </div>
            <div>
              <img class="h-auto max-w-xs mx-auto rounded-lg" src="/rx-78-02.jpg" alt="" />
            </div>
          </div>
          <div class="grid gap-3">
            <div>
              <img class="h-auto max-w-xs mx-auto rounded-lg" src="/aerial3.jpg" alt="" />
            </div>
            <div>
              <img class="h-auto max-w-xs mx-auto rounded-lg" src="/rx-78-02_2.jpg" alt="" />
            </div>
            <div>
              <img class="h-auto max-w-xs mx-auto rounded-lg" src="/aerial4.jpg" alt="" />
            </div>
          </div>
        </div>

        <div class="foto grid grid-cols-2 md:grid-cols-1 gap-10">
          <div class="grid gap-3">
            <div>
              <hr class="h-px my-8 bg-gray-200 border-2 rounded-lg dark:bg-gray-700" />
            </div>
          </div>
        </div>
        <br /><br />
        <div class="foto grid grid-cols-2 md:grid-cols-1 gap-10">
          <div class="grid gap-3">
            <div>
              <h1 class="text-center mb-4 text-2xl tracking-tight leading-none text-gray-900 dark:text-white">
                Riwayat Pendidikan
              </h1>
            </div>
            <div>
              <ol class="items-center sm:flex">
                <li class="relative mb-6 sm:mb-0">
                  <div class="flex items-center">
                    <div
                      class="z-10 flex items-center justify-center w-6 h-6 bg-blue-100 rounded-full ring-0 ring-white dark:bg-blue-900 sm:ring-8 dark:ring-gray-900 shrink-0"
                    >
                      <svg
                        class="w-2.5 h-2.5 text-blue-800 dark:text-blue-300"
                        aria-hidden="true"
                        xmlns="http://www.w3.org/2000/svg"
                        fill="currentColor"
                        viewBox="0 0 20 20"
                      >
                        <path
                          d="M20 4a2 2 0 0 0-2-2h-2V1a1 1 0 0 0-2 0v1h-3V1a1 1 0 0 0-2 0v1H6V1a1 1 0 0 0-2 0v1H2a2 2 0 0 0-2 2v2h20V4ZM0 18a2 2 0 0 0 2 2h16a2 2 0 0 0 2-2V8H0v10Zm5-8h10a1 1 0 0 1 0 2H5a1 1 0 0 1 0-2Z"
                        />
                      </svg>
                    </div>
                    <div class="hidden sm:flex w-full bg-gray-200 h-0.5 dark:bg-gray-700"></div>
                  </div>
                  <div class="mt-3 sm:pr-8">
                    <h3 class="text-lg font-semibold text-gray-900 dark:text-white">SD Islam Al-Mumtaaz</h3>
                    <time class="block mb-2 text-sm font-normal leading-none text-gray-400 dark:text-gray-500 hidden"
                      >Released on December 2, 2021</time
                    >
                    <p class="text-base font-normal text-gray-500 dark:text-gray-400">
                      Kampung Bobojong, Ds.Purwadana, kec.Teluk Jambe Timur, Karawang barat
                    </p>
                  </div>
                </li>
                <li class="relative mb-6 sm:mb-0">
                  <div class="flex items-center">
                    <div
                      class="z-10 flex items-center justify-center w-6 h-6 bg-blue-100 rounded-full ring-0 ring-white dark:bg-blue-900 sm:ring-8 dark:ring-gray-900 shrink-0"
                    >
                      <svg
                        class="w-2.5 h-2.5 text-blue-800 dark:text-blue-300"
                        aria-hidden="true"
                        xmlns="http://www.w3.org/2000/svg"
                        fill="currentColor"
                        viewBox="0 0 20 20"
                      >
                        <path
                          d="M20 4a2 2 0 0 0-2-2h-2V1a1 1 0 0 0-2 0v1h-3V1a1 1 0 0 0-2 0v1H6V1a1 1 0 0 0-2 0v1H2a2 2 0 0 0-2 2v2h20V4ZM0 18a2 2 0 0 0 2 2h16a2 2 0 0 0 2-2V8H0v10Zm5-8h10a1 1 0 0 1 0 2H5a1 1 0 0 1 0-2Z"
                        />
                      </svg>
                    </div>
                    <div class="hidden sm:flex w-full bg-gray-200 h-0.5 dark:bg-gray-700"></div>
                  </div>
                  <div class="mt-3 sm:pr-8">
                    <h3 class="text-lg font-semibold text-gray-900 dark:text-white">SMP Islam Al-Mumtaaz</h3>
                    <time class="block mb-2 text-sm font-normal leading-none text-gray-400 dark:text-gray-500 hidden"
                      >Released on December 23, 2021</time
                    >
                    <p class="text-base font-normal text-gray-500 dark:text-gray-400">
                      Kampung Bobojong, Ds.Purwadana, kec.Teluk Jambe Timur, Karawang barat
                    </p>
                  </div>
                </li>
                <li class="relative mb-6 sm:mb-0">
                  <div class="flex items-center">
                    <div
                      class="z-10 flex items-center justify-center w-6 h-6 bg-blue-100 rounded-full ring-0 ring-white dark:bg-blue-900 sm:ring-8 dark:ring-gray-900 shrink-0"
                    >
                      <svg
                        class="w-2.5 h-2.5 text-blue-800 dark:text-blue-300"
                        aria-hidden="true"
                        xmlns="http://www.w3.org/2000/svg"
                        fill="currentColor"
                        viewBox="0 0 20 20"
                      >
                        <path
                          d="M20 4a2 2 0 0 0-2-2h-2V1a1 1 0 0 0-2 0v1h-3V1a1 1 0 0 0-2 0v1H6V1a1 1 0 0 0-2 0v1H2a2 2 0 0 0-2 2v2h20V4ZM0 18a2 2 0 0 0 2 2h16a2 2 0 0 0 2-2V8H0v10Zm5-8h10a1 1 0 0 1 0 2H5a1 1 0 0 1 0-2Z"
                        />
                      </svg>
                    </div>
                    <div class="hidden sm:flex w-full bg-gray-200 h-0.5 dark:bg-gray-700"></div>
                  </div>
                  <div class="mt-3 sm:pr-8">
                    <h3 class="text-lg font-semibold text-gray-900 dark:text-white">SMK Assalaam Bandung</h3>
                    <time class="block mb-2 text-sm font-normal leading-none text-gray-400 dark:text-gray-500 hidden"
                      >Pada tanggal January 5, 2022</time
                    >
                    <p class="text-base font-normal text-gray-500 dark:text-gray-400">
                      Jl. Situ Tarate, Cibaduyut, Dayeuhkolot, Kab. Bandung
                    </p>
                  </div>
                </li>
              </ol>
            </div>
          </div>
        </div>
        <div class="foto grid grid-cols-2 md:grid-cols-1 gap-10">
          <div class="grid gap-3">
            <div>
              <hr class="h-px my-8 bg-gray-200 border-2 rounded-lg dark:bg-gray-700" />
            </div>
          </div>
        </div>

        <br /><br />

        <div class="foto grid grid-cols-2 md:grid-cols-1 gap-10">
          <div class="grid gap-3">
            <div>
              <h1 class="text-center mb-4 text-2xl tracking-tight leading-none text-gray-900 dark:text-white">Kemampuan</h1>
            </div>

            <!-- Kemampuan 1 -->
            <div>
              <div class="flex justify-between mb-1">
                <span class="text-base font-medium text-blue-700 dark:text-white">HTML</span>
                <span class="text-sm font-medium text-blue-700 dark:text-white">50%</span>
              </div>
              <div class="w-full bg-gray-200 rounded-full h-2.5 dark:bg-gray-700">
                <div class="bg-gray-600 h-2.5 rounded-full" style="width: 50%"></div>
              </div>
            </div>
            <br />
            <!-- Kemampuan 2 -->
            <div>
              <div class="flex justify-between mb-1">
                <span class="text-base font-medium text-blue-700 dark:text-white">CSS</span>
                <span class="text-sm font-medium text-blue-700 dark:text-white">50%</span>
              </div>
              <div class="w-full bg-gray-200 rounded-full h-2.5 dark:bg-gray-700">
                <div class="bg-blue-600 h-2.5 rounded-full" style="width: 50%"></div>
              </div>
            </div>
            <br />
            <!-- Kemampuan 1 -->
            <div>
              <div class="flex justify-between mb-1">
                <span class="text-base font-medium text-blue-700 dark:text-white">Express</span>
                <span class="text-sm font-medium text-blue-700 dark:text-white">50%</span>
              </div>
              <div class="w-full bg-gray-200 rounded-full h-2.5 dark:bg-gray-700">
                <div class="bg-green-400 h-2.5 rounded-full" style="width: 50%"></div>
              </div>
            </div>
            <br />
            <!-- Kemampuan 1 -->
            <div>
              <div class="flex justify-between mb-1">
                <span class="text-base font-medium text-blue-700 dark:text-white">Nodejs</span>
                <span class="text-sm font-medium text-blue-700 dark:text-white">50%</span>
              </div>
              <div class="w-full bg-gray-200 rounded-full h-2.5 dark:bg-gray-700">
                <div class="bg-yellow-300 h-2.5 rounded-full" style="width: 50%"></div>
              </div>
            </div>
            <br />
            <!-- Kemampuan 1 -->
            <div>
              <div class="flex justify-between mb-1">
                <span class="text-base font-medium text-blue-700 dark:text-white">JavaScript</span>
                <span class="text-sm font-medium text-blue-700 dark:text-white">50%</span>
              </div>
              <div class="w-full bg-gray-200 rounded-full h-2.5 dark:bg-gray-700">
                <div class="bg-purple-600 h-2.5 rounded-full" style="width: 50%"></div>
              </div>
            </div>
            <br />
            <!-- Kemampuan 1 -->
            <div>
              <div class="flex justify-between mb-1">
                <span class="text-base font-medium text-blue-700 dark:text-white">PHP</span>
                <span class="text-sm font-medium text-blue-700 dark:text-white">50%</span>
              </div>
              <div class="w-full bg-gray-200 rounded-full h-2.5 dark:bg-gray-700">
                <div class="bg-green-600 h-2.5 rounded-full" style="width: 50%"></div>
              </div>
            </div>
            <br />
            <!-- Kemampuan 1 -->
            <div>
              <div class="flex justify-between mb-1">
                <span class="text-base font-medium text-blue-700 dark:text-white">Mysql</span>
                <span class="text-sm font-medium text-blue-700 dark:text-white">50%</span>
              </div>
              <div class="w-full bg-gray-200 rounded-full h-2.5 dark:bg-gray-700">
                <div class="bg-red-700 h-2.5 rounded-full" style="width: 50%"></div>
              </div>
            </div>
            <br />
            <!-- Kemampuan 1 -->
            <div>
              <div class="flex justify-between mb-1">
                <span class="text-base font-medium text-blue-700 dark:text-white">Tailwindcss</span>
                <span class="text-sm font-medium text-blue-700 dark:text-white">50%</span>
              </div>
              <div class="w-full bg-gray-200 rounded-full h-2.5 dark:bg-gray-700">
                <div class="bg-pink-400 h-2.5 rounded-full" style="width: 50%"></div>
              </div>
            </div>
          </div>
        </div>
        <br /><br />
        <div class="foto grid grid-cols-2 md:grid-cols-1 gap-10">
          <div class="grid gap-3">
            <div>
              <h1 class="text-center mb-4 text-2xl tracking-tight leading-none text-gray-900 dark:text-white">Project</h1>
            </div>

            <div class="carousel">
              
              <div class="carousel-wrapper">
                <div
                  v-for="(item, index) in items"
                  :key="index"
                  :class="['carousel-item', { hidden: currentIndex !== index, block: currentIndex === index }]"
                >
                  <img :src="item" alt="" class="w-full" />
                </div>
              </div>
              <div class="carousel-controls">
                <button @click="prev" class="carousel-control-btn prev-btn">&lt</button>
                <button @click="next" class="carousel-control-btn next-btn">></button>
              </div>
            </div>

          </div>
        </div>
      </div>
      <div class="bg-gradient-to-b from-blue-50 to-transparent dark:from-blue-900 w-full h-full absolute top-0 left-0 z-0"></div>
    </section>
  </div>
</template>

<style scoped>

.carousel-control-btn {
  cursor: pointer;
  border: none;
  color: white;
  padding: 0.5rem 1rem;
  border-radius: 0.25rem;
  font-size: 1rem;
}

.prev-btn {
  background-color: #ff5722; /* Orange background color for previous button */
}

.next-btn {
  background-color: #3f51b5; /* Indigo background color for next button */
}

.carousel-control-btn:hover {
  opacity: 0.8; /* Reduce opacity on hover for both buttons */
}

.carousel-control-btn:focus {
  outline: none;
  box-shadow: 0 0 0 3px rgba(63, 81, 181, 0.4); /* Add an indigo border on focus for next button */
}
.nama {
  font-family: "Poppins Bold", sans-serif;
  font-size: 30px;
  font-weight: bold;
  color: #000000;
  text-decoration: none;
  display: inline-block;
  margin-bottom: 0px;
  max-width: 100%;
  display: block;
}
.foto {
  width: auto;
  height: 100%;
  margin-left: 20%;
}
.carousel {
  max-width: 500px;
  margin: 0 auto;
}

.carousel-wrapper {
  display: flex;
  overflow: hidden;
}

.carousel-controls {
  display: flex;
  justify-content: space-between;
  margin-top: 0.5rem;
}

.carousel-control-btn {
  cursor: pointer;
  border: none;
  background-color: #333;
  color: #fff;
  padding: 0.5rem 1rem;
  border-radius: 0.25rem;
}
</style>
