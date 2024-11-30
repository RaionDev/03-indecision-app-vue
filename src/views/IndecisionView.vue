<template>
  <div class="flex flex-col h-screen max-w-lg mx-auto bg-gray-100">
    <div class="flex items-center justify-between p-4 text-white bg-blue-500">
      <span>Mi esposa</span>
    </div>

    <ChatMessages :messages="messages"/>

    <MessageBox @send-message="onMessage"/>

  </div>
</template>

<script setup lang="ts">
import ChatMessages from '@/components/chat/ChatMessages.vue';
import MessageBox from '@/components/chat/MessageBox.vue';
import { useChat } from '@/composables/useChat';

const {messages, onMessage} = useChat();

</script>
