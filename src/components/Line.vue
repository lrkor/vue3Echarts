<template>
    <div class="line" id="line">line</div>
</template>

<script lang="ts">
import {defineComponent, ref, onMounted} from 'vue';
import * as echarts from 'echarts';
export default defineComponent({
    name: 'Line',
    setup() {
        const initEcharts = () => {
            const myChart = echarts.init(document.getElementById('line'));
            const option = {
                xAxis: {
                    type: 'category',
                    data: ['Mon', 'Tue', 'Wed', 'Thu', 'Fri', 'Sat', 'Sun'],
                },
                yAxis: {
                    type: 'value',
                },
                series: [
                    {
                        data: [150, 230, 224, 218, 135, 147, 260],
                        type: 'line',
                    },
                ],
            };

            myChart.setOption(option);
        };

        onMounted(() => {
            initEcharts();
        });

        return {
            initEcharts,
        };
    },
});
</script>

<style scoped>
.line {
    width: 800px;
    height: 500px;
}
</style>
