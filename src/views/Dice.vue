<template>
    <div class="row">
        <div class="col-lg-6">
            <div class="card">
                <div class="card-header bg-dark text-white text-center">
                    <h4 class="display-3">{{diceValue}}</h4>
                </div>
            </div>
            <div class="badge badge-primary">
            </div>
            <!-- conditinal info -->
            <div v-if='diceValue <= 2' class="alert alert-success">That was low</div>
            <div v-else-if='diceValue > 2 && diceValue <= 4' class="alert alert-warning">That was average</div>
            <div v-else class="alert alert-danger">That was high</div>
            <div v-on:click='throwDice' class="btn btn-primary">Roll Dice</div>
        </div>
    </div>
</template>

<script>
export default {
    data() {
        const between1And6 = 1 + Math.floor(Math.random()*6);
        return {
            diceValue: between1And6
        }
    },
    methods: {
        throwDice() {
            this.diceValue = 1 + Math.floor(Math.random()*6);
        }
    }
}
</script>