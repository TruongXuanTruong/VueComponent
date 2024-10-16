<template>
    <h2>First Component</h2>
    <p>{{ message }}</p>
    <LocalComponent />
</template>


<script>
    import LocalComponent from './LocalComponent.vue'
    export default {
        data(){
            return {
                message: "Đây là component thứ 2",
            };
        },
        components: {
            LocalComponent,
        }
    };
</script>

<style></style>