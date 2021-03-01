<template>
    <div class="home">
        <h1>Ajout du bulletin</h1>

        <q-uploader
                class="uploader"
                url="http://localhost:4444/upload"
        />
    </div>
</template>

<script>
    export default {
        name: "adding_bulletin_step"
    }
</script>

<style scoped lang="scss">
    .home{
        .uploader{
            margin-top: 15px;
            margin-right: auto;
            margin-left: auto;
            width: 50%;
            height: 60%;
        }


    }




</style>