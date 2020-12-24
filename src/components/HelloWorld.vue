<template>
  <p>{{value.fact}}</p>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: ['value']
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
p{
  font-size: 20px;
}
</style>
