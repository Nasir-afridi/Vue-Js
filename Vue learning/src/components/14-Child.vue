<!-- 
   ye apny parent Provideinject sy data receive kry using props
   yane grandparent nyy apny child ko diya pher os child nyy apny child ko diya. 
-->

   <script setup>
      // Example-1 without using provide and inject
        defineProps([
            'studentName',
            'studentAge', 
            'studentLocation'
        ])

      // Example-2 using provide and inject
      import { inject } from 'vue';
      const name = inject('firstName')
      const age = inject('age')
      const location = inject('location')
   </script>

 <template>
   <!-- Example-1 without using provide and inject -->
    <h1>{{ studentName }}</h1>
    <h2>{{ studentAge }}</h2>
    <h3>{{ studentLocation }}</h3>

    <!-- Example-2 using provide and inject -->
    <h1>{{ name }}</h1>
    <h2>{{ age }}</h2>
    <h3>{{ location }}</h3>
 </template>

 <style scoped></style>