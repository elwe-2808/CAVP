<template>
    <div class="page">
        <q-btn v-for="n in step_number" :key="n" class="button midd" round :color="check_color(n)" :label="n" size="8"/>
    </div>
</template>

<script>
    export default {
        name: "step-indicator",
        data(){
            return {
                default_color: "blue-9",
                current_color: "blue-5"
            }
        },
        methods: {
            check_color(button_number){
                if(this.current_page === button_number)
                    return "blue-5"
                else
                    return "blue-9"
            },
        },
        props: {
            current_page: Number,
            step_number: Number
        }
    }
</script>

<style scoped lang="scss">
    .page{
        .midd{
            margin: 2%;
        }
    }
</style>