<template>
    <div class="row">
        <div class="col" v-on:click="showAnswer(index)" v-for="(element, index) in questions" v-bind:key='index' >
            <div class="card">
                <div class="card-header">
                    <a href="#">{{element.question}}</a>
                </div>
                <div class="card-body" v-if='element.showAnswer'>
                    {{element.answer}}
                </div>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        data() {
            return {
                questions: [
                    {
                        question: 'Is this a question?',
                        answer: 'Yes, it is!',
                        showAnswer: false
                    },
                    {
                        question: 'Is this another question?',
                        answer: 'Also true, it is!',
                        showAnswer: false
                    }
                ]
            }  
        },
        methods: {
            showAnswer(index) {
                this.questions[index].showAnswer = !this.questions[index].showAnswer;
            }
        }
    }
</script>