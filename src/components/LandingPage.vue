<template>
  <div>
  <h2>Buttons</h2>
  <h5 :style="{'color':'grey', 'font-style':'italic'}">Coded by Pascu Ioana-Georgia in Vue</h5>

        <div class="columnFlex">
  <p> {{`< ButtonComponent />`}} </p>
  <ButtonComponent> Click me </ButtonComponent>
  </div>
</div>

  <div class="columnFlex">
  <p> {{`< ButtonComponent :variant = "'simple'"/>`}} </p>

  <div class="flexRow">
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
  </div>


  <div class="columnFlex">
  <p> {{`< ButtonComponent :variant = "'outline'"/>`}} </p>

  <div class="flexRow">
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

  </div>
</div>

  <div class="columnFlex">
  <p> {{`< ButtonComponent :variant = "'text'"/>`}} </p>

  <div class="flexRow">
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

  </div>
</div>

  <div class="columnFlex">
  <div class="flexRow">
      <div>
  <p> {{`< ButtonComponent :variant="'simple'"  :color="'primary'" :size="'sm'" />`}} </p>
  <ButtonComponent :variant="'simple'" :color="'primary'" :size="'sm'"> Click me </ButtonComponent>
  </div>

      <div>
  <p> {{`< ButtonComponent :variant="'simple'"  :color="'secondary'" :size="'md'" />`}} </p>
  <ButtonComponent :variant="'simple'" :color="'secondary'" :size="'md'"> Click me </ButtonComponent>
  </div>

      <div>
  <p> {{`< ButtonComponent :variant="'outline'"  :color="'danger'" :size="'lg'"" />`}} </p>
  <ButtonComponent :variant="'outline'" :color="'danger'" :size="'lg'"> Click me </ButtonComponent>

</div>
</div>
</div>


      <div class="columnFlex">
  <p> {{`< ButtonComponent :variant="'outline'"  :color="'primary'" :endIcon="'shopping_cart'" />`}} </p>
  <ButtonComponent :variant="'outline'" :color="'danger'" :endIcon="'shopping_cart'"> Click me </ButtonComponent>

      <div class="columnFlex">
  <p> {{`< ButtonComponent :variant="'simple'"  :color="'primary'" :endIcon="'paid'" />`}} </p>
  <ButtonComponent :variant="'simple'" :color="'primary'" :endIcon="'paid'"> Click me </ButtonComponent>

      <div class="columnFlex">
  <p> {{`< ButtonComponent :variant="'simple'"  :color="'secondary'" :startIcon="'person'" />`}} </p>
  <ButtonComponent :variant="'simple'" :color="'secondary'" :startIcon="'person'"> Click me </ButtonComponent>

        <div class="columnFlex">
  <p> {{`< ButtonComponent :variant="'text'"  :color="'default'" :startIcon="'edit'" />`}} </p>
  <ButtonComponent :variant="'text'" :color="'default'" :startIcon="'edit'"> Click me </ButtonComponent>

      <div class="columnFlex">
  <p> {{`< ButtonComponent :variant="'primary'" disabledShadow />`}} </p>
  <ButtonComponent :variant="'primary'" disableShadow> Click me </ButtonComponent>
  </div>

<div class="columnFlex">
<div class="flexRow">
      <div>
  <p> {{`< ButtonComponent disabled />`}} </p>
  <ButtonComponent disabled> Click me </ButtonComponent>
  </div>

        <div>
  <p> {{`< ButtonComponent :variant="'text'" disabled />`}} </p>
  <ButtonComponent :variant="'text'" disabled> Click me </ButtonComponent>
  </div>
  </div>
  </div>
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
.flexRow{
  display:flex;
  justify-content:space-between;
  align-items:center;
  padding-top:1em;
  width:80%;
}
.columnFlex{
  display:flex;
  flex-direction:column;
  justify-content:space-between;
  align-items:center;
  width:100%;
  padding-top:3em;
}
.columnFlex > p{
  margin:0px;
  margin-bottom:1em;
}
.flexRow div p{
    margin:0px;
  margin-bottom:1em;
}
.flexRow div{
  display:grid;
  place-items:center;

}
body{
  margin-bottom:6em;
}
</style>
