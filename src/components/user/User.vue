<template>
    <div>
        <h1>The User Page</h1>
        <hr>
        <p>Loaded Id: {{id}} </p>
        <p>Message {{hello}} </p>
        <button @click="navigateToHome" class="btn btn-primary">Go to Home</button>
    </div>

</template>
<script>
    export default {
        data() {
            return {
                id: this.$route.params.id,
                hello: "I want meat"
            }
        },
        watch: {
            '$route'(to, from) {
                this.id = to.params.id
            }
        },
        methods: {
            navigateToHome() {
                this.$router.push('/');
            }
        }
    }
</script>

<style scoped>

</style>