<template>
  <div>
    <p>demo</p>
  </div>
</template>

<script lang="ts" setup>
// https://github.com/antfu/unplugin-vue2-script-setup/issues/17
// PropType for @vue/runtime-core 
import type { PropType } from '@vue/runtime-core';

type BaseProp = number | string
type ObjectProp = {
  params1: number
}

// // work
// defineProps<{ baseProp:BaseProp, objectProp:ObjectProp }>()

// no work
const props = defineProps({

  // no work
  baseProp: {
    type: undefined as unknown as PropType<BaseProp>,
    required: true
  },

  // work
  objectProp: {
    type: undefined as unknown as PropType<ObjectProp>,
    required: true
  }
})

</script>
