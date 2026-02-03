<template>
  <ul>
    <li v-for="country in countries" :key="country.id">{{ country.name }}</li>
  </ul>

  <h1>Teto Foods</h1>
  <food-item/>
  <food-item2/>
  <personal-profile/>
  <comment-form/>
  <comment/>


</template>

<script>
  import { ref, onMounted } from 'vue'
  import { supabase } from './lib/supabaseClient'

  const countries = ref([])

  async function getCountries() {
    const { data } = await supabase.from('countries').select()
    countries.value = data
  }

  onMounted(() => {
    getCountries()
  })
</script>