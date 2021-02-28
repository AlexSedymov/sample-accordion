<template>
  <div>
    <div  class="main-body" v-if="hidden">
      {{ text }}
    </div>
    <div v-else>
    </div>
  </div>
</template>

<script>
export default {
  name: "TextBody",
  props: {
    text: {
      type: String,
      default: ""
    },
    hidden: {
      type: Boolean,
      default: true
    }
  }
}
</script>

<style scoped>
.main-body {
  text-align: left;
  padding: 15px;
  width: auto;
  height: auto;
  background: #b1b1b7;
}
</style>