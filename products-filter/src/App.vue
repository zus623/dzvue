<template>
  <div>
    <h1>Список заданий</h1>
    <div class="products">
      <TaskItem 
        v-for="task in tasks" 
        :key="task._id"  
        :task="task"
       >
      </TaskItem>
    </div>

  </div>
</template>


<script setup lang="ts">
import { ref, computed } from "vue";
import TaskItem from "./components/TaskItem.vue";

const tasks = [
  { _id: "1", title: "Завтрак", text: "Приготовить завтрак и поесть" },
  { _id: "2", title: "Прогулка", text: "После пар пройтись погулять" },
  { _id: "3", title: "Сделать дз", text: "Вечером выполнить дз" },
  { _id: "4", title: "Ужин", text: "Приготовить ужин и поесть" },
];

</script>

<style>
.products {
  display: flex;
  gap: 16px;
  flex-direction: column;
}
</style>