<template>
  <div>
    <p>{{ text }}</p>
    <ChildInput v-model="text" :value="text" @key-up="text"/>
  </div>
</template>

<script>
import ChildInput from './ChildInput.vue'

export default {
  components: { ChildInput },
  data() {
    return {
      text:"hello",
    }
  }
}
</script>

<style>

</style>