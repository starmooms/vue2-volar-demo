<template>
  <div>
    <p>{{ value }}</p>
  </div>
</template>

<script lang="ts" setup>
// https://github.com/antfu/unplugin-vue2-script-setup/issues/17
// PropType for @vue/runtime-core 
import type { PropType } from '@vue/runtime-core';

type SelectId = number | string

// // work
// defineProps<{ value: SelectId }>()

// no work
const props = defineProps({
  value: {
    type: undefined as unknown as PropType<SelectId>,
    required: true
  },
})

const a = props.value
</script>

<style scoped>
a {
  color: #42b983;
}

label {
  margin: 0 0.5em;
  font-weight: bold;
}

code {
  background-color: #eee;
  padding: 2px 4px;
  border-radius: 4px;
  color: #304455;
}
</style>
