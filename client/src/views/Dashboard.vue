<template>
    <div style="background-color: #f7f2e7; height: 100vh;">
        
        <Navbar 
            @changePage="changePage">
            </Navbar>

        <Kanban 
            @changePage="changePage">
            </Kanban>

    </div>
</template>

<script>

import Kanban from './Kanban'
import Navbar from './Navbar'
export default {
    name: 'Dashboard',
    data() {
        return {
            activity: 'kanban',
        }
    },
    components: {
        Kanban,
        Navbar
    },
    methods: {
        changePage(status){
           localStorage.clear()
           this.$emit('changePage', status)
        },

    }

}
</script>

<style>

</style>