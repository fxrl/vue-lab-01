<template>
    <div v-on:click="increment" class="btn btn-primary">{{count}}</div>
</template>

<script>
export default {
    data() {
        return {
            count: this.startValue
        }
    },
    name: 'counter',
    props: {
        incSteps: Number,
        startValue: Number
    },
    methods: {
        increment() {
            this.count = this.count + this.incSteps;
        }
    }
}
</script>