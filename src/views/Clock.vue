<template>
    <div class="row">
        <div class="col">
            <h1>The current time is</h1>
            <div class="alert alert-info">
                <h2 class='display-4'>
                    <span v-if='hours <= 9'>0</span>
                    {{hours}}
                    :
                    <span v-if='minutes <= 9'>0</span>
                    {{minutes}}
                    :
                    <span v-if='seconds <= 9'>0</span>
                    {{seconds}}
                </h2>
            </div>
        </div>
    </div>
</template>

<script>
import { setInterval } from 'timers';
export default {
    data() {
        const now = new Date();
        let hours = now.getHours();
        let minutes = now.getMinutes();
        let seconds = now.getSeconds();
        return {
            hours,
            minutes,
            seconds
        }
    },
    created() {
        var update = setInterval(this.updateTime, 1000);
    },
    destroyed() {
        clearInterval(update)
    },
    methods: {
        updateTime() {
            const nowToo = new Date();
            this.hours = nowToo.getHours();
            this.minutes = nowToo.getMinutes();
            this.seconds = nowToo.getSeconds();
        }
    }
}
</script>