<template>
    <assignment-list :assignments="inProgress" title="In Progress"/>
    <assignment-list :assignments="inComplete" title="In Complete"/>

    <assignment-create v-model:newAssignment="newAssignment" :assignments="assignments" :add="add"></assignment-create>
    <!-- <form @submit.prevent="add">
        <input v-model="newAssignment" type="text" placeholder="New Assignment..."/>
        <button type="submit">Add</button>
    </form> -->
</template>

  <script>

  import AssignmentList from './AssignmentList.vue';
  import AssignmentCreate from './AssignmentCreate.vue';
  export default {
    name: "AssignmentsVue",
    components: {
        AssignmentList,
        AssignmentCreate
    },
    data(){
        return {
            assignments :[
                {name: "Ye Myat Hein", complete : false, id: 1},
                {name: "Htet Shine", complete : false, id: 2},
                {name: "Htain Lin Aung", complete : false, id: 3}
            ],
            newAssignment : ''
        }
    },
    computed:{
        inProgress(){
            return this.assignments.filter(assignment=> !assignment.complete)
        },
        inComplete(){
            return this.assignments.filter(assignment=> assignment.complete)
        }
    },

    methods: {
        add(){
            this.assignments.push({
                name: this.newAssignment,
                complete : false,
                id : this.assignments.length+ 1
            })

            this.newAssignment = ""
        }
    }

  }
  </script>
  
  <!-- Add "scoped" attribute to limit CSS to this component only -->
  <style scoped>
    form input, form button{
        padding: 5px;
    }
  </style>