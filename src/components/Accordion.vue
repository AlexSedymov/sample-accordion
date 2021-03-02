<template>
<div class="accordion">
  <div v-for="(val, key) in allTexts" :key="key">
    <Head :text="val" @display="hideAll">
    </Head>
  </div>
</div>
</template>

<script>
import Head from "@/components/Head";

export default {
  name: "Accordion",
  components: {
    Head,
  },
  data() {
    return {
      allTexts: this.text
    }
  },
  props: {
    text: {
      type: Array,
      default: () => [],
    },
  },
  methods: {
    hideAll(headerName) {
      for (let i = 0; this.allTexts.length > i; i++) {
        if(this.allTexts[i].name === headerName && this.allTexts[i].display === true) {
          this.allTexts[i].display = !this.allTexts[i].display
          this.allTexts[i].bgColor = this.changeBgColor(this.allTexts[i].display)
        }
        else {
          this.allTexts[i].display = this.allTexts[i].name === headerName;
          this.allTexts[i].bgColor = this.changeBgColor(this.allTexts[i].display)
        }
      }
    },
    changeBgColor(val) { return (val) ? "#B7B7B7" : "#919191"}
  }
}
</script>
<style scoped>
.accordion {
  margin: auto;
  border: 2px solid black;
  border-radius: 5px;
  width: 400px;
}
</style>