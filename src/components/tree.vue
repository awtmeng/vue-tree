<template>
  <ul class="tree">
    <li>
      <span v-html="data.title"></span>
      <m-tree v-for="(item, idx) in data.children" :data="item" :key="idx"></m-tree>
    </li>
  </ul>
</template>

<script>
  export default {
    name: 'mTree',
    props: {
      data: {
        type: Object,
        default () {
          return {}
        }
      }
    }
  }
</script>
