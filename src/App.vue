<template>
  <div id="app">
    <test-slot>
      <template #some-name>
        <div v-if="false">
          This is set to false
        </div>
        This should show up but it won't
      </template>
    </test-slot>
    <test-slot>
      <template #some-name>
        <div v-if="true">
          This is set to true
        </div>
        This should show up and it would
      </template>
    </test-slot>
  </div>
</template>

<script>
import TestSlot from './components/TestSlot.vue'

export default {
  name: 'app',
  components: {
    'test-slot': TestSlot,
  }
}
</script>
