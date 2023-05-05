<template>
  <div class="employment-history">
    <div class="sm:px-14 px-5 mt-11">
      <p class="font-bold text-[18px] text-[#323A46]">Education</p>
      <p class="mt-1 mb-[6px] text-sm text-[#8e929e]">A Veried education on your resume sums up the value that your learnings and background will bring to job.</p>
      <!-- Form 1 -->
      <div class="form" :class="[employe1]">
        <div class="border-[1px] py-4 px-4 mt-3 rounded-sm">
          <div 
            class="hidden-form"
            :class="[hiddenForm1]"
          >
            <div class="flex justify-between items-center cursor-pointer" @click="trigerOpenForm(1)">
              <div>
                <p class="text-sm text-[#323A46] font-bold">{{ jobTitle1 }} at {{ company1 }}</p>
                <p class="text-sm text-[#8e929e]">{{ startDate1 }} - {{ endDate1 }} </p>
              </div>
              <IconArrow />
            </div>
          </div>
          <div 
            class="show-form"
            :class="[showForm1]"
          >
            <div class="flex justify-between cursor-pointer" @click="trigerCloseForm(1)">
              <p class="text-sm font-bold text-[#323A46]">(Not specified)</p>
              <IconArrow class="rotate-180" />
            </div>
              <div class="grid grid-cols-2 items-end gap-8">
                <div>
                  <p class="mt-5 mb-[6px] text-sm text-[#8e929e]">Degree</p>
                  <Input type="text" @EmitDataInput="getJobTitle1" />
                </div>
                <div>
                  <p class="mt-3 mb-[6px] text-sm text-[#8e929e]">School</p>
                  <Input type="text" @EmitDataInput="getCompany1" />
                </div>
              </div>
              <div class="grid grid-cols-2 items-end gap-8">
                <div>
                  <p class="mt-5 mb-[6px] text-sm text-[#8e929e]">Start & End Date</p>
                  <div class="grid grid-cols-2 gap-4">
                    <input  
                      placeholder="MM/YYYY"
                      type="text"
                      onfocus="(this.type='month')"
                      onblur="(this.type='text')"
                      @input="getStartDate1"
                      class="h-[45px] bg-[#F0F2F9] w-full rounded-sm focus:outline-none px-4 font-[400] text-base text-[#323A46]"
                    >
                    <input 
                      type="text" 
                      placeholder="MM/YYYY"
                      @input="getEndDate1"
                      onfocus="(this.type='month')"
                      onblur="(this.type='text')"
                      class="h-[45px] bg-[#F0F2F9] w-full rounded-sm focus:outline-none px-4 font-[400] text-base text-[#323A46]"
                    >
                  </div>
                </div>
                <div>
                  <p class="mt-3 mb-[6px] text-sm text-[#8e929e]">city</p>
                  <Input type="text" />
                </div>
              </div>
              <p class="mt-5 mb-[6px] text-sm text-[#8e929e]">Description</p>
              <div class="bg-[#F0F2F9] rounded-sm h-56">
                <QuillEditor
                  v-model:content="content" 
                  contentType="html"
                  toolbar="#education-toolbar1"
                >
                <template #toolbar>
                  <div id="education-toolbar1">
                    <div class="flex justify-between">
                      <div>
                        <button class="ql-bold"></button>
                        <button class="ql-italic"></button>
                        <button class="ql-underline"></button>
                        <button class="ql-list" value="ordered"></button>
                        <button class="ql-list" value="bullet"></button>
                        <button class="ql-link"></button>
                      </div>
                      <div class="flex pr-1">
                        <span class="mb-[6px] text-sm text-[#8e929e] mr-1">Pre-written Phrases</span>
                        <IconPlus />
                      </div>
                    </div>
                  </div>
                </template>
              </QuillEditor>
            </div>
            <div class="flex justify-between">
              <p class="mt-2 mb-[6px] text-sm text-[#8e929e]">Recuiter tip: write 200+ characters to increase interview chances</p>
              <p class="mt-2 mb-[6px] text-sm text-[#8e929e]">0/200+</p>
            </div>
          </div>
        </div>
      </div>

      <!-- FORM 2 -->
      <div class="form" :class="[employe2]">
        <div class="border-[1px] py-4 px-4 mt-3 rounded-sm">
          <div 
            class="hidden-form"
            :class="[hiddenForm2]"
          >
            <div class="flex justify-between items-center cursor-pointer" @click="trigerOpenForm(2)">
              <div>
                <p class="text-sm text-[#323A46] font-bold">{{ jobTitle2 }} at {{ company2 }}</p>
                <p class="text-sm text-[#8e929e]">{{ startDate2 }} - {{ endDate2 }} </p>
              </div>
              <IconArrow />
            </div>
          </div>
          <div 
            class="show-form"
            :class="[showForm2]"
          >
            <div class="flex justify-between cursor-pointer" @click="trigerCloseForm(2)">
              <p class="text-sm font-bold text-[#323A46]">(Not specified)</p>
              <IconArrow class="rotate-180" />
            </div>
              <div class="grid grid-cols-2 items-end gap-8">
                <div>
                  <p class="mt-5 mb-[6px] text-sm text-[#8e929e]">Degree</p>
                  <Input type="text" @EmitDataInput="getJobTitle2" />
                </div>
                <div>
                  <p class="mt-3 mb-[6px] text-sm text-[#8e929e]">School</p>
                  <Input type="text" @EmitDataInput="getCompany2" />
                </div>
              </div>
              <div class="grid grid-cols-2 items-end gap-8">
                <div>
                  <p class="mt-5 mb-[6px] text-sm text-[#8e929e]">Start & End Date</p>
                  <div class="grid grid-cols-2 gap-4">
                    <input  
                      placeholder="MM/YYYY"
                      type="text"
                      onfocus="(this.type='month')"
                      onblur="(this.type='text')"
                      @input="getStartDate2"
                      class="h-[45px] bg-[#F0F2F9] w-full rounded-sm focus:outline-none px-4 font-[400] text-base text-[#323A46]"
                    >
                    <input 
                      type="text" 
                      placeholder="MM/YYYY"
                      @input="getEndDate2"
                      onfocus="(this.type='month')"
                      onblur="(this.type='text')"
                      class="h-[45px] bg-[#F0F2F9] w-full rounded-sm focus:outline-none px-4 font-[400] text-base text-[#323A46]"
                    >
                  </div>
                </div>
                <div>
                  <p class="mt-3 mb-[6px] text-sm text-[#8e929e]">city</p>
                  <Input type="text" />
                </div>
              </div>
              <p class="mt-5 mb-[6px] text-sm text-[#8e929e]">Description</p>
              <div class="bg-[#F0F2F9] rounded-sm h-56">
                <QuillEditor
                  v-model:content="content" 
                  contentType="html"
                  toolbar="#education-toolbar2"
                >
                <template #toolbar>
                  <div id="education-toolbar2">
                    <div class="flex justify-between">
                      <div>
                        <button class="ql-bold"></button>
                        <button class="ql-italic"></button>
                        <button class="ql-underline"></button>
                        <button class="ql-list" value="ordered"></button>
                        <button class="ql-list" value="bullet"></button>
                        <button class="ql-link"></button>
                      </div>
                      <div class="flex pr-1">
                        <span class="mb-[6px] text-sm text-[#8e929e] mr-1">Pre-written Phrases</span>
                        <IconPlus />
                      </div>
                    </div>
                  </div>
                </template>
              </QuillEditor>
            </div>
            <div class="flex justify-between">
              <p class="mt-2 mb-[6px] text-sm text-[#8e929e]">Recuiter tip: write 200+ characters to increase interview chances</p>
              <p class="mt-2 mb-[6px] text-sm text-[#8e929e]">0/200+</p>
            </div>
          </div>
        </div>
      </div>

      <!-- FORM 3 -->
      <div class="form" :class="[employe3]">
        <div class="border-[1px] py-4 px-4 mt-3 rounded-sm">
          <div 
            class="hidden-form"
            :class="[hiddenForm3]"
          >
            <div class="flex justify-between items-center cursor-pointer" @click="trigerOpenForm(3)">
              <div>
                <p class="text-sm text-[#323A46] font-bold">{{ jobTitle3 }} at {{ company3 }}</p>
                <p class="text-sm text-[#8e929e]">{{ startDate3 }} - {{ endDate3 }} </p>
              </div>
              <IconArrow />
            </div>
          </div>
          <div 
            class="show-form"
            :class="[showForm3]"
          >
            <div class="flex justify-between cursor-pointer" @click="trigerCloseForm(3)">
              <p class="text-sm font-bold text-[#323A46]">(Not specified)</p>
              <IconArrow class="rotate-180" />
            </div>
              <div class="grid grid-cols-2 items-end gap-8">
                <div>
                  <p class="mt-5 mb-[6px] text-sm text-[#8e929e]">Degree</p>
                  <Input type="text" @EmitDataInput="getJobTitle3" />
                </div>
                <div>
                  <p class="mt-3 mb-[6px] text-sm text-[#8e929e]">School</p>
                  <Input type="text" @EmitDataInput="getCompany3" />
                </div>
              </div>
              <div class="grid grid-cols-2 items-end gap-8">
                <div>
                  <p class="mt-5 mb-[6px] text-sm text-[#8e929e]">Start & End Date</p>
                  <div class="grid grid-cols-2 gap-4">
                    <input  
                      placeholder="MM/YYYY"
                      type="text"
                      onfocus="(this.type='month')"
                      onblur="(this.type='text')"
                      @input="getStartDate3"
                      class="h-[45px] bg-[#F0F2F9] w-full rounded-sm focus:outline-none px-4 font-[400] text-base text-[#323A46]"
                    >
                    <input 
                      type="text" 
                      placeholder="MM/YYYY"
                      @input="getEndDate3"
                      onfocus="(this.type='month')"
                      onblur="(this.type='text')"
                      class="h-[45px] bg-[#F0F2F9] w-full rounded-sm focus:outline-none px-4 font-[400] text-base text-[#323A46]"
                    >
                  </div>
                </div>
                <div>
                  <p class="mt-3 mb-[6px] text-sm text-[#8e929e]">city</p>
                  <Input type="text" />
                </div>
              </div>
              <p class="mt-5 mb-[6px] text-sm text-[#8e929e]">Description</p>
              <div class="bg-[#F0F2F9] rounded-sm h-56">
                <QuillEditor
                  v-model:content="content" 
                  contentType="html"
                  toolbar="#education-toolbar3"
                >
                <template #toolbar>
                  <div id="education-toolbar3">
                    <div class="flex justify-between">
                      <div>
                        <button class="ql-bold"></button>
                        <button class="ql-italic"></button>
                        <button class="ql-underline"></button>
                        <button class="ql-list" value="ordered"></button>
                        <button class="ql-list" value="bullet"></button>
                        <button class="ql-link"></button>
                      </div>
                      <div class="flex pr-1">
                        <span class="mb-[6px] text-sm text-[#8e929e] mr-1">Pre-written Phrases</span>
                        <IconPlus />
                      </div>
                    </div>
                  </div>
                </template>
              </QuillEditor>
            </div>
            <div class="flex justify-between">
              <p class="mt-2 mb-[6px] text-sm text-[#8e929e]">Recuiter tip: write 200+ characters to increase interview chances</p>
              <p class="mt-2 mb-[6px] text-sm text-[#8e929e]">0/200+</p>
            </div>
          </div>
        </div>
      </div>

      <!-- FORM 4 -->
      <div class="form" :class="[employe4]">
        <div class="border-[1px] py-4 px-4 mt-3 rounded-sm">
          <div 
            class="hidden-form"
            :class="[hiddenForm4]"
          >
            <div class="flex justify-between items-center cursor-pointer" @click="trigerOpenForm(4)">
              <div>
                <p class="text-sm text-[#323A46] font-bold">{{ jobTitle4 }} at {{ company4 }}</p>
                <p class="text-sm text-[#8e929e]">{{ startDate4 }} - {{ endDate4 }} </p>
              </div>
              <IconArrow />
            </div>
          </div>
          <div 
            class="show-form"
            :class="[showForm4]"
          >
            <div class="flex justify-between cursor-pointer" @click="trigerCloseForm(4)">
              <p class="text-sm font-bold text-[#323A46]">(Not specified)</p>
              <IconArrow class="rotate-180" />
            </div>
              <div class="grid grid-cols-2 items-end gap-8">
                <div>
                  <p class="mt-5 mb-[6px] text-sm text-[#8e929e]">Degree</p>
                  <Input type="text" @EmitDataInput="getJobTitle4" />
                </div>
                <div>
                  <p class="mt-3 mb-[6px] text-sm text-[#8e929e]">School</p>
                  <Input type="text" @EmitDataInput="getCompany4" />
                </div>
              </div>
              <div class="grid grid-cols-2 items-end gap-8">
                <div>
                  <p class="mt-5 mb-[6px] text-sm text-[#8e929e]">Start & End Date</p>
                  <div class="grid grid-cols-2 gap-4">
                    <input  
                      placeholder="MM/YYYY"
                      type="text"
                      onfocus="(this.type='month')"
                      onblur="(this.type='text')"
                      @input="getStartDate4"
                      class="h-[45px] bg-[#F0F2F9] w-full rounded-sm focus:outline-none px-4 font-[400] text-base text-[#323A46]"
                    >
                    <input 
                      type="text" 
                      placeholder="MM/YYYY"
                      @input="getEndDate4"
                      onfocus="(this.type='month')"
                      onblur="(this.type='text')"
                      class="h-[45px] bg-[#F0F2F9] w-full rounded-sm focus:outline-none px-4 font-[400] text-base text-[#323A46]"
                    >
                  </div>
                </div>
                <div>
                  <p class="mt-3 mb-[6px] text-sm text-[#8e929e]">city</p>
                  <Input type="text" />
                </div>
              </div>
              <p class="mt-5 mb-[6px] text-sm text-[#8e929e]">Description</p>
              <div class="bg-[#F0F2F9] rounded-sm h-56">
                <QuillEditor
                  v-model:content="content" 
                  contentType="html"
                  toolbar="#education-toolbar4"
                >
                <template #toolbar>
                  <div id="education-toolbar4">
                    <div class="flex justify-between">
                      <div>
                        <button class="ql-bold"></button>
                        <button class="ql-italic"></button>
                        <button class="ql-underline"></button>
                        <button class="ql-list" value="ordered"></button>
                        <button class="ql-list" value="bullet"></button>
                        <button class="ql-link"></button>
                      </div>
                      <div class="flex pr-1">
                        <span class="mb-[6px] text-sm text-[#8e929e] mr-1">Pre-written Phrases</span>
                        <IconPlus />
                      </div>
                    </div>
                  </div>
                </template>
              </QuillEditor>
            </div>
            <div class="flex justify-between">
              <p class="mt-2 mb-[6px] text-sm text-[#8e929e]">Recuiter tip: write 200+ characters to increase interview chances</p>
              <p class="mt-2 mb-[6px] text-sm text-[#8e929e]">0/200+</p>
            </div>
          </div>
        </div>
      </div>

      <!-- FORM 5 -->
      <div class="form" :class="[employe5]">
        <div class="border-[1px] py-4 px-4 mt-3 rounded-sm">
          <div 
            class="hidden-form"
            :class="[hiddenForm5]"
          >
            <div class="flex justify-between items-center cursor-pointer" @click="trigerOpenForm(5)">
              <div>
                <p class="text-sm text-[#323A46] font-bold">{{ jobTitle5 }} at {{ company5 }}</p>
                <p class="text-sm text-[#8e929e]">{{ startDate5 }} - {{ endDate5 }} </p>
              </div>
              <IconArrow />
            </div>
          </div>
          <div 
            class="show-form"
            :class="[showForm5]"
          >
            <div class="flex justify-between cursor-pointer" @click="trigerCloseForm(5)">
              <p class="text-sm font-bold text-[#323A46]">(Not specified)</p>
              <IconArrow class="rotate-180" />
            </div>
              <div class="grid grid-cols-2 items-end gap-8">
                <div>
                  <p class="mt-5 mb-[6px] text-sm text-[#8e929e]">Degree</p>
                  <Input type="text" @EmitDataInput="getJobTitle5" />
                </div>
                <div>
                  <p class="mt-3 mb-[6px] text-sm text-[#8e929e]">School</p>
                  <Input type="text" @EmitDataInput="getCompany5" />
                </div>
              </div>
              <div class="grid grid-cols-2 items-end gap-8">
                <div>
                  <p class="mt-5 mb-[6px] text-sm text-[#8e929e]">Start & End Date</p>
                  <div class="grid grid-cols-2 gap-4">
                    <input  
                      placeholder="MM/YYYY"
                      type="text"
                      onfocus="(this.type='month')"
                      onblur="(this.type='text')"
                      @input="getStartDate5"
                      class="h-[45px] bg-[#F0F2F9] w-full rounded-sm focus:outline-none px-4 font-[400] text-base text-[#323A46]"
                    >
                    <input 
                      type="text" 
                      placeholder="MM/YYYY"
                      @input="getEndDate5"
                      onfocus="(this.type='month')"
                      onblur="(this.type='text')"
                      class="h-[45px] bg-[#F0F2F9] w-full rounded-sm focus:outline-none px-4 font-[400] text-base text-[#323A46]"
                    >
                  </div>
                </div>
                <div>
                  <p class="mt-3 mb-[6px] text-sm text-[#8e929e]">city</p>
                  <Input type="text" />
                </div>
              </div>
              <p class="mt-5 mb-[6px] text-sm text-[#8e929e]">Description</p>
              <div class="bg-[#F0F2F9] rounded-sm h-56">
                <QuillEditor
                  v-model:content="content" 
                  contentType="html"
                  toolbar="#education-toolbar5"
                >
                <template #toolbar>
                  <div id="education-toolbar5">
                    <div class="flex justify-between">
                      <div>
                        <button class="ql-bold"></button>
                        <button class="ql-italic"></button>
                        <button class="ql-underline"></button>
                        <button class="ql-list" value="ordered"></button>
                        <button class="ql-list" value="bullet"></button>
                        <button class="ql-link"></button>
                      </div>
                      <div class="flex pr-1">
                        <span class="mb-[6px] text-sm text-[#8e929e] mr-1">Pre-written Phrases</span>
                        <IconPlus />
                      </div>
                    </div>
                  </div>
                </template>
              </QuillEditor>
            </div>
            <div class="flex justify-between">
              <p class="mt-2 mb-[6px] text-sm text-[#8e929e]">Recuiter tip: write 200+ characters to increase interview chances</p>
              <p class="mt-2 mb-[6px] text-sm text-[#8e929e]">0/200+</p>
            </div>
          </div>
        </div>
      </div>
      <button class="text-sm font-semibold text-[#405ce6] mt-2" @click="addEmploye()"> <span class="text-xl"> + </span>Add Education</button>
    </div>
  </div>
</template>

<script setup>
import { ref, watch } from 'vue'
import Input from '@/components/input/Input.vue'
import { QuillEditor } from '@vueup/vue-quill'
import '@vueup/vue-quill/dist/vue-quill.snow.css'
import '@vueup/vue-quill/dist/vue-quill.bubble.css'
import IconPlus from '@/components/icon/PlusCicrcle.vue'
import IconArrow from '@/components/icon/ArrowDown.vue'

const content = ref('e.g Graduated with High Honors.')

const showForm1 = ref('hidden')
const hiddenForm1 = ref('hidden')
const employe1 =  ref('hidden')

const showForm2 = ref('hidden')
const hiddenForm2 = ref('hidden')
const employe2 =  ref('hidden')

const showForm3 = ref('hidden')
const hiddenForm3 = ref('hidden')
const employe3 =  ref('hidden')

const showForm4 = ref('hidden')
const hiddenForm4 = ref('hidden')
const employe4 =  ref('hidden')

const showForm5 = ref('hidden')
const hiddenForm5 = ref('hidden')
const employe5 =  ref('hidden')

const jobTitle1 = ref('Degree')
const company1 = ref('Shcool')
const startDate1 = ref('')
const endDate1 = ref('')

const jobTitle2 = ref('Degree')
const company2 = ref('Shcool')
const startDate2 = ref('')
const endDate2 = ref('')

const jobTitle3 = ref('Degree')
const company3 = ref('Shcool')
const startDate3 = ref('')
const endDate3 = ref('')

const jobTitle4 = ref('Degree')
const company4 = ref('Shcool')
const startDate4 = ref('')
const endDate4 = ref('')

const jobTitle5 = ref('Degree')
const company5 = ref('Shcool')
const startDate5 = ref('')
const endDate5 = ref('')

function addEmploye () {
  if(employe1.value == 'hidden') {
    employe1.value = 'block'
    showForm1.value = 'block'
  } else if(employe2.value == 'hidden') {
    employe2.value = 'block'
    showForm2.value = 'block'
  } else if(employe3.value == 'hidden') {
    employe3.value = 'block'
    showForm3.value = 'block'
  } else if(employe4.value == 'hidden') {
    employe4.value = 'block'
    showForm4.value = 'block'
  }else if(employe5.value == 'hidden') {
    employe5.value = 'block'
    showForm5.value = 'block'
  }
}

function trigerOpenForm (val) {
  if(val == 1) {
    showForm1.value = 'block'
    hiddenForm1.value = 'hidden'
  } else if(val == 2) {
    showForm2.value = 'block'
    hiddenForm2.value = 'hidden'
  }
  else if(val == 3) {
    showForm3.value = 'block'
    hiddenForm3.value = 'hidden'
  }
  else if(val == 4) {
    showForm4.value = 'block'
    hiddenForm4.value = 'hidden'
  }
  else if(val == 5) {
    showForm5.value = 'block'
    hiddenForm5.value = 'hidden'
  }
}
function trigerCloseForm (val) {
  if(val == 1) {
    showForm1.value = 'hidden'
    hiddenForm1.value = 'block'
  }else if(val == 2) {
    showForm2.value = 'hidden'
    hiddenForm2.value = 'block'
  }else if(val == 3) {
    showForm3.value = 'hidden'
    hiddenForm3.value = 'block'
  }else if(val == 4) {
    showForm4.value = 'hidden'
    hiddenForm4.value = 'block'
  }
  else if(val == 5) {
    showForm5.value = 'hidden'
    hiddenForm5.value = 'block'
  }
}

function getJobTitle1(value) {
  jobTitle1.value = value
}
function getCompany1(value) {
  company1.value = value
}
function getStartDate1 (event) {
  const selectedDate = new Date(event.target.value + '-01');
  startDate1.value = selectedDate.toLocaleString('default', { month: 'long' }) + ' ' + selectedDate.getFullYear()
}
function getEndDate1 (event) {
  const selectedDate = new Date(event.target.value + '-01');
  endDate1.value = selectedDate.toLocaleString('default', { month: 'long' }) + ' ' + selectedDate.getFullYear()
}

function getJobTitle2(value) {
  jobTitle2.value = value
}
function getCompany2(value) {
  company2.value = value
}
function getStartDate2 (event) {
  const selectedDate = new Date(event.target.value + '-01');
  startDate2.value = selectedDate.toLocaleString('default', { month: 'long' }) + ' ' + selectedDate.getFullYear()
}
function getEndDate2 (event) {
  const selectedDate = new Date(event.target.value + '-01');
  endDate2.value = selectedDate.toLocaleString('default', { month: 'long' }) + ' ' + selectedDate.getFullYear()
}

function getJobTitle3(value) {
  jobTitle3.value = value
}
function getCompany3(value) {
  company3.value = value
}
function getStartDate3 (event) {
  const selectedDate = new Date(event.target.value + '-01');
  startDate3.value = selectedDate.toLocaleString('default', { month: 'long' }) + ' ' + selectedDate.getFullYear()
}
function getEndDate3 (event) {
  const selectedDate = new Date(event.target.value + '-01');
  endDate3.value = selectedDate.toLocaleString('default', { month: 'long' }) + ' ' + selectedDate.getFullYear()
}

function getJobTitle4(value) {
  jobTitle4.value = value
}
function getCompany4(value) {
  company4.value = value
}
function getStartDate4 (event) {
  const selectedDate = new Date(event.target.value + '-01');
  startDate4.value = selectedDate.toLocaleString('default', { month: 'long' }) + ' ' + selectedDate.getFullYear()
}
function getEndDate4 (event) {
  const selectedDate = new Date(event.target.value + '-01');
  endDate4.value = selectedDate.toLocaleString('default', { month: 'long' }) + ' ' + selectedDate.getFullYear()
}

function getJobTitle5(value) {
  jobTitle5.value = value
}
function getCompany5(value) {
  company5.value = value
}
function getStartDate5 (event) {
  const selectedDate = new Date(event.target.value + '-01');
  startDate5.value = selectedDate.toLocaleString('default', { month: 'long' }) + ' ' + selectedDate.getFullYear()
}
function getEndDate5 (event) {
  const selectedDate = new Date(event.target.value + '-01');
  endDate5.value = selectedDate.toLocaleString('default', { month: 'long' }) + ' ' + selectedDate.getFullYear()
}

watch(() => content.value, (val) => {
  // console.log(val)
})

</script>