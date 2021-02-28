<template>
  <div class="home">
    <!--Step indicator-->
    <step class="step" :current_page=current_page :step_number=3></step>

    <!--Component for editing CAVP-->
    <bulletin_update class="action_section" v-if="this.current_page===1"></bulletin_update>
    <lesson_selection class="action_section" v-if="this.current_page===2"></lesson_selection>
    <notes_indication class="action_section" v-if="this.current_page===3"></notes_indication>

    <!--Navigation buttons-->
    <div class="navigation_buttons">
      <q-btn class="back_button" v-if="current_page>1" color="blue-9" icon="fas fa-backward" label="Précédent" @click="go_back"/>
      <q-btn class="next_button" v-if="current_page<3" color="blue-9" icon-right="fas fa-forward" label="Suivant" @click="go_next"/>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
import step from "../components/student_comp/step-indicator"
import adding_bulletin_step from "../components/student_comp/adding_bulletin_step";
import lesson_selection_step from "../components/student_comp/lesson_selection_step";
import notes_indication_step from "../components/student_comp/notes_indication_step";

export default {
  name: 'Home',
  components: {
    step,
    bulletin_update: adding_bulletin_step,
    lesson_selection: lesson_selection_step,
    notes_indication: notes_indication_step
  },
  data(){
    return{
      current_page: 1
    }
  },
  methods: {
    go_next(){
      if(this.current_page<3)
        this.current_page++
    },
    go_back(){
      if(this.current_page>1){
        this.current_page--
      }
    }
  }
}
</script>

<style lang="scss">
  .home{

  }
  .step{
    //background-color: yellow;
  }
  .action_section{
    margin-left: auto;
    margin-right: auto;
    margin-bottom: 30px;

    height: 30vw;
    width: 70%;

    background-color: #e5e5e5;

    h1{
      display: inline;
      font-size: 40px;
    }
  }
  .navigation_buttons{
    margin-right: auto;
    margin-left: auto;
    width: 80%;
      .back_button{
        position: fixed;
        left: 13%;
      }
      .next_button{
        position: fixed;
        right: 13%;
      }
  }
</style>