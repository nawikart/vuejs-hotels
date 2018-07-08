<template>
  <div>
    <p>&nbsp;</p>
    <p>&nbsp;</p>
    <p>&nbsp;</p>
    <p>&nbsp;</p>
    mixins   
  </div>
</template>


<script>
  export default {
    data () {
      return {
        map: false,
      }
    }
  }

import Vue from 'vue'

var mixin = {
  data: function () {
    return {
      message: 'hello',
      foo: 'abc'
    }
  }
}

new Vue({
  mixins: [mixin],
  data: function () {
    return {
      message: 'goodbye',
      bar: 'def'
    }
  },
  created: function () {
    console.log(this.$data)
    // => { message: "goodbye", foo: "abc", bar: "def" }
  }
})

// define a component that uses this mixin
var Component = Vue.extend({
  mixins: [mixin]
})

var component = new Component() // => "hello from mixin!"  
</script>