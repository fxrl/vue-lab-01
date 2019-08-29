<template>
    <div class="row">
        <div class="col">
            <counter v-bind:start-value="0" v-bind:inc-steps="1"></counter>
        </div>
        <div class="col">
            <counter v-bind:start-value="45" v-bind:inc-steps="5"></counter>
        </div>
        <div class="col">
            <counter v-bind:start-value="33" v-bind:inc-steps="10"></counter>
        </div>
    </div>
</template>

<script>
import Counter from '../components/Counter.vue';
export default {
    components: {
        Counter
    }
}
</script>