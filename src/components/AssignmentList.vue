<template>
    <section v-show="assignments.length">
        <h3>{{ title }}</h3>
        <ul>
            <li v-for="assignment in assignments" :key="assignment.id">
                <label>
                    {{ assignment.name }}
                    <input type="checkbox" v-model="assignment.complete">
                </label>
            </li>
        </ul>
    </section>
</template>
  <script>

export default {
    name:"AssignmentList",

    props : {
        assignments : Array,
        title : String
    }
  }
  </script>
  
  <!-- Add "scoped" attribute to limit CSS to this component only -->
  <style scoped>
    ul{
        list-style: none;
        border: 1px solid gray;
        padding: 5px;
        text-align: left;
    }

    ul li{
        border-bottom: 1px solid gray;
        padding: 7px;
    }

    ul li label{
        display: flex;
        justify-content: space-between;
        align-items: center;
        gap: 4px;
    }
  </style>