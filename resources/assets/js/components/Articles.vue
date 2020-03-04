<template>
    <div class="container">
        <div>
            <h2>SCSS</h2>
            <p :class="$style.red">message：{{ message }}</p>
            <p :id="$style.gray">now (computed)：{{ now }}</p>
            <p>getNow (method)：{{ getNow() }}</p>
            <button @click="test">asdasd</button>
        </div>
    </div>
</template>

<style module>
    .red {
        color: red;
    }
    #gray{
        color: gray;
    }
</style>

<script>
    export default {
        data(){
            return{
                message:'123456'
            }
        },
        computed: {
            now: function() {
                return Date.now();
            }
        },
        methods: {
            getNow: function() {
                return Date.now();
            },
            test(){
                alert(123123);
            }
        }
    }
</script>
