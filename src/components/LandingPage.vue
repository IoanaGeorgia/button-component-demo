<template>
  <div>
  <h2>Buttons</h2>
  <h5 :style="{'color':'grey', 'font-style':'italic'}">Coded by Pascu Ioana-Georgia in Vue</h5>


  <p class='subtitle'> {{`< ButtonComponent />`}} </p>
  <ButtonComponent> Click me </ButtonComponent>



  <p class='subtitle'> {{`< ButtonComponent :variant = "'simple'"/>`}} </p>
  <div>
  <p>{{`:color="'default'"`}}</p>
    <ButtonComponent :variant="'simple'" :color="'default'"> Click me </ButtonComponent>
  </div>
  
  <div>
  <p>{{`:color="'primary'"`}}</p>
    <ButtonComponent :variant="'simple'" :color="'primary'"> Click me </ButtonComponent>
  </div>

    <div>
  <p>{{`:color="'secondary'"`}}</p>
    <ButtonComponent :variant="'simple'" :color="'secondary'"> Click me </ButtonComponent>
  </div>

    <div>
  <p>{{`:color="'danger'"`}}</p>
    <ButtonComponent :variant="'simple'" :color="'danger'"> Click me </ButtonComponent>
  </div>

  </div>


  <p class='subtitle'> {{`< ButtonComponent :variant = "'outline'"/>`}} </p>

  <div>
  <p>{{`:color="'default'"`}}</p>
    <ButtonComponent :variant="'outline'" :color="'default'"> Click me </ButtonComponent>
  </div>
  
  <div>
  <p>{{`:color="'primary'"`}}</p>
    <ButtonComponent :variant="'outline'" :color="'primary'"> Click me </ButtonComponent>
  </div>

    <div>
  <p>{{`:color="'secondary'"`}}</p>
    <ButtonComponent :variant="'outline'" :color="'secondary'"> Click me </ButtonComponent>
  </div>

    <div>
  <p>{{`:color="'danger'"`}}</p>
    <ButtonComponent :variant="'outline'" :color="'danger'"> Click me </ButtonComponent>
  </div>


  <p class='subtitle'> {{`< ButtonComponent :variant = "'text'"/>`}} </p>

  <div>
  <p>{{`:color="'default'"`}}</p>
    <ButtonComponent :variant="'text'" :color="'default'"> Click me </ButtonComponent>
  </div>
  
  <div>
  <p>{{`:color="'primary'"`}}</p>
    <ButtonComponent :variant="'text'" :color="'primary'"> Click me </ButtonComponent>
  </div>

    <div>
  <p>{{`:color="'secondary'"`}}</p>
    <ButtonComponent :variant="'text'" :color="'secondary'"> Click me </ButtonComponent>
  </div>

    <div>
  <p>{{`:color="'danger'"`}}</p>
    <ButtonComponent :variant="'text'" :color="'danger'"> Click me </ButtonComponent>
  </div>

      <div>
  <p class='subtitle'> {{`< ButtonComponent :variant="'simple'"  :color="'primary'" :size="'sm'" />`}} </p>
  <ButtonComponent :variant="'simple'" :color="'primary'" :size="'sm'"> Click me </ButtonComponent>
  </div>

      <div>
  <p class='subtitle'> {{`< ButtonComponent :variant="'simple'"  :color="'secondary'" :size="'md'" />`}} </p>
  <ButtonComponent :variant="'simple'" :color="'secondary'" :size="'md'"> Click me </ButtonComponent>
  </div>

      <div>
  <p class='subtitle'> {{`< ButtonComponent :variant="'outline'"  :color="'danger'" :size="'lg'"" />`}} </p>
  <ButtonComponent :variant="'outline'" :color="'danger'" :size="'lg'"> Click me </ButtonComponent>

</div>


  <p class='subtitle'> {{`< ButtonComponent :variant="'outline'"  :color="'primary'" :endIcon="'shopping_cart'" />`}} </p>
  <ButtonComponent :variant="'outline'" :color="'danger'" :endIcon="'shopping_cart'"> Click me </ButtonComponent>

  <p class='subtitle'> {{`< ButtonComponent :variant="'simple'"  :color="'primary'" :endIcon="'paid'" />`}} </p>
  <ButtonComponent :variant="'simple'" :color="'primary'" :endIcon="'paid'"> Click me </ButtonComponent>


  <p class='subtitle'> {{`< ButtonComponent :variant="'simple'"  :color="'secondary'" :startIcon="'person'" />`}} </p>
  <ButtonComponent :variant="'simple'" :color="'secondary'" :startIcon="'person'"> Click me </ButtonComponent>

  <p class='subtitle'> {{`< ButtonComponent :variant="'text'"  :color="'default'" :startIcon="'edit'" />`}} </p>
  <ButtonComponent :variant="'text'" :color="'default'" :startIcon="'edit'"> Click me </ButtonComponent>

  <p class='subtitle'> {{`< ButtonComponent :variant="'primary'" disabledShadow />`}} </p>
  <ButtonComponent :variant="'primary'" disableShadow> Click me </ButtonComponent>


      <div>
  <p class='subtitle'> {{`< ButtonComponent disabled />`}} </p>
  <ButtonComponent disabled> Click me </ButtonComponent>
  </div>


  <div>
  <p class='subtitle'> {{`< ButtonComponent :variant="'text'" disabled />`}} </p>
  <ButtonComponent :variant="'text'" disabled> Click me </ButtonComponent>
  </div>
 
 <p class='specialPar'>Coding challenge done by Pascu Ioana for <a href='https://devchallenges.io/challenges/ohgVTyJCbm5OZyTB2gNY'>devChallenges -> Front End Developer Path</a></p>
 </div>
</template>

<script>
import ButtonComponent from './ButtonComponent.vue'
export default {
  name: 'LandingPage',
  components:{
    ButtonComponent
  },
}
</script>

<style>
.subtitle{
  font-weight:bold;
  margin-top:4em;
}
.specialPar{
  padding-top:3em;
  padding-bottom:1em;
}
body{
  padding:3em;
  padding-top:1em;
  padding-bottom:0px;
}
</style>
