<script lang="ts">
import { defineComponent } from "vue";
import ContactInfo from "./ContactInfo.vue";

export default defineComponent({
  name: "Sidebar",
  components: { ContactInfo },
});
</script>
<template>
  <div class="sidebar-container">
    <!-- image -->
    <contact-info />
    <!-- skills -->
    <!-- language -->
    <!-- hobbies -->
    <slot />
  </div>
</template>
