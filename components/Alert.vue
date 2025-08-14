<template>
  <div
    class="alert-container my-4 p-4 rounded border-l-4"
    :class="[currentType.bg, currentType.border]"
  >
    <div class="flex items-start">
      <span v-if="icon" class="text-xl mr-2" :class="currentType.text">{{
        currentType.icon
      }}</span>
      <div class="flex-1">
        <h4 v-if="title" class="font-bold mb-1" :class="currentType.text">
          {{ title }}
        </h4>
        <p v-if="content" :class="currentType.text">{{ content }}</p>
        <div v-if="$slots.default" :class="currentType.text">
          <slot />
        </div>
      </div>
    </div>
  </div>
</template>
<script setup lang="ts">
import { computed } from "vue";
interface Props {
  type?: "success" | "warning" | "error" | "info";
  title?: string;
  content?: string;
  icon?: boolean;
}

const props = withDefaults(defineProps<Props>(), {
  type: "info",
  title: "",
  content: "",
  icon: false
});

const typeMap = {
  success: {
    icon: "✅",
    bg: "bg-green-100",
    border: "border-green-500",
    text: "text-green-800",
  },
  warning: {
    icon: "⚠️",
    bg: "bg-yellow-100",
    border: "border-yellow-500",
    text: "text-yellow-800",
  },
  error: {
    icon: "❌",
    bg: "bg-red-100",
    border: "border-red-500",
    text: "text-red-800",
  },
  info: {
    icon: "ℹ️",
    bg: "bg-blue-100",
    border: "border-blue-500",
    text: "text-blue-800",
  },
};

const currentType = computed(() => typeMap[props.type]);
</script>
<style scoped>
.alert-container {
  box-shadow:
    0 1px 3px rgba(0, 0, 0, 0.12),
    0 1px 2px rgba(0, 0, 0, 0.24);
  transition: all 0.3s cubic-bezier(0.25, 0.8, 0.25, 1);
}

.alert-container:hover {
  box-shadow:
    0 4px 8px rgba(0, 0, 0, 0.15),
    0 4px 8px rgba(0, 0, 0, 0.2);
}
</style>
