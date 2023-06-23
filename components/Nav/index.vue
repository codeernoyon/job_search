<template>
  <nav class="bg-teal-700 py-4 px-2 md:px-5 fixed w-full shadow-md !z-[999]">
    <div class="container m-auto flex justify-between place-items-center rela\">
      <!-- logo -->
      <NuxtLink to="/" class="font-bold text-3xl text-main-clr">Job</NuxtLink>
      <!-- right side -->
      <div
        class="flex gap-5 justify-center flex-col-reverse lg:flex-row items-center absolute lg:relative h-screen lg:h-fit w-full lg:w-fit top-[100%] left-0 bg-teal-800 lg:bg-transparent transition-all duration-300"
        :class="[toggle_active ? 'left-0' : 'left-[-110%] lg:left-0']"
      >
        <!-- search -->
        <div
          class="rounded-full overflow-hidden border-[2px] border-main-clr bg-teal-200 flex justify-center h-[45px] w-auto"
        >
          <input
            type="text"
            class="w-[200px] md:w-[400px] text-teal-800 flex-1 px-5 transition-all duration-300"
            placeholder="Find Job Here"
            :class="[search_active ? 'block' : 'hidden']"
          />
          <!-- icon -->
          <div
            class="bg-teal-800 px-8 h-[100%] flex justify-center items-center cursor-pointer"
            @click="update_search_active(!search_active.value)"
          >
            <Icon name="prime:search" color="#f5deb3" size="1.5rem" />
          </div>
        </div>
        <div class="flex gap-5">
          <!-- login -->
          <div>
            <UtilsButton title="Login" class="py-[7px] lg:py-[5px] px-8" />
          </div>
          <!-- singup -->
          <div>
            <UtilsButton title="Singup" class="py-[7px] lg:py-[5px] px-8" />
          </div>
        </div>
      </div>
      <!-- toggle button -->
      <div
        class="h-auto flex flex-col gap-1 w-10 transition-all duration-300 cursor-pointer lg:hidden"
        @click="toggle"
      >
        <div
          class="h-1 rounded-full bg-main-clr relative transition-all duration-300"
          :class="[
            toggle_active ? 'w-[100%] rotate-[43deg] top-[11px]' : 'w-[60%]',
          ]"
        ></div>
        <div
          class="h-1 rounded-full bg-main-clr transition-all duration-300"
          :class="[toggle_active ? 'w-[0%]' : 'w-[100%]']"
        ></div>
        <div
          class="h-1 rounded-full bg-main-clr relative transition-all duration-300"
          :class="[
            toggle_active ? 'w-[100%] -rotate-[40deg] top-[-5px]' : 'w-[85%]',
          ]"
        ></div>
      </div>
    </div>
  </nav>
</template>
<script setup>
const toggle_active = useState(() => false);
const search_active = useState(() => false);
// nav toggle
const toggle = () => {
  toggle_active.value = !toggle_active.value;
};
// search
const update_search_active = () => {
  search_active.value = !search_active.value;
};
</script>
