<script setup>
import '@/assets/css/style.css'
import Chart from '@/components/Chart.vue'
</script>

<template>
    <div class="card">
        <div class="card__top">
            <div class="card__top-left">
                <p>My balance</p>
                <h1>$921.48</h1>
            </div>
            <img src="@/assets/img/logo.svg">
        </div>
        <div class="card__bottom">
            <h1>Spending - Last 7 days</h1>
            <chart />
            <div class="card__bottom-wrapper">
                <div class="card__bottom-left">
                    <p>Total this month</p>
                    <h2>$478.33</h2>
                </div>
                <div class="card__bottom-right">
                    <h3>+2.4%</h3>
                    <p>from last month</p>
                </div>
            </div>
        </div>
    </div>
    <div class="attribution">
        Challenge by <a href="https://www.frontendmentor.io?ref=challenge" target="_blank">Frontend Mentor</a>. 
        Coded by <a href="https://MomboteQ.github.io">MomboteQ</a>.
    </div>
</template>