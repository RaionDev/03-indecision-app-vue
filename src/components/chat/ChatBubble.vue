<template>
  <!-- Example Message -->
  <div v-if="itsMine" class="flex justify-end">
    <div class="max-w-xs p-2 text-black bg-blue-200 rounded-lg">
      {{ message }}
    </div>
  </div>

  <!-- Example Received Message -->
  <div v-else class="flex">
    <div class="max-w-xs p-2 text-black bg-gray-300 rounded-lg">
      <span class="capitalize">{{ message }}</span>
      <img v-if="image" :src="image" alt="YesNoImage" class="object-cover rounded-md w-52 h-52" />
    </div>
  </div>

</template>

<script setup lang="ts">
interface Props {
  message: string;
  itsMine: boolean;
  image?: string;
}

defineProps<Props>();
</script>
