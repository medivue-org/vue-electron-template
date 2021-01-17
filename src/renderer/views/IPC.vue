<template>
  <div class="section">
    <h1 class="title is-4">
      IPC Test
    </h1>
    <h2 class="subtitle is-6">
      <button @click="ipcTest">Test IPC</button>
    </h2>
  </div>
</template>

<script>
import Vue from 'vue';
import ipc from 'node-ipc';

export default Vue.extend({
  name: 'IPC',
  methods: {
    ipcTest() {
      ipc.of.coordinator.emit('clientA.test', {
        msg: 'test',
      });
    },
  },
});
</script>

<style>
.block.has-text-centered figure {
  margin: 0 auto;
}
</style>
