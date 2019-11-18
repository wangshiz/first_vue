<template>
  <div class="about">
    <TestComponent msg="this is a testCompobent code"></TestComponent>
  </div>
</template>

<script>// @ is an alias to /src
import TestComponent from '@/components/TestComponent.vue'

export default {
  name: 'about',
  components: {
    TestComponent
  }
}

</script>
