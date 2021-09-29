<template>
    <div class='root'>
        <div class='button' @click="btnClick(i)" :key="i" v-for="i in this.keypad">
            {{ i }}
        </div>
    </div>
</template>

<script>
    const component = {};

    function btnClick(i) {
        console.log(i);
        this.$emit('input-append', i);
    }

    component.name="Buttons";
    component.methods={
        btnClick
        };
    component.data = function() {
        return {
            keypad: []
        }
    }
    component.created = function() {
        for (let i = 1; i < 10; i++) {
            this.keypad.push(i);
        }
    }

    export default component;
</script>

<style scoped>
    .button {
        border-radius: 100%;
        background-color: aliceblue;
        padding: 15px;
        height: 30px;
        width: 30px;
        margin: 10px;
    }
    .root {
        display: flex;
        flex-direction: row;
    }
</style>