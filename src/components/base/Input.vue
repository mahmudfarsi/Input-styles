<template>
  <input
    :type="type"
    :placeholder="placeholder"
    :id="id"
    :class="['input', elementClass]"
  />
</template>

<script setup>
import { defineProps, computed } from "vue";
import { string, bool } from "vue-types";

const props = defineProps({
  type: string(),
  placeholder: string(),
  id: string(),
  isBorderB: bool().def(false),
  isBorder: bool().def(false),
  isPlaceholderDanger: bool().def(false),
  isPlaceholderWarning: bool().def(false),
  isPlaceholderSuccess: bool().def(false),
  isPlaceholderPrimary: bool().def(false),
  isCapitalize: bool().def(false),
  isPill: bool().def(false),
  isCurve: bool().def(false),
  isBorderBSuccess: bool().def(false),
  isBorderBPrimary: bool().def(false),
  isBorderBDanger: bool().def(false),
  isBorderBInfo: bool().def(false),
  isBorderBWarning: bool().def(false),
  isBorderWarning:bool().def(false),
  isBorderSuccess:bool().def(false),
  isBorderDanger:bool().def(false),
  isBorderPrimary:bool().def(false),
  isBorderInfo:bool().def(false),
  isSharp: bool().def(false),

});

const elementClass = computed(() => ({
  "is-border-bottom": props.isBorderB,
  "is-border": props.isBorder,
  "is-capitalize": props.isCapitalize,
  "is-pill": props.isPill,
  "is-curve": props.isCurve,
  "is-border-danger": props.isBorderBDanger,
  "is-border-b-warning": props.isBorderBWarning,
  "is-border-b-primary": props.isBorderBPrimary,
  "is-border-b-success": props.isBorderBSuccess,
  "is-border-b-info": props.isBorderBInfo,
  "is-sharp": props.isSharp,
  "is-placeholder-danger": props.isPlaceholderDanger,
  "is-placeholder-primary": props.isPlaceholderPrimary,
  "is-placeholder-warning": props.isPlaceholderWarning,
  "is-placeholder-success": props.isPlaceholderSuccess,
  "is-border-primary": props.isBorderPrimary,
  "is-border-success": props.isBorderSuccess,
  "is-border-warning": props.isBorderWarning,
  "is-border-info": props.isBorderInfo,
  "is-border-danger": props.isBorderDanger,
}));
</script>

<style>
.input {
  @apply px-[10px] py-[8px];
}

.input.is-border-bottom {
  @apply border-b-[1px] border-b-black;
}

.input.is-border {
  @apply border-[1px] border-black;
}

.input.is-capitalize {
  @apply capitalize;
}

.input.is-curve {
  @apply rounded-md;
}

.input.is-pill {
  @apply rounded-full;
}

.input.is-border-b-danger {
  @apply border-b-red-500 border-b-[1px];
}

.input.is-border-b-warning {
  @apply border-b-yellow-500 border-b-[1px];
}

.input.is-border-b-primary {
  @apply border-b-blue-500 border-b-[1px];
}

.input.is-border-b-success {
  @apply border-b-lime-400 border-b-[1px];
}


.input.is-border-b-info {
  @apply border-b-sky-400 border-b-[1px];
}

.input.is-sharp {
  @apply rounded-none;
}

.input.is-placeholder-danger::placeholder {
  @apply text-red-400;
}

.input.is-placeholder-success::placeholder {
  @apply text-lime-400;
}

.input.is-placeholder-primary::placeholder {
  @apply text-blue-400;
}

.input.is-placeholder-warning::placeholder {
  @apply text-yellow-500;
}

.input.is-border-primary {
    @apply border-blue-500 border-[1px]
}

.input.is-border-success {
    @apply border-lime-400 border-[1px]
}

.input.is-border-danger {
    @apply border-red-500 border-[1px]
}

.input.is-border-warning {
    @apply border-yellow-500 border-[1px]
}

.input.is-border-info {
    @apply border-sky-400 border-[1px]
}
</style>
