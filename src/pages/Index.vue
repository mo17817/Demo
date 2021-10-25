<template>
  <div>
    <navbar></navbar>
  </div>
</template>

<script>
import navbar from 'src/components/navbar.vue';
import { defineComponent } from 'vue';

export default defineComponent({
  components: { navbar },
  name: 'PageIndex'
})
</script>
