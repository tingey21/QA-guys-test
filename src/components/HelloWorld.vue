<template>
  <div class="hello">
    <div>Running Total: {{counter}}</div>
    <input v-model="num" type="number">
    <div>{{num}}</div>
   <button v-on:click ="add();" >Add </button>
   <button v-on:click ="subtract()">subtract</button>
   <button v-on:click ="multiply()">multiply</button>
   <button v-on:click ="divide()">divide</button>
    <button>reset</button>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data () {
    return {
      counter: 0,
      num: 0,
    }
  },
  methods:{
    add: function(){
      let number = parseInt(this.num)
      let equals = this.counter += number;
      this.counter = equals
    },
    subtract: function() {
      let number = parseInt(this.num)
      let equals = this.counter - number;
      this.counter = equals
    },
    multiply: function() {
      let number = parseInt(this.num)
      let equals = this.counter += number;
      this.counter = equals
    },
    divide: function() {
      let number = parseInt(this.num)
      let equals = this.counter / this.counter;
      this.counter = equals
    },
    reset: function(){
      this.counter = 0;
      this.num = 0;
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
