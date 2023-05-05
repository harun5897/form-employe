<template>
  <div class="input">
    <input 
      :type="inputType"
      @input="dataInput"
      class="h-[45px] bg-[#F0F2F9] w-full rounded-sm focus:outline-none px-4 font-[600] text-base text-[#323A46]"
      :placeholder="props.placeholder"
      v-model="data"
    >
  </div>
</template>

<script setup>
import { ref, watch } from 'vue'

const props = defineProps({
  placeholder: '',
  type: String,
})
//Emit
const emit = defineEmits(['EmitDataInput'])

const data = ref()

// Emit for return value on input to parent
function dataInput(event) {
  emit('EmitDataInput', event.target.value)
}

const inputType = ref(props.type)

watch(() => props.type, (newValue) => {
  inputType.value = newValue
})
</script>