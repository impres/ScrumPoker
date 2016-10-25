<template>
    <div id="app">
        <card v-for="(color, value) in values" :value="value" :color="color"></card>
    </div>
</template>

<style>
    body {
        background-color: #E0E0E0;
    }

    #app {
        text-align: center;
    }
</style>

<script>
    import Card from "./components/Card.vue";

    export default {
        data() {
            return {
                values: {
                    "0": "#82b437",
                    "1/2": "#1ba21f",
                    "1": "#148e9c",
                    "2": "#193cab",
                    "3": "#252896",
                    "5": "#422795",
                    "8": "#c31077",
                    "13": "#db0e15",
                    "20": "#d97d09",
                    "40": "#d3a708",
                    "100": "#cfc108",
                    "?":"#c7cd07",
                    "BEER": "#c1c3af",
                    "ELMO": "#ff1515"
                }
            };
        },

        components: {
            Card
        }
    }
</script>
