<template>
  <div class="ToDoItem">
    <p class="ToDoItem-Text">{{item.text}}</p>
    <button class="ToDoItem-Delete" @click="deleteItem(item.id)">-</button>
  </div>
</template>

<script>
export default {
  name: "ToDoItem",
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

.ToDoItem-Text {
  width: 90%;
  background-color: white;
  border: 1px solid lightgrey;
  box-shadow: 1px 1px 1px lightgrey;
  padding: 12px;
  margin-right: 10px;
}

.ToDoItem-Delete {
  padding: 4px 12px;
  cursor: pointer;
  background: #ff7373;
  border-radius: 10px;
  box-shadow: 1px 1px 1px #c70202;
  color: white;
  font-size: 28px;
}

.ToDoItem-Delete:hover {
  box-shadow: none;
  margin-top: 1px;
  margin-left: 1px;
}
</style>