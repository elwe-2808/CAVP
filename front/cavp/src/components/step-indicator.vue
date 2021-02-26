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
                default_color: "yellow-9",
                current_color: "yellow-5"
            }
        },
        methods: {
            check_color(button_number){
                if(this.current_page === button_number)
                    return "yellow-9"
                else
                    return "yellow-5"
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