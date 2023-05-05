<template>
  <div class="px-14 mt-14">
    <p class="font-bold text-[18px] text-[#323A46]">Professional Summary</p>
    <p class="mt-1 mb-[6px] text-sm text-[#8e929e]">Write 2-4 short & energetic sentences to interest the reader! Mention your role, expereience & most importantly - your biggest achievements best qualities and skils</p>
    <div class="bg-[#F0F2F9] rounded-sm h-56 mt-4">
      <QuillEditor 
        toolbar="#custom-toolbar"
        v-model:content="content" 
        contentType="html"
        >
        <template #toolbar>
          <div class="flex justify-between items-center">
            <div id="custom-toolbar">
              <button class="ql-bold"></button>
              <button class="ql-italic"></button>
              <button class="ql-underline"></button>
              <button class="ql-list" value="ordered"></button>
              <button class="ql-list" value="bullet"></button>
              <button class="ql-link"></button>
            </div>
            <div class="flex pt-3 pr-3">
              <span class="mb-[6px] text-sm text-[#8e929e] mr-1">Pre-written Phrases</span>
              <IconPlus />
            </div>
          </div>
        </template>
      </QuillEditor>
    </div>
  </div>
</template>

<script setup>
import { ref, watch } from 'vue'
import { QuillEditor } from '@vueup/vue-quill'
import '@vueup/vue-quill/dist/vue-quill.snow.css'
import '@vueup/vue-quill/dist/vue-quill.bubble.css'
import IconPlus from '@/components/icon/PlusCicrcle.vue'

const content = ref('e.g Passionate science teacher with 8+ years of expereience and a track record of ...')
watch(() => content.value, (val) => {
  console.log(val)
})
</script>

<style>
  .ql-toolbar.ql-snow {
    border: none;
    padding-top: 12px;
    padding-bottom: 0px;
  }
  .ql-container.ql-snow {
    border: none;
  }
  .ql-editor {
    padding-top: 8px;
    color: #8e929e
  }
</style>
