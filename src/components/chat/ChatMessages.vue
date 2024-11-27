<template>
  <div class="flex-1 p-4 overflow-y-auto">
    <div class="flex flex-col space-y-2">
      <ChatBubble :its-mine="true" :message="'Hola Mundo'" />
      <ChatBubble :its-mine="false" :message="'no'"
        image="https://yesno.wtf/assets/no/26-34b31d1f0777f70c61488f67a36576a9.gif" />
    </div>
  </div>
</template>

<script setup lang="ts">
import ChatBubble from './ChatBubble.vue';
</script>
