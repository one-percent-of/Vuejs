<template>
  <div id="test1">
      <h3>{{a1}}</h3>
      <h3>{{a2}}</h3>
      <div>{{a3}}</div>
      <div v-html="a3"></div>
      <img v-bind:src='a4' :width='a5' :height='a6'/>
  </div>
</template>

<script>
export default {
  name: 'Template',
  data: function () {
    return {
      a1: '문자열1',
      a2: '문자열2',
      a3: '<h3>문자열3</h3>',
      a4: require('../assets/logo.png'),
      a5: 150,
      a6: 150
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
