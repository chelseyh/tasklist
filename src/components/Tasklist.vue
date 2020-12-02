<template>
    <div class="todoitem">
        <!-- <p>A Single Task</p> -->
        <div v-bind:class="{'is-completed':atask.completed}">
            {{atask.title}}
        </div>
    </div>
</template>

<script>
export default {
    name:'Tasklist',
    props: ['atask']
}
</script>

<style scoped>
    .todoitem
    {
        background: #f4f4f4;
        padding: 10px;
        border-bottom: 3px #cccc dotted;
    }

    .is-completed
    {
        text-decoration: line-through;
    }
</style>