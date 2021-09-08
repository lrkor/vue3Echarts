<template>
    <Line />
</template>

<script lang="ts">
import {defineComponent, ref} from 'vue';
import HelloWorld from './components/HelloWorld.vue';
import Line from './components/Line.vue';
export default defineComponent({
    name: 'App',
    components: {Line, HelloWorld},
    setup() {
        const a = ref('111');

        return {
            a,
        };
    },
});
</script>

<style></style>
