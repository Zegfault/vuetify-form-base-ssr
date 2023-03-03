<script>
import Vue from 'vue';
import VuetifyFormBaseSsr from '@/vuetify-form-base-ssr.vue';

export default Vue.extend({
  name: 'ServeDev',
  components: {
    VuetifyFormBaseSsr
  }
});
</script>

<template>
  <div id="app">
    <vuetify-form-base-ssr :schema="{
        name: { type: 'text', label: 'Name', col: 8, offset: 1 },
        position: { type: 'text', label: 'Position', col: 8, offset: 1 },
        tasks: {
          type: 'array',
          col: 8,
          offset: 1,
          schema: {
            done: { type: 'checkbox', label: 'done', col: 4 },
            title: { type: 'text', col: 4 }
          }
        }
      }" />
  </div>
</template>
