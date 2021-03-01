<template>
    <div class="main">
        <div class="Connection-dialog">
            <h1>Connection</h1>
            <hr>
            <form>
                <q-input class="input" color="grey-3" label-color="black" outlined v-model="text" label="Identifiant">
                    <template v-slot:prepend>
                        <q-icon name="fas fa-user" color="black" />
                    </template>
                </q-input>

                <q-input class="input" color="grey-3" label-color="black" outlined v-model="password" label="Mot de passe" type="password">
                    <template v-slot:prepend>
                        <q-icon name="fas fa-unlock" color="black" />
                    </template>
                </q-input>

                <q-btn class="submit-button" color="blue-9" icon-right="fas fa-forward" label="Connection" />
                <p><a href="nothing">Mot de passe oublié</a></p>
            </form>

        </div>
    </div>
</template>

<script>
    export default {
        name: "connection"
    }
</script>

<style scoped lang="scss" >

    .main {
        background-color: rgba(165, 174, 182, 0.38);
        display: flex;
        justify-content: center; /* alignement vertical */
        height: 100vh;
        .Connection-dialog {
            display: flex;
            flex-direction: column;
            align-items: center;
            background-color: rgba(198, 219, 249, 0.82);

            border-radius: 20px;

            margin: auto;
            width: 30%;
            height: 40em;
            padding: 5px;

            -webkit-box-shadow: -12px 12px 45px -3px rgba(0,0,0,0.61);
            box-shadow: -12px 12px 45px -3px rgba(0,0,0,0.61);

            h1{
                display: inline;
                font-size: 50px;
            }

            hr{
                width: 70%;
                margin-top: -20px;
            }

            form{
                //background-color: red;
                width: 90%;
                margin-top: 50px;
                height: 70%;


                .input{
                    margin-left: auto;
                    margin-right: auto;
                    margin-bottom: 10%;
                    width: 100%;
                }

                .submit-button{
                    width: 100%;
                    margin-bottom: 5px;
                }

                @media screen and (max-width: 576px){
                    margin-top: 15vh;
                }

            }

            @media screen and (max-width: 1200px){
                width: 60%;
            }

            @media screen and (max-width: 576px){
                width: 100vh;
                height: 100%;
                border-radius: 0;
            }

        }
    }
</style>