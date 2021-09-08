<template>
    <div class="map" id="barSimple">line</div>
</template>

<script lang="ts">
import {defineComponent, ref, onMounted} from 'vue';
import * as echarts from 'echarts';
export default defineComponent({
    name: 'BarSimple',
    setup() {
        const initEcharts = () => {
            const myChart = echarts.init(document.getElementById('barSimple'));
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
                        data: [120, 200, 150, 80, 70, 110, 130],
                        type: 'bar',
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
.map {
    width: 800px;
    height: 500px;
}
</style>
