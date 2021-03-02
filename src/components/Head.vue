<template>
  <div :style="cssVars">
    <div @click="hider" class="main-head">
      {{ text.name }}
      <div class="symbol">
        <Minus v-if="text.display"></Minus>
        <Plus v-else></Plus>
      </div>
    </div>
    <TextBody :text="text.body" :hidden="text.display" class="symbol-minus"></TextBody>
  </div>
</template>

<script>
import TextBody from "@/components/TextBody";
import Plus from "@/assets/img/plus-small.svg";
import Minus from "@/assets/img/minus-small.svg"

export default {
name: "Head",
  components: {
    TextBody,
    Plus,
    Minus
  },
  props: {
    text: {
      type: Object,
      default: () => {},
    },
  },
  computed: {
    cssVars() {
      return {
        'background-color': this.text.bgColor,
      }
    }
  },
  methods: {
    hider() {
      this.$emit("display", this.text.name)
    },
  }
}
</script>

<style scoped>
.main-head {
  position: relative;
  width: auto;
  text-align: left;
  padding: 15px;
  font-weight: bold;
  border-bottom: 2px solid black;
}
.symbol {
  position: absolute;
  width: 30px;
  right: 10px;
  top: 10px;
}
</style>