<template>
  <div
    class="top-0 left-0 h-screen w-screen bg-black z-[1111] bg-opacity-90 px-5 py-5 text-main-clr"
    :class="[active ? 'fixed' : 'hidden']"
  >
    <div class="h-full w-full bg-teal-700 rounded-xl p-3 relative">
      <Icon
        name="ic:outline-close"
        size="30"
        class="absolute top-5 right-5 cursor-pointer"
        @click="upDtate"
      />
      <!-- name -->
      <!-- <span>{{ data?.title }}</span> -->
    </div>
  </div>
</template>
<script setup>
const active = usePopUpActive();
const data = usePopUpData().value;
const upDtate = () => {
  console.log(data);
  active.value = !active.value;
};
</script>
