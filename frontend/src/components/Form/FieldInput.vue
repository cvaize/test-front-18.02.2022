<template>
  <input
    class="field"
    @input="$emit('input', $event)"
    @change="$emit('change', $event)"
    @keydown="$emit('keydown', $event)"
    :value="value"
    :type="type || 'text'"
    :disabled="disabled"
    :readonly="readonly"
    :placeholder="placeholder"
  />
</template>

<script lang="ts" setup>
import { defineEmits, defineProps } from "vue";

defineProps({
  value: [String, Number],
  type: String,
  placeholder: String,
  disabled: Boolean,
  readonly: Boolean,
});
defineEmits(["input", "change", "keydown"]);
</script>
