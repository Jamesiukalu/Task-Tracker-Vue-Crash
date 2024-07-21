<template>
    <header>
        <h1>{{title}}</h1>
        <ButtonItem v-show="homepage" @btn-click="$emit('toggle-add-task')" 
        :text="showAddTask ? 'Close' : 'Add Task' "
        :color="showAddTask ? 'red' : 'green' " />
    </header>
</template>

<script>
import ButtonItem from './Button'
export default {
    name: 'HeaderItem',
    props: {
        title: String,
        showAddTask:Boolean
    },
    components: {
        ButtonItem,
    },
    computed: {
        homepage() {
            if (this .$route.path === '/') {
                return true
            } else {
                return false
            }
        }
    }

}
</script>

<style>
    header {
        display: flex;
        justify-content: space-between;
        align-items: center;
        margin-bottom: 20px;
    }
</style>