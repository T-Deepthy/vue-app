<template>
  <div id="app">
    <h1>{{ header }}</h1>
    <div id="example-1">
        <input v-model="msg" placeholder="type message">
        <p>new message: {{ msg }}</p>
    </div>
    <br>
    <div id="example-2">
        <span>multiline message is</span>
        <p style="white-space: pre-line;"> {{ multiline }}</p>
        <textarea v-model="multiline" placeholder="add multiple lines"></textarea>
    </div>
    <br>
    <div id="example-3">
        <input type="checkbox" id="checkbox" v-model="checked">
        <label for="checkbox">{{ checked}}</label>
    </div>
    <br>
    <div id="example-4">
      <input type="checkbox" id="name" value="Name" v-model="checkedFields">
      <label for="name">Name</label>
      <input type="checkbox" id="empid" value="Employee id" v-model="checkedFields">
      <label for="empid">Employee id</label>
      <input type="checkbox" id="dept" value="Department" v-model="checkedFields">
      <label for="dept">Department</label>
      <br>
      <span>Checked Fields: {{ checkedFields }}</span>
    </div>
    <br>
    <div id="example-5">
        <input type="radio" id="one" value="one" v-model="picked">
        <label for="one">one</label>
        <input type="radio" id="two" value="two" v-model="picked">
        <label for="two">two</label>
        <br>
        <span>picked: {{ picked }}</span>
    </div>
    <br>
    <div id="example-6">
        <select v-model="selected">
          <option disabled value="">Please select one</option>
          <option>A</option>
          <option>B</option>
          <option>C</option>
        </select>
    </div>
    <br>
    <div id="example-7">
      <select v-model="selected_multiple" multiple>
        <option>A</option>
        <option>B</option>
        <option>C</option>
      </select>
      <br>
        <span>Selected: {{ selected_multiple }}</span>
    </div>
    <br>
    <div id="example-8">
      <select v-model="selectedf">
        <option v-for="option in options" v-bind:key="option.id" v-bind:value="option.value">
          {{ option.text }}
        </option>
      </select>
      <span>Selected: {{ selectedf }}</span>
    </div>
    <br>
    <div id="example-9">
        <input type="radio" v-model="picked" value="a">
        <input type="checkbox" v-model="checked">
        <select v-model="selected">
          <option value="abc">ABC</option>
        </select>
        <br>
         <input
            type="checkbox"
            v-model="toggle"
            true-value="yes"
            false-value="no"
          >
        <span>togggle: {{ toggle }}</span>
        <br>
        <input type="radio" v-model="picked" v-bind:value="a">
      <br>
      <select v-model="selected">
  <!-- inline object literal -->
  <option v-bind:value="{ number: 124 }">124</option>
  <br>
  <input v-model.number="age" type="number">
</select>
    </div>
  </div>
</template>

<script>
export default {
  el: "example-8",
  data () {
    return {
      header: 'Hashroot technologies pvt ltd!',
      msg: "hello",
      multiline: "line1",
      checked: false,
      checkedFields: [],
      picked: "",
      selected: "",
      selected_multiple: [],
      selectedf: 'A',
      options: [ 
        {text: 'one', value: 'A'},
        {text: 'two', value: 'B'},
        {text: 'three', value: 'C'},
      ],
      toggle: 'yes'
    }
  }
}
</script>

<style>
</style>
