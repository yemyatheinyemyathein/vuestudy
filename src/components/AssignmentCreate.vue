<template>
  <form @submit.prevent="add">
    <input
      :value="newAssignment"
      @keyup="changePageTitle($event.target.value)"
      type="text"
      placeholder="New Assignment..."
    />
    <button type="submit">Add</button>
  </form>
</template>


<script type="module">
export default {
  name: "AssignmentCreate",
  props: {
    assignments: Array,
    add: {},
    newAssignment: {
      default: "",
    },
  },
  data() {
    return {};
  },
  methods: {
    changePageTitle(title) {
      this.$emit("update:newAssignment", title); // previously was `this.$emit('input', title)`
    },
  },
};
</script>


<style>
form input,
form button {
  padding: 5px;
}
</style>