<script setup lang="ts">
import { Duration } from "luxon";
import { reactive } from "vue";

const props = defineProps<{
    name: string;
    description: string;
    duration: Duration;
    color: string;
}>()

const styleObject = reactive({
    backgroundColor: props.color,
    width: '20rem'
})
</script>

<template>
    <div class="card">
        <div class="card-body" :style="styleObject">
            <h4 class="card-title">{{ props.name }}</h4>
            <p class="card-text"> {{ props.description }}</p>
            <span> {{ props.duration.minutes }}</span>
        </div>
    </div>
</template>
