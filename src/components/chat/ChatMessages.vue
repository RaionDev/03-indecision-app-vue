<template>
  <div class="flex-1 p-4 overflow-y-auto">
    <div class="flex flex-col space-y-2">
      <ChatBubble
        v-for="message in messages"
        :key="message.id"
        v-bind="message"
        />
        <!-- :its-mine="message.itsMine"
        :message="message.message"
        :image="message.image" -->
    </div>
  </div>
</template>

<script setup lang="ts">
import type { ChatMessage } from '@/interfaces/chat-message.interface';
import ChatBubble from './ChatBubble.vue';

interface Props {
  messages: ChatMessage[]
}

defineProps<Props>();
</script>
