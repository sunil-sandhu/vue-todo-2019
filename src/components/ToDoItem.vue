<template>
  <div class="ToDoItem">
    <p class="ToDoItem-Text">{{item.text}}</p>
    <div class="ToDoItem-Delete" 
         @click="deleteItem(item.id)">-</div>
  </div>
</template>

<script>
export default {
  name: "to-do-item",
  props: ["item"],
  methods: {
    deleteItem(id) {
      this.$emit("delete", id);
    }
  }
};
</script>

<style>
.ToDoItem {
  display: flex;
  justify-content: center;
  align-items: center;
}
</style>