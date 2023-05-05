<template>
  <div class="w-full flex justify-center">
    <div class="w-[860px] bg-white py-14">
      <PersnoalDeatails />
      <ProfessionalSummary />
      <EmploymentHistory />
      <Education />
      <Skills />
    </div>
  </div>
</template>

<script setup>
import PersnoalDeatails from './PersnoalDeatails.vue'
import ProfessionalSummary from './ProfessionalSummary.vue'
import EmploymentHistory from './EmploymentHistory.vue'
import Education from './Education.vue'
import Skills from './Skills.vue'
</script>