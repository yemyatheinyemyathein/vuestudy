<template>
    <button :class="active?'text-red':'text-green'" @click="toggle">Click Me</button>
  </template>
  
  <script>
  export default {
    name: 'ButtonClick',
    data(){
        return{
            buttonClasses: "text-red",
            active: false
        }
    },

    methods:{
        toggle(){
            this.active = ! this.active
        }
    }

  }
  </script>
  
  <!-- Add "scoped" attribute to limit CSS to this component only -->
  <style scoped>
    button{
        padding: 20px;
        display: block;
        margin: 20px;
        font-size: large;
        background: linear-gradient(20deg, skyblue, pink);
        border: none;
        border-radius: 20px;
        color: gray;
        font-weight: bold;
    }

    .text-red{
        color: red;
    }

    .text-green{
        color: green;
    }
  </style>