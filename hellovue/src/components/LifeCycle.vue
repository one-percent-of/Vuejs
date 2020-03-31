<template>
  <div id="test1">
    <h1>{{ msg }}</h1>
    <h3>{{a1}}</h3>
    <button type="button" v-on:click="setValue">값 변경</button>
  </div>
</template>

<script>
export default {
  name: 'LifeCycle',
  props: {
    msg: String
  },
  data: function () {
    return {
      a1: 100
    }
  },
  // Vue 객체가 관리할 요소들이 만들어지기 전에 호출되는 함수
  beforeCreate: function () {
    console.log('Vue 객체가 관리할 요소들이 만들어지기 전입니다')
    console.log('a1 : ' + this.a1)
  },
  // Vue 객체가 관리할 요소들이 만들어지고 난 이후
  created: function () {
    console.log('Vue 객체가 관리할 요소들이 만들어진 후 입니다')
    console.log('a1 : ' + this.a1)
  },
  // Vue 객체가 관리할 HTML 태그 객체가 할당 되기 전
  beforeMount: function () {
    console.log('Vue 객체가 관리할 태그가 할당 되기 전입니다')
  },
  // Vue 객체가 관리할 HTML 태그 객체가 할당된 후
  mounted: function () {
    console.log('Vue 객체가 관리할 태그가 할당 된 이후 입니다')
  },
  beforeUpdate: function () {
    console.log('관리하고 있는 HTML 요소 내부가 변경되기 전입니다')
  },
  updated: function () {
    console.log('관리하고 있는 HTML 요소 내부가 변경 된 후 입니다')
  },
  beforeDestroy: function () {
    console.log('Vue 객체의 기능이 소멸되기 전입니다')
  },
  destroyed: function () {
    console.log('Vue 객체의 기능이 소멸된 후 입니다')
  },
  methods: {
    setValue: function () {
      this.a1 = 200
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
