<template>
  
  <!-- Esempio vue/max-attributes-per-line (ad es. impostato a 1) -->
  
  <!-- ✓ GOOD -->
  <MyComponent
    lorem="1"
    ipsum="2"
  />
  <MyComponent
    lorem="1"
    ipsum="2"
    dolor="3"
  />

  <!-- ✗ BAD -->
  <MyComponent lorem="1" ipsum="2" />
  <MyComponent lorem="1" ipsum="2" dolor="3" />



  <!-- vue/require-v-for-key -->

  <!-- ✓ GOOD -->
  <ol 
    v-for="todo in todos" 
    :key="todo.id">
  </ol>
  <!-- ✗ BAD -->
  <div v-for="todo in todos" />



  <!-- vue/no-use-v-if-with-v-for -->

  <!-- ✓ GOOD -->
  <ul v-if="complete">
    <TodoItem
      v-for="todo in todos"
      :key="todo.id"
    />
  </ul>
  <TodoItem
    v-for="todo in shownTodos"
    :key="todo.id"
  />

  <!-- ✗ BAD -->
  <TodoItem
    v-for="todo in todos"
    v-if="complete"
    :key="todo.id"
  /><!-- ↑ In this case, the `v-if` should be written on the wrapper element. -->
  <TodoItem
    v-for="todo in todos"
    v-if="todo.shown"
    :key="todo.id"
  /><!-- ↑ In this case, the `v-for` list variable should be replaced with a computed property that returns your filtered list. You should not mix 'v-for' with 'v-if' -->
</template>

<script>
export default {}
</script>
<style lang=""></style>
