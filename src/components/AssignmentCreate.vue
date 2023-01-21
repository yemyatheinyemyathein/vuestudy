<template>
    <form @submit.prevent="add">
        <input v-model="newAssignment" type="text" placeholder="New Assignment..."/>
        <button type="submit">Add</button>
    </form>
</template>


<script type="module">

export default {
    name: "AssignmentCreate",
    props: {
        assignments: Array,
        add: {},
        newAssignment: {}
    },
    data(){
        return {
            
        }
    },
}

</script>


<style>
    form input, form button{
        padding: 5px;
    }
</style>