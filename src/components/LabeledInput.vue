<template>
  <div class="relative">
    <input
      :id="id"
      :value="modelValue"
      type="text"
      class="rounded placeholder-transparent peer"
      :placeholder="label"
      @input="$emit('update:modelValue', $event.target.value)"
    >
    <label
      :for="id"
      class="
        block absolute top-1/2 left-2
        -translate-y-8 text-xs bg-white px-2
        transition-all
        peer-focus:-translate-y-8 peer-focus:text-xs
        peer-placeholder-shown:-translate-y-1/2 peer-placeholder-shown:text-base"
    >{{ label }}</label>
  </div>
</template>

<script>
export default {
  props: {
    id: {
      type: String,
      required: true,
    },
    label: {
      type: String,
      default: '',
    },
    modelValue: {
      type: String,
      required: true,
    },
  },
  emits: ['update:modelValue'],
};
</script>

<style>

</style>
