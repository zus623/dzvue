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
  { _id: "1", title: "Проснуться", text: "Почистить зубы" },
  { _id: "2", title: "Собраться", text: "Поехать в колледж" },
  { _id: "3", title: "Вечером", text: "Поехать на тренировку" },
  { _id: "4", title: "Перед сном", text: "Сходить в душ" },
];

</script>

<style>
body{
  background-color: #b9f3dd;
  color: black;
}

.products {
  display: flex;
  gap: 16px;
  flex-direction: column;
}
</style>