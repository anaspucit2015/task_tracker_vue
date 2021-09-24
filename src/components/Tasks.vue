<template>
    <div :key="task.id" v-for="task in tasks">
       <Task @toggle-reminder="$emit('toggle-reminder',task.id)" @task-delete="$emit('task-delete',task.id)" :task="task"/>
    </div>
</template>
<script>

import Task from './task.vue'

export default ({
   name:"Tasks",
   props:{
       tasks: Array,
   },
   components:{
       Task,
   },
   emits:['task-delete','toggle-reminder']
   
})
</script>
