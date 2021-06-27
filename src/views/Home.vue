<template>
  <div class="home">
    <welcome />
  </div>
</template>

<script>
// @ is an alias to /src
// import NavBar from "@/components/NavBar.vue";
// import HelloWorld from "@/components/HelloWorld.vue";
import Welcome from "@/components/Welcome.vue";

export default {
  name: "Home",
  components: {
    // HelloWorld,
    // NavBar,
    Welcome,
  },
};
</script>
