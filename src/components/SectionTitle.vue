<script lang="ts">
import { defineComponent } from "vue";
import { PropType } from "vue-demi";
import type { IconType } from "@/common/IconType";

export default defineComponent({
  name: "SectionTitle",
  props: {
    title: { type: String, required: true },
    icon: { type: String as PropType<IconType>, required: true },
  },
});
</script>
<template>
  <div class="title-contaner">
    <span class="title-text">{{ title }}</span>
    <i class="fa-solid" :class="`fa-${icon}`"></i>
  </div>
</template>
