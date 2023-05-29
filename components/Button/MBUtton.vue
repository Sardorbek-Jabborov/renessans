<template>
  <div>
    <button
      :title="title"
      :icon="icon"
      class="bg-[#DBCCa9] flex items-center py-2 px-5 font-normal text-xs leading-140 text-[#021117] ease-all duration-300 hover:cursor-pointer hover:bg-[#DCBC71]"
    >
      {{ title }}
      <img :src="icon" alt="" class="ml-2" />
    </button>
  </div>
</template>

<script setup lang="ts">
interface Props {
  title?: String
  icon?: String
}

defineProps<Props>()
</script>
