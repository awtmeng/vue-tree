<template>
  <div>
    <Tree :data="data" @nodeClick="nCllick"></Tree>
  </div>
</template>

<script>
  import Tree from '@/components/tree.vue'

  export default {
    components: {Tree},
    name: 'app',
    data () {
      return {
        data: {
          'title': '111',
          'children': [
            {
              'title': '111 - 1'
            }, {
              'title': '111 - 2',
              'children': [
                {
                  'title': '111 - 2 - 1',
                  'children': [
                    {
                      'title': '111 - 2 - 1 - 1'
                    }
                  ]
                }
              ]
            }
          ]
        }
      }
    },
    methods: {
      nCllick (title) {
        console.log(title)
      }
    }

  }
</script>
