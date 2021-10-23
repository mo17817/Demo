<template>
  <div>
    <navbar></navbar>
    <parralax></parralax>
  </div>
</template>

<script>
import navbar from 'src/components/navbar.vue';
import Parralax from 'src/components/Parralax.vue';
import { defineComponent } from 'vue';

export default defineComponent({
  components: { Parralax }, { navbar },
  name: 'PageIndex'
})
</script>
