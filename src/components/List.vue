<template>
  <div>
    <p>ページ数は{{ pageNum }}ページ</p>
    <ul class="list">
      <li v-for='page in pageNum' :key=page>{{ page }}</li>
    </ul>
  </div>
</template>

<script>
export default {
  name:'List',
  props: {
    pageNum:Number,
  }
}
</script>

<style>
  .list{
    list-style: none;
    display:flex;
    justify-content: center;
    margin: 0;
    padding: 0;
  }
  .list > li + li{
    margin-left: 20px;
  }
</style>