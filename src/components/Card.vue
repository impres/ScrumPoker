<template>
    <div class="card">
        <span class="card__background" :style="style">
            <span class="card__value">
                <template v-if="value == 'ELMO'">
                    <img src="/assets/elmo.png">
                </template>
                <template v-else>
                    {{ value }}
                </template>
            </span>
        </span>
    </div>
</template>

<style lang="sass">
    .card {
        display: inline-block;
        margin: 15px;
        box-sizing: border-box;
        position: relative;
        width: 11%;
        border-radius: 15px;
        background-color: white;
        padding: 10px;
        transition: all .2s;
        user-select: none;
    }

    .card::before {
        display: inline-block;
        content: '';
        padding-top: 160%;
    }

    .card:hover {
        transform: scale(1.1, 1.1);
    }

    .card__background {
        position: absolute;
        top: 10px;
        right: 10px;
        bottom: 10px;
        left: 10px;
        border-radius: 15px;
    }

    .card__value {
        display: block;
        width: 100%;
        position: absolute;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%);
        color: white;
        font-size: 72px;

        img {
            width: 80%;
        }
    }
</style>

<script>
    var me = {
        name: "Lorey",
        occupation: "Life",
        interests: ["Creating"]
    };

    export default {
        props: {
            'value': {
                type: String,
                default: ""
            },
            'color': {
                type: String,
                default: ""
            }
        },

        mounted() {
            console.log(this.color);
        },

        computed: {
            style() {
                return {
                    'background-color': this.color
                }
            }
        }
    }
</script>
