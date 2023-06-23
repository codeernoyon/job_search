<template>
  <div
    class="w-full h-screen md:py-20 flex md:flex-col-reverse lg:flex-row items-center justify-center md:justify-normal container m-auto px-2 md:px-5"
  >
    <!-- image -->
    <div class="lg:w-2/4 md:h-3/4 lg:h-full md:py-5 hidden md:block">
      <img src="@/assets/hero/job.svg" alt="image" class="h-full w-full" />
    </div>
    <!-- SEARCH ber -->
    <div class="lg:pl-14">
      <!-- content -->
      <h2
        class="text-main-clr font-semibold text-3xl lg:text-6xl text-center md:text-left"
      >
        Search Your Dream <br class="hidden lg:block" />
        Jobs
      </h2>
      <div
        class="rounded-full overflow-hidden border-[2px] border-main-clr bg-teal-700 flex justify-center h-[60px] mt-5 lg:mt-10"
      >
        <input
          type="text"
          class="w-[270px] md:w-[400px] text-main-clr flex-1 px-5"
          placeholder="Find Job Here"
        />
        <!-- icon -->
        <div
          class="bg-teal-800 px-8 h-[100%] flex justify-center items-center cursor-pointer"
        >
          <Icon name="prime:search" color="#f5deb3" size="1.5rem" />
        </div>
      </div>
    </div>
  </div>
</template>
<script setup></script>
