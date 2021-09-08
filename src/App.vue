<template>
    <Line />
    <AreaStack />
    <BarSimple />
</template>

<script lang="ts">
import {defineComponent, ref} from 'vue';
import Line from './components/Line.vue';
import AreaStack from './components/AreaStack.vue';
import BarSimple from './components/BarSimple.vue';
export default defineComponent({
    name: 'App',
    components: {Line, AreaStack, BarSimple},
    setup() {},
});
</script>

<style></style>
