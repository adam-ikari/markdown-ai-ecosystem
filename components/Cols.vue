<template>
    <div class="grid gap-4" :class="gridClass">
        <slot />
    </div>
</template>

<script setup>
import { computed } from 'vue'

const props = defineProps({
    columns: {
        type: Number,
        default: 1
    }
})

// 使用对象映射替代 switch case 语句，但仍然保持静态类名以符合 TailwindCSS 规范
const columnClassMap = {
    1: 'grid-cols-1',
    2: 'grid-cols-2',
    3: 'grid-cols-3',
    4: 'grid-cols-4',
    5: 'grid-cols-5',
    6: 'grid-cols-6',
    7: 'grid-cols-7',
    8: 'grid-cols-8',
    9: 'grid-cols-9',
    10: 'grid-cols-10',
    11: 'grid-cols-11',
    12: 'grid-cols-12'
}

const gridClass = computed(() => {
    return columnClassMap[props.columns] || 'grid-cols-1'
})
</script>

<style scoped>
.cols-container {
    width: 100%;
}
</style>