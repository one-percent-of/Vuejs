<template>
  <div class="home">
    <LifeCycle msg="Props로 값 넘겨주고 받기"/>
    <Template></Template>
  </div>
</template>

<script>
// @ is an alias to /src
import LifeCycle from '@/components/LifeCycle.vue'
import Template from '@/components/Template.vue'

export default {
  name: 'Home',
  components: {
    LifeCycle,
    Template
  }
}
</script>
