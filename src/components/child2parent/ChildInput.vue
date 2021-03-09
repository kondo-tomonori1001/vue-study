<template>
  <label for="text">
    <input id="text" type="text" @keyup="updateValue" />
  </label>
</template>

<script>
export default {
  props: {
    text: {
      type: String,
    },
  },
  // 親のv-modelと紐づけ
  model: {
    prop: "text",
    event: "event",
  },
  methods: {
    // inputタグに入力された時（keyup）で発火するイベント
    updateValue(e) {
      // e.target.valueを親に渡す
      this.$emit("event", e.target.value);
    },
  },
};
</script>

<style>
</style>