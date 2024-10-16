<template>
    <div class="card text-left">
            <img 
                class="card-img-top"
                :src="ProItem.urlImage"
            />
        <div class="card-body">
            <h4 class="card-title">{{ ProItem.nameProduct }}</h4>
            <button class="btn btn-info" @click="hanldeSelect(ProItem)">
                Select
            </button>
        </div>
        <p>{{ user }}</p>
    </div>
</template>

<script>
    export default {
        methods: {

            hanldeSelect(ProItem){
                // console.log(ProItem);
                this.$emit("custom-handle-select",ProItem);
            },
        },
        inject: ["user"],
        props : {
            ProItem: {
                type : Object,
                required: true,
            },
        multipleType: {
            type: [String, Number],
            required: false,
            default: "Hello",
            validator(value){
                if (value.lenght > 3){
                    return true;
                }else{
                    return false;
                }
            },
        },
        },
    };
</script>
<style>

</style>