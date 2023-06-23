<template>
  <div :class="Bclass">
    <button
      class="border-[2px] text-main-clr border-main-clr rounded-md shadow-xl font-semibold w-[100%]"
      @click="$emit('btnClick')"
      :class="class"
    >
      {{ title }}
    </button>
  </div>
</template>
<script>
export default {
  props: ["title", "class", "Bclass"],
};
</script>
