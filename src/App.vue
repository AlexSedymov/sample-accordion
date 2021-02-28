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
      // text: [
      //   {"First item": { body: "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Duis eget aliquet tellus. " +
      //       "Fusce id facilisis sapien. Suspendisse vel purus lectus.", display: false }},
      //   {"Second item": { body: "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Duis eget aliquet tellus. " +
      //       "Fusce id facilisis sapien. Suspendisse vel purus lectus.", display: false }},
      //   {"Third item": { body: "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Duis eget aliquet tellus. " +
      //       "Fusce id facilisis sapien. Suspendisse vel purus lectus.", display: false }},
      // ]
      text: [
        {
          name: "First item",
          body: "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Duis eget aliquet tellus. " +
              "Fusce id facilisis sapien. Suspendisse vel purus lectus.",
          display: false
        },
        {
          name: "Second item",
          body: "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Duis eget aliquet tellus. " +
              "Fusce id facilisis sapien. Suspendisse vel purus lectus.",
          display: false
          },
        {
          name: "Third item",
          body: "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Duis eget aliquet tellus. " +
              "Fusce id facilisis sapien. Suspendisse vel purus lectus.",
          display: false
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
