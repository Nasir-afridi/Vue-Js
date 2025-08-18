   <!-- ye apny parent Provideinject sy data receive kry using props
    yane grandparent nyy apny child ko diya pher os child nyy apny child ko diya. -->
   <script setup>
        defineProps([
            'studentName',
            'studentAge', 
            'studentLocation'

        ])
    </script>

 <template>
    <h1>{{ studentName }}</h1>
    <h2>{{ studentAge }}</h2>
    <h3>{{ studentLocation }}</h3>
 </template>

 <style scoped></style>