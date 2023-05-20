<template>
  <div class="hello">
    <input type="text" :value="modelValue" @input="$emit('update:modelValue',$event.target.value)">
    <input type="text" :value="lastValue" @input="$emit('update:lastValue',$event.target.value)">
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    modelValue: String,
    lastValue: String,
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
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
