<template>
  <div class="flex flex-col h-screen max-w-lg mx-auto bg-gray-100">
    <div class="flex items-center justify-between p-4 text-white bg-blue-500">
      <span>Mi esposa</span>
    </div>

    <ChatMessages />

    <MessageBox />

  </div>
</template>

<script setup lang="ts">
import ChatMessages from '@/components/chat/ChatMessages.vue';
import MessageBox from '@/components/chat/MessageBox.vue';
import type { ChatMessage } from '@/interfaces/chat-message.interface';
import { ref } from 'vue';

const messages = ref<ChatMessage[]>([
  {
    id: new Date().getTime(),
    message: 'Hola mundo',
    itsMine: true
  },
  {
    id: new Date().getTime() + 1,
    message: 'Si',
    itsMine: false,
    image: "https://yesno.wtf/assets/no/26-34b31d1f0777f70c61488f67a36576a9.gif",
  }
]);

</script>
