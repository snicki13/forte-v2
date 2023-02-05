<script setup lang="ts">
import { Duration } from "luxon";
import Activity from "./Activity.vue";

const activities = [{
    name: "Activity 1",
    description: "This is the first activity",
    duration: Duration.fromObject({ minutes: 30 }),
    color: "var(--cyber-grape)",
},
{
    name: "Activity 2",
    description: "This is the second activity",
    duration: Duration.fromObject({ minutes: 60 }),
    color: "var(--dark-electric-blue)",
},
{
    name: "Activity 3",
    description: "This is the third activity",
    duration: Duration.fromObject({ minutes: 90 }),
    color: "var(--myrtle-green)",
},
{
    name: "Activity 4",
    description: "This is the fourth activity",
    duration: Duration.fromObject({ minutes: 120 }),
    color: "var(--viridian)",
},
{
    name: "Activity 5",
    description: "This is the fifth activity",
    duration: Duration.fromObject({ minutes: 150 }),
    color: "var(--illuminating-emerald)",
}
]
</script>

<template>
    <centered>
        <h1>Activities</h1>
    </centered>
    <div class="wrapper flow">
        <Activity v-for="activity in activities" :name="activity.name" :description="activity.description"
            :duration="activity.duration" :color="activity.color" />
    </div>

</template>

<style scoped>
.flow {
    display: flex;
    flex-flow: row wrap;
    justify-content: space-around;
}
</style>
