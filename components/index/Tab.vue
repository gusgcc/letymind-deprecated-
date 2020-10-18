<template>
  <div class="tab">

  </div>
</template>

<script>
export default {
  props: {
    name: String
  },
  data () {
    return {
      name_tab: 'name_tab' + Math.random() * 999999
    }
  }
}
</script>

<style lang="sass" scoped>
.tab
  
</style>