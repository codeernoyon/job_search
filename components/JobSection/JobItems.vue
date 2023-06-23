<template>
  <div
    class="border-[2px] border-main-clr p-3 md:p-5 rounded-md shadow-xl flex flex-col md:flex-row w-full gap-5 lg:gap-10 my-5"
  >
    <!-- title -->
    <div class="text-main-clr lg:w-[40%]">
      <h2 class="text-2xl font-[600]">Ks Devware</h2>
      <span>{{ itemData.title }}</span>
      <!-- description -->
      <p class="text-slate-200">
        {{ itemData.description }}
        <span class="text-main-clr cursor-pointer">...see more</span>
      </p>
    </div>
    <!-- job details  -->
    <!-- salary -->
    <div class="flex flex-col">
      <span class="text-2xl">Salary</span>
      <span class="text-slate-200">${{ itemData.salary }}</span>
    </div>
    <div class="flex flex-col">
      <span class="text-2xl">Age</span>
      <span class="text-slate-200">{{ itemData.age }}</span>
    </div>
    <!-- --====-- -->
    <div class="flex flex-col">
      <span class="text-2xl">Apply last date</span>
      <span class="text-slate-200">{{ itemData.lastDate }}</span>
    </div>
    <!-- apply button -->
    <div class="flex items-center justify-center">
      <UtilsButton
        title="Apply"
        Bclass=""
        class="p-3 md:px-10 md:py-2"
        v-on:btnClick="updatePopupActive"
      />
    </div>
  </div>
</template>
<script>
export default {
  props: ["itemData", "index"],
  setup(props) {
    const active = usePopUpActive();
    const pData = usePopUpData();
    const updatePopupActive = () => {
      pData.value = { ...props.itemData, index: props.index };
      active.value = !active.value;
    };
    return { updatePopupActive };
  },
};
</script>
