<template>
    <WaterLevel />
    <Line />
    <AreaStack />
    <BarSimple />
    <Map />
</template>

<script lang="ts">
import {defineComponent, ref} from 'vue';
import Line from './components/Line.vue';
import AreaStack from './components/AreaStack.vue';
import BarSimple from './components/BarSimple.vue';
import WaterLevel from './components/WaterLevel.vue';
import Map from './components/Map.vue';
export default defineComponent({
    name: 'App',
    components: {Line, AreaStack, BarSimple, WaterLevel, Map},
    setup() {},
});
</script>

<style></style>
