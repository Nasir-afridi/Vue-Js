<!-- ismein ham grand parent syyy direct child ko data bhaij skty hain yane parent kk child kk child ko direct -->
 <script setup>
    import Child from './14-Child.vue'
    defineProps([
        'studentName',
        'studentAge', 
        'studentLocation'

    ])
</script>

 <template>
    <Child 
        :studentName = "studentName"
        :studentAge = "studentAge"
        :studentLocation = "studentLocation"
    />
 </template>

 <style scoped></style>