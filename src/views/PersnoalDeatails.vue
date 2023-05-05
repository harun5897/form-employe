<template>
  <div class="form-employe ">
    <div class="px-14 grid grid-cols-2 items-end gap-10">
      <div>
        <p class="font-bold text-[18px] text-[#323A46]">Personal Details</p>
        <p class="mt-3 mb-[6px] text-sm text-[#8e929e]">Wanted Job Title</p>
        <Input type="text" />
      </div>
      <div class="input-file flex items-center">
        <div class="bg-[#F0F2F9] w-[60px] px-2 py-1 rounded">
          <img src="../assets/user.png" width="45" alt="">
        </div>
        <label for="upload" class="cursor-pointer">
          <span class="text-blue-400 text-sm ml-5">Upload photo</span>
          <input id="upload" type="file" class="hidden" />
        </label>
      </div>
    </div>
    <div class="px-14 grid grid-cols-2 items-end gap-10">
      <div>
        <p class="mt-5 mb-[6px] text-sm text-[#8e929e]">First Name</p>
        <Input type="text" />
      </div>
      <div>
        <p class="mt-3 mb-[6px] text-sm text-[#8e929e]">Last Name</p>
        <Input type="text" />
      </div>
    </div>
    <div class="px-14 grid grid-cols-2 items-end gap-10">
      <div>
        <p class="mt-5 mb-[6px] text-sm text-[#8e929e]">Email</p>
        <Input type="email" />
      </div>
      <div>
        <p class="mt-3 mb-[6px] text-sm text-[#8e929e]">Phone</p>
        <Input type="number" />
      </div>
    </div>
    <div class="px-14 grid grid-cols-2 items-end gap-10">
      <div>
        <p class="mt-5 mb-[6px] text-sm text-[#8e929e]">Address</p>
        <Input type="text" />
      </div>
      <div>
        <p class="mt-3 mb-[6px] text-sm text-[#8e929e]">Postal Code</p>
        <Input type="number" />
      </div>
    </div>
    <div class="px-14 grid grid-cols-2 items-end gap-10">
      <div>
        <p class="mt-5 mb-[6px] text-sm text-[#8e929e]">Driving License</p>
        <Input type="text" />
      </div>
      <div>
        <p class="mt-3 mb-[6px] text-sm text-[#8e929e]">Nationality</p>
        <Input type="text" />
      </div>
    </div>
    <div class="px-14 grid grid-cols-2 items-end gap-10">
      <div>
        <p class="mt-5 mb-[6px] text-sm text-[#8e929e]">Place Of Birth</p>
        <Input type="text" />
      </div>
      <div>
        <p class="mt-3 mb-[6px] text-sm text-[#8e929e]">Date Of Birth</p>
        <input 
          type="text" 
          placeholder="MM/DD/YYYY"
          onfocus="(this.type='date')"
          onblur="(this.type='text')"
          class="h-[45px] bg-[#F0F2F9] w-full rounded-sm focus:outline-none px-4 font-[400] text-base text-[#323A46]"
        >
      </div>
    </div>
  </div>
</template>

<script setup>
import Input from '@/components/input/Input.vue'
</script>