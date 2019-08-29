<template>
    <div class="row">
        <div class="col-sm-12 col-md-4">
            <h2>Enter two Numbers</h2>
            <label for="number-1">Number #1</label>
            <input type="number" id="number-1" v-model.number="number1">
            <label for="number-2">Number #2</label>
            <input type="number" id="number-2" v-model.number="number2">
        </div>
        <div class="col-sm-12 col-md-8">
            <h2>Select an operator</h2>
           <input name="operator" type="radio" id="addNumber" value='+' v-model="operator"> 
           <label class='pl-2' for="addNumber">Add</label><br />
           <input name="operator" type="radio" id="subtractNumbers" value='-' v-model="operator"> 
            <label class='pl-2' for="subtractNumbers">Subtract</label><br />
           <input name="operator" type="radio" id="multiplyNumbers" value='*' v-model="operator"> 
            <label class='pl-2' for="multiplyNumbers">Multiply</label><br />
           <input name="operator" type="radio" id="divideNumbers" value='/' v-model="operator"> 
           <label class='pl-2' for="divideNumbers">Divide</label>
        </div>
        <div class="col">
            <div class="alert alert-info my-4 ">
                <p class='lead'>The result is
                {{result}} </p>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        data() {
            return {
                number1: 2,
                number2: 2,
                operator: null
            }
        },
        computed: {
            result() {
                switch(this.operator) {
                    case '+':
                    return this.number1 + this.number2;
                    case '-':
                    return this.number1 - this.number2;
                    case '/':
                    return this.number1 / this.number2;
                    case '*':
                    return this.number1 * this.number2;
                }
            }
        }
    }
</script>