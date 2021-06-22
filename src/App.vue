<template>
  <section class="min-h-screen pt-16 flex flex-col items-center gap-12">
    <h1 class="text-2xl">
      Two-Way Binding for own Components
    </h1>
    <labeled-input
      id="firstname"
      v-model="firstname"
      label="Vorname"
    />
    <span>Hello {{ firstname || 'Anonymous' }}!</span>
  </section>
</template>

<script>
import LabeledInput from './components/LabeledInput.vue';

export default {
  name: 'App',
  components: { LabeledInput },
  data: () => ({
    firstname: '',
  }),
};
</script>

<style>

</style>
