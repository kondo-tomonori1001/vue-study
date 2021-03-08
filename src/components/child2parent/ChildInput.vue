<template>
  <label for="text">
    <input id="text" v-model="text" type="text" @change="updateValue">
  </label>
</template>

<script>
export default {
  props: {
    text: {
      type: String,
      required: true,
    },
    model: {
      prop: 'value',
      event: 'change'
    }
  },
  methods: {
    updateValue(e) {
      this.$emit('change', e.target.value);
    }
  }
}
</script>

<style>

</style>