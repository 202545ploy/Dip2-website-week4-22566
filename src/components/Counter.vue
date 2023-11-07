<script>
export default {
    name:'CounTer',
    data() {
        return {
            Counter:0
        }
    },
    methods: {
        submiFrom(event) {
            // prevent a page refresh
            event.preventDefault();
            alert('The from was sumitted')
        },
        countUp() {
            this.Counter++   //this.Counter = this.Counter + 1
        },
        countDown() {
            this.Counter--   //this.Counter = this.Counter - 1
        }
    }
}
</script>

<template>
    <div>
        <h1>{{ Counter }}</h1>
        <span>
            <button @click.right="countUp">Counter UP</button>
            <button @click.middle="countDown">Counter Down</button>
        </span>
         
    </div>
    <from @submit.prevent="submiFrom">
        <p>
            <button>Submit</button>
        </p>
    </from>
</template>

<style lang="scss" scoped>

</style>