<script lang="ts">
import { defineComponent } from "vue";
import SectionTitle from "./SectionTitle.vue";
import SectionItem from "./SectionItem.vue";

export default defineComponent({
  name: "ContactInfo",
  components: { SectionTitle, SectionItem },
});
</script>
<template>
  <div class="contact-info-container">
    <section-title icon="phone" title="Contact" />
    <section-item icon="phone" placeholder="Telefono" />
    <section-item icon="envelope" placeholder="Mail" />
    <section-item icon="location-dot" placeholder="Direccion" />
    <section-item icon="globe" placeholder="Web" />
  </div>
</template>
