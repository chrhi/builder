<script lang="ts">
import { defineComponent } from 'vue';
import { RenderContent } from '@builder.io/sdk-vue/vue3';

export default defineComponent({
  name: 'DynamicallyRenderBuilderPage',
  components: {
    'builder-render-content': RenderContent,
  },
  props: ['props'],
});
</script>

<template>
  <div v-if="props?.content">
    <builder-render-content v-bind="props" />
  </div>
  <div v-else>Content not Found</div>
</template>
