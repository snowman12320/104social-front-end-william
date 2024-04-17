<template>
  <div class="h-full space-y-5 bg-gray-700 p-10">
    <p>Page: demo/DemoPage.vue</p>
    <Panel
      header="Overriden"
      :pt="{ title: 'text-xl font-mono text-red-500 font-bold' }"
      >Content</Panel
    >

    <div class="card flex justify-center">
      <Dropdown
        v-model="selectedCity"
        :options="cities"
        optionLabel="name"
        placeholder="Select a City"
        class="md:w-[10rem]"
      />
    </div>
  </div>
</template>

<script setup>
const selectedCity = ref()
const cities = ref([
  { name: 'New York', code: 'NY' },
  { name: 'Rome', code: 'RM' },
  { name: 'London', code: 'LDN' },
  { name: 'Istanbul', code: 'IST' },
  { name: 'Paris', code: 'PRS' }
])
</script>
