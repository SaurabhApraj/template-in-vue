<template>
  <div>
    <p v-html="rowHtml"></p>
    <h3 v-once>{{ name }}</h3>
    <h3>{{ name }}</h3>
    <h3>{{ok?"Yes":"No"}}</h3>
    <!--Ternery Operator-->
    <h3>Addition: {{10+10}}</h3>
    <h3>Subtraction: {{b-a}}</h3>

    <button v-bind:disabled="disabledBtn" v-on:click="updateName">Click me</button>
  </div>
</template>
<script>
export default {
  name: "Home",
  data() {
    return {
      name: "Saurabh",
      a: 10,
      b: 20,
      ok: false,
      rowHtml: "<h1>Hello Saurabh</h1>",
      disabledBtn: false
    };
  },
  methods: {
    updateName() {
      this.ok = !this.ok;
    }
  }
};
</script>
