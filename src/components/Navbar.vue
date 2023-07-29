<style scoped>
  .nama{
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
  
</style>



<script>
export default {
  props: {
    sidebarVisible: Boolean, // Receive sidebar visibility as a prop
  },
  setup() {
    const sidebarVisible = ref(false);
    const screenWidth = ref(window.innerWidth);

    // Computed property to check if the screen is small (below 768px)
    const isSmallScreen = computed(() => screenWidth.value < 768);

    // Update the screenWidth when the window is resized
    const updateScreenWidth = () => {
      screenWidth.value = window.innerWidth;
    };

    // Add event listener for window resize
    onMounted(() => {
      window.addEventListener('resize', updateScreenWidth);
    });

    // Remove event listener on component unmount
    onUnmounted(() => {
      window.removeEventListener('resize', updateScreenWidth);
    });

    function toggleSidebar() {
      sidebarVisible.value = !sidebarVisible.value;
    };

    return {
      sidebarVisible,
      isSmallScreen,
      toggleSidebar,
    };
  },
};
import { ref, computed, onMounted, onUnmounted } from 'vue';


</script>

<template>
  
  <div>
    <button
      data-drawer-target="default-sidebar"
      data-drawer-toggle="default-sidebar"
      aria-controls="default-sidebar"
      type="button"
      class="inline-flex items-center p-2 mt-2 ml-3 text-sm text-gray-500 rounded-lg sm:hidden hover:bg-gray-100 focus:outline-none focus:ring-2 focus:ring-gray-200 dark:text-gray-400 dark:hover:bg-gray-700 dark:focus:ring-gray-600"
      @click="toggleSidebar"
    >
      <span class="sr-only">Open sidebar</span>
      <svg class="w-6 h-6" aria-hidden="true" fill="currentColor" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg">
        <path
          clip-rule="evenodd"
          fill-rule="evenodd"
          d="M2 4.75A.75.75 0 012.75 4h14.5a.75.75 0 010 1.5H2.75A.75.75 0 012 4.75zm0 10.5a.75.75 0 01.75-.75h7.5a.75.75 0 010 1.5h-7.5a.75.75 0 01-.75-.75zM2 10a.75.75 0 01.75-.75h14.5a.75.75 0 010 1.5H2.75A.75.75 0 012 10z"
        ></path>
      </svg>
    </button>

    <aside
      id="default-sidebar"
      class="bg fixed top-0 left-0 z-40 w-64 h-screen transition-transform -translate-x-full sm:translate-x-0"
      aria-label="Sidebar"
    >
      <div class="h-full px-3 py-4 overflow-y-auto bg-gray-50 dark:bg-gray-800">
        <ul class="space-y-2 font-medium">
          <li>
            <a
              href="#"
              class="flex items-center p-2 text-gray-900 rounded-lg dark:text-white hover:bg-gray-100 dark:hover:bg-gray-700 group"
            >
              <span class="ml-3">
                <p class="nama text-4xl text-gray-900 dark:text-white">M. ATHHAR MALIKA P.</p>
                <br />
                <p class="text-xs text-gray-500 dark:text-white">Software engineering student + <br> Gundam addict</p>
              </span>
            </a>
          </li>
          <li>
            <a
              href="#"
              class="flex items-center p-2 text-gray-900 rounded-lg dark:text-white hover:bg-gray-100 dark:hover:bg-gray-700 group"
            >
              <svg
                class="flex-shrink-0 w-5 h-5 text-gray-500 transition duration-75 dark:text-gray-400 group-hover:text-gray-900 dark:group-hover:text-white"
                aria-hidden="true"
                xmlns="http://www.w3.org/2000/svg"
                fill="currentColor"
                viewBox="0 0 18 18"
              >
              </svg>
              <span class="flex-1 ml-3 whitespace-nowrap">Portofolio</span>
            </a>
          </li>
          <li>
           <About/>
            <a
              href="#"
              class="flex items-center p-2 text-gray-900 rounded-lg dark:text-white hover:bg-gray-100 dark:hover:bg-gray-700 group"
            >
              
              <span class="flex-1 ml-8 whitespace-nowrap">About</span>
            </a>
          </li>
          <li>
            <a
              href="#"
              class="flex items-center p-2 text-gray-900 rounded-lg dark:text-white hover:bg-gray-100 dark:hover:bg-gray-700 group"
            >
              <svg
                class="flex-shrink-0 w-5 h-5 text-gray-500 transition duration-75 dark:text-gray-400 group-hover:text-gray-900 dark:group-hover:text-white"
                aria-hidden="true"
                xmlns=""
                fill="currentColor"
                viewBox="0 0 18 20"
              >
                
              </svg>
              <span class="flex-1 ml-3 whitespace-nowrap">Contact</span>
            </a>
          </li>
        </ul>
        <br /><br /><br /><br /><br /><br /><br /><br /><br /><br /><br><br>
        <hr class="my-6 border-gray-200 sm:mx-auto dark:border-gray-700 lg:my-8" />
        <span class="block text-xs text-gray-500 sm:text-center dark:text-gray-400"
          >© Copyright All Rights Reserved.</span
        >
      </div>
    </aside>
  </div>
</template>
