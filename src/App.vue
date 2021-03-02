<template>
  <div id="app">
    <Accordion :text="text"></Accordion>
  </div>
</template>

<script>
import Accordion from "@/components/Accordion";
export default {
  name: 'App',
  components: {
    Accordion
  },
  data() {
    return{
      text: [
        {
          name: "First item",
          body: "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Duis eget aliquet tellus. " +
              "Fusce id facilisis sapien. Suspendisse vel purus lectus.",
          display: false,
          bgColor: "#919191"
        },
        {
          name: "Second item",
          body: "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Duis eget aliquet tellus. " +
              "Fusce id facilisis sapien. Suspendisse vel purus lectus.",
          display: false,
          bgColor: "#919191"
          },
        {
          name: "Third item",
          body: "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Duis eget aliquet tellus. " +
              "Fusce id facilisis sapien. Suspendisse vel purus lectus.",
          display: false,
          bgColor: "#919191"
        }
      ]
    }
  },
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  margin-top: 60px;
}
</style>
