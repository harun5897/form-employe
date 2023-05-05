<template>
  <div class="sm:px-14 px-5 mt-11">
    <p class="font-bold text-[18px] text-[#323A46]">Skills</p>
    <p class="mt-1 mb-[6px] text-sm text-[#8e929e]">Choose 5 of the important  skills to show your talents! Make sure they match the keywords of the job listing if applying via an online system.</p>
    <div class="flex flex-wrap">
      <button
        v-for="items in dataLabel"
        class="bg-[#F0F2F9] px-2 text-center rounded text-sm font-[600] pb-1 mr-2 mt-2"
      > {{items.label}} <span class="text-xl font-bold text-[#8e929e]"> + </span></button>
    </div>
    <div class="border-[1px] py-4 px-4 mt-3 rounded-sm" :class="[skillShow]">
      <div class="flex justify-between items-center cursor-pointer" @click="TrigerOpenCloseForm()">
        <div>
          <p class="text-sm text-[#323A46] font-bold">{{ dataSkill }}</p>
          <p class="text-sm text-[#8e929e]">Experienced</p>
        </div>
        <IconArrow :class="[openCloseForm == 'block' ? 'rotate-180' : '']" />
      </div>
      <div class="sm:grid grid-cols-2 items-end gap-8" :class="[openCloseForm]">
        <div>
          <p class="mt-5 mb-[6px] text-sm text-[#8e929e]">Skills</p>
          <Input type="text" @EmitDataInput="getSkill" />
        </div>
        <div>
          <p class="mt-3 mb-[6px] text-sm text-[#8e929e]">Level - <span class="text-orange-300"> Skillfull</span> </p>
          <Input type="text" />
        </div>
      </div>
    </div>
    <button class="text-sm font-semibold text-[#405ce6] mt-5" @click="addSkill()"> <span class="text-xl"> + </span>Add Skills</button>
  </div>
</template>

<script setup>
import { ref } from 'vue'
import IconArrow from '@/components/icon/ArrowDown.vue'
import Input from '@/components/input/Input.vue'

const skillShow = ref('hidden')
const openCloseForm = ref('hidden')
const dataSkill = ref('Skill')

const dataLabel =  ref([
  {
    id: 1,
    label: 'Git'
  },
  {
    id: 2,
    label: 'Java'
  },
  {
    id: 3,
    label: 'Python'
  },
  {
    id: 4,
    label: 'JavaScript'
  },
  {
    id: 5,
    label: 'SQL'
  },
  {
    id: 6,
    label: 'C++'
  },
  {
    id: 7,
    label: 'TypeScript'
  },
  {
    id: 8,
    label: 'C#'
  },
  {
    id: 9,
    label: 'PHP'
  },
  {
    id: 10,
    label: 'Docker'
  },
])

function addSkill() {
  skillShow.value = 'block'
  openCloseForm.value = 'block'
}

function TrigerOpenCloseForm() {
  if(openCloseForm.value == 'hidden') {
    openCloseForm.value = 'block'
  } else if(openCloseForm.value == 'block') {
    openCloseForm.value = 'hidden'
  }
}

function getSkill(val) {
  dataSkill.value = val
}
</script>