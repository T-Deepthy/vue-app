<template>
<div>
    <h2>heading</h2>
    <div id="app-2">
            <span v-bind:title="message">
                Hover your mouse over me for a few seconds
                to see my dynamically bound title!
            </span>
</div>
<div id="app-3">
  <span v-if="seen">Now you see me</span>
</div>


<div id="app-4">
  <ol>
    <li v-for="todo in todos">
      {{ todo.text }}
    </li>
  </ol>
</div>
</div>
</template>

<script>
export default {
  el: "app-3",
  data () {
    return {
 message: 'You loaded this page on ' + new Date().toLocaleString(),
  seen: true,
  todos: [
      { text: 'Learn JavaScript' },
      { text: 'Learn Vue' },
      { text: 'Build something awesome' }
    ]
    }
  }
}
</script>


<style>

</style>
