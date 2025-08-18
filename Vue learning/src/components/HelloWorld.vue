<script setup>    
    import TextInterpolation from './01-TextInterpolation.vue';
    import AttributeBinding from './02-AttributeBinding.vue';
    import Reactive from './03-Reactive.vue';
    import Ref from './04-Ref.vue';
    import Computed from './05-Computed.vue';
    import ConditionalRendering from './06-ConditionalRendering.vue';
    import vShow from './07-vShow.vue';
    import vFor from './08-vFor.vue';
    import Props from './09-Props.vue';

     // Example - 1 - dynamic-variables
    import { provide, ref } from 'vue';
    const firstName = ref('Muhammad');
    const lastName = ref('Nasir')
    // Example - 2 - dynamic-variables
    const val1 = ref(3 + 4);

    import dynamicProps from './10-dynamicProps.vue';
    import Slots from './11-Slots.vue';
    import FallbackContentSlots from './12-FallbackContentSlots.vue'
    import NamedSlot from './13-NamedSlot.vue'
    import ProvideInject from './14-ProvideInject.vue'

    // without provide inject variables
    const studentName = "Nasir";
    const studentAge = 44;
    const studentLocation = ["earth", "pakistan"]

    // using provide inject.
    provide('firstName', 'Nasir Khan')
    provide('age', 10)
    provide('location', ['pak', 'ind'])

    import vueWatchers from './15-vueWatchers.vue'

</script>



<template>
    <TextInterpolation />
    <AttributeBinding />
    <Reactive /> 
    <Ref />
    <Computed />
    <ConditionalRendering />
    <vShow />
    <vFor />
    <Props name="jordan"/>

    <!-- Example - 1 dynamic props-->
    <dynamicProps 
    :firstName = "firstName"
    :lastName = "lastName"
    :val = "val1"
    />

    <Slots>
        <h1>This is my content</h1>
        <h2>its coming from the parent component</h2>
    </Slots>

    <FallbackContentSlots></FallbackContentSlots>
    <NamedSlot>
        <template v-slot:one>
            <h1>{{2+2}}</h1>
        </template>

        <template v-slot:two>
            <h1>hi</h1>
        </template>
    </NamedSlot>
    
<!-- sending data from parent to child Provideinject -->
    <ProvideInject 
        :studentName = "studentName"
        :studentAge = "studentAge"
        :studentLocation = "studentLocation"
    />

    <vueWatchers />
</template>



<style scoped></style>
