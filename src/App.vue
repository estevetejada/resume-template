<script lang="ts">
import { defineComponent } from "vue";
import Sidebar from "@/components/Sidebar.vue";

export default defineComponent({
  name: "App",
  components: { Sidebar },
});
</script>
<template>
  <div class="container">
    <sidebar />
  </div>
</template>

<style lang="scss"></style>
