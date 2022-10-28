<template>
  <div class="hello">

  </div>
</template>

<script>
export default {
  props: {
    msg: String
  },
  methods: {
    removeTitle() {
      this.$emit('removeTitle', this.msg) 
    }
  }
}
</script>

<style scoped>

</style>
