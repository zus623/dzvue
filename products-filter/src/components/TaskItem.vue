<template>
  <div class="task-card">
    <header>
      <div><b>{{ props.task.title }}</b></div>
    </header>

    <main>
      <div> Задание: {{ props.task.text }}. </div>
      <slot></slot>
    </main>

    <footer>
      <button type="button" @click="complete">Выполнить</button>
    </footer>
  </div>
</template>

<script setup lang="ts">
const props = defineProps<{
  task: { title: string; text: string };
}>();

function complete() {
  alert(`Вы выполнили задание ${props.task.title}`);
}
</script>

<style>
.task-card {
  display: flex;
  gap: 4px;
  flex-direction: column;
  border: 1px solid #ccc;
  padding: 12px;
  border-radius: 8px;
}
</style>