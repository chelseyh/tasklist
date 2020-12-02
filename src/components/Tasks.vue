<template>
    <div>
        
       <Tasklist v-for="task in tasklist" v-bind:key="task.id" v-bind:atask=task></Tasklist> 
    <!-- <p>Tasklist from tasks</p> -->
    </div>
</template>

<script>
import Tasklist from './Tasklist.vue'

export default {
    name: 'Tasks',
    props:['tasklist'],
    components: 
    {
        Tasklist
    }
}
</script>

