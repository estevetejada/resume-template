<script lang="ts">
import { ref, defineComponent } from "vue";
import { PropType } from "vue-demi";
import { IconType } from "@/common/IconType";

export default defineComponent({
  name: "SectionItem",
  props: {
    icon: { type: String as PropType<IconType>, required: true },
    placeholder: { type: String, default: "" },
  },
  data() {
    return {
      value: "",
    };
  },
  setup() {
    const isEditable = ref(true);
    const toggleEditable = () => {
      isEditable.value = !isEditable.value;
    };
    return { isEditable, toggleEditable };
  },
});
</script>
<template>
  <div class="section-item-container">
    <i class="fa-solid" :class="`fa-${icon}`"></i>
    <input
      v-model="value"
      type="text"
      :disabled="!isEditable"
      :placeholder="placeholder"
    />
    <button @click="toggleEditable">
      <i v-if="isEditable" class="fa-solid fa-floppy-disk"></i>
      <i v-else class="fa-solid fa-pen"></i>
    </button>
  </div>
</template>
