<template>
  <div>
    <div @click="hider" class="main-head">
      {{ text.name }}
    </div>
    <TextBody :text="text.body" :hidden="text.display"></TextBody>
  </div>
</template>

<script>
import TextBody from "@/components/TextBody";
export default {
name: "Head",
  components: {
    TextBody
  },
  props: {
    text: {
      type: Object,
      default: () => {},
    }
  },
  methods: {
    hider() {
      this.$emit("display", this.text.name)
    }
  }
}
</script>

<style scoped>
.main-head {
  width: auto;
  text-align: left;
  padding: 15px;
  font-weight: bold;
  background: gray;
  border-bottom: 2px solid black;
}
</style>