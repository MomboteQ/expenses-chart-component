<script setup>
import data from '@/assets/json/data.json'
</script>

<template>
    <div class="chart">
        <div class="chart__bar" v-for="item in data" :key="item" :style="[{ height: (item.amount / maxAmount) * 100 + '%' }, item.amount == maxAmount ? { background: 'hsl(186, 34%, 60%)' } : { background: 'hsl(10, 79%, 65%)' }]" :tooltip="'$' + item.amount">
        </div>
        <p class="chart__day" v-for="item in data" :key="item">{{ item.day }}</p>
    </div>
</template>

<script>
export default {
    data() {
        return {
            amounts: [],
            maxAmount: 0,
        }
    },
    created() {
        this.amounts = data.map(item => item.amount)

        const index = this.amounts.indexOf(Math.max(...this.amounts))

        this.maxAmount = this.amounts[index]
    }
}
</script>

<!--        <div class="chart__bar">
            <div class="chart__bar-fill"></div>
            <p>mon</p>
        </div>
        <div class="chart__bar">
            <div class="chart__bar-fill"></div>
            <p>tue</p>
        </div>
        <div class="chart__bar">
            <div class="chart__bar-fill"></div>
            <p>wed</p>
        </div>
        <div class="chart__bar">
            <div class="chart__bar-fill"></div>
            <p>thu</p>
        </div>
        <div class="chart__bar">
            <div class="chart__bar-fill"></div>
            <p>fri</p>
        </div>
        <div class="chart__bar">
            <div class="chart__bar-fill"></div>
            <p>sat</p>
        </div>
        <div class="chart__bar">
            <div class="chart__bar-fill"></div>
            <p>sun</p>
        </div> -->