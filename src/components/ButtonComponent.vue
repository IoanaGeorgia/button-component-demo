<template>
  <span> 
  <button :class="buttonStyling">
<span v-if="startIcon" class="material-icons-outlined" :style="{'padding-right':'7px'}">
{{startIcon}}
</span>
  <slot>
  </slot>
  <span v-if="endIcon" class="material-icons-outlined" :style="{'padding-left':'7px'}">
{{endIcon}}
</span>
  </button>

  </span>
</template>

<script>
export default {
  name: 'ButtonComponent',
  props: {
        variant: {
            type: String,  //simple outline text
            default: "simple",
        },
        color:{ //default primary secondary danger
        type:String,
        default:'default'
        },
        disableShadow:{
          type:Boolean,
          default:false,
        },
        disabled:{
          type:Boolean,
          default:false,
        },
        startIcon:{ //send a string with the name of the icon
          type:String,
          default:false,
        },
        endIcon:{ //send a string with the name of the icon
          type:String, 
          required:false,
        },
        size:{ //sm md lg
          type:String,
          default:'md',
        }
  },
  computed:{
    buttonStyling(){
      let classes = ''
      let classesArray = []


      // adding the size class
      classesArray.push(this.size)


    // adding colors for the default variant
    if(this.variant == 'simple'){
       if(this.color ){
         classesArray.push( this.color)
       }
      }
        else{
         classesArray.push(this.variant)
       }


  // adding colors for the outline variant
      if(this.variant == 'outline'){
       if(this.color ){
         classesArray.push(this.color+'OutlineClass')
       }
       } else{
         classesArray.push(this.variant)
       }

  //adding colors for the text variant
      if(this.variant == 'text'){
       if(this.color ){
         classesArray.push(this.color+'Text')
       }
       } else{
         classesArray.push(this.variant)
       }

//adding a class to deal with incorporating an icon inside the button
if(this.startIcon || this.endIcon){
  classesArray.push('iconAdded')
}

// removing the box-shadow
if(this.disableShadow){
  classesArray.push('disableShadow')
}

      // adding the disabled class
    if(this.disabled){
      if(this.variant == 'text'){
        classesArray.push('disabledText')
      }
      else{
      classesArray.push('disabledClass')
    }}

      // joining all the classes in an array and then turning that array into a string
       classes= classesArray.join(' ')
       console.log(classes)
       return classes
    }

    
  }
}
</script>

<style scoped>

button{
  border-radius:6px;
border:none;
text-align: center;
font-size: 14px;
font-family: Noto Sans JP;
font-weight: 500;
box-shadow: 0px 2px 3px 0px rgba(0, 49, 202, 0.20);
color:#FFF;
padding-left:1em !important;
padding-right:1em !important;
}


/* class to remove the box shadow */
.disableShadow{
  box-shadow: 0px 0px;
}

/* classes for colors of the default button */
.default{
background: #E0E0E0;
color: #3F3F3F;
}

.primary{
background: #2962FF;
color:#FFF;

}
.secondary{
background: #455A64;
color:#FFF;
}
.danger{
background: #D32F2F;
color:#FFF;
}


/* classes for colors of the outline button */

.outline{
border: 1px solid #3D5AFE;
background:transparent;
color: #3D5AFE;
}

.defaultOutlineClass{
  border: 1px solid  #9E9E9E;
background:transparent;
color:  #9E9E9E;
}

.primaryOutlineClass{
  background: transparent;
  border: 1px solid #2962FF;
  color:  #2962FF;
}

.secondaryOutlineClass{
  background: transparent;
  border: 1px solid #455A64;
  color:  #455A64;
}

.dangerOutlineClass{
  background: transparent;
  border: 1px solid #D32F2F;
  color:  #D32F2F;
}

/* classes for colors of the text variant */
.defaultText{
  color:#3F3F3F;
  background:transparent;
  border:none;
  box-shadow:0px 0px;
}
.primaryText{
    color:  #2962FF;
  background:transparent;
  border:none;
  box-shadow:0px 0px;
}
.secondaryText{
  color:#455A64;
    background:transparent;
  border:none;
  box-shadow:0px 0px;
}
.dangerText{
  color:#D32F2F;
      background:transparent;
  border:none;
  box-shadow:0px 0px;
}


/* classes for sizes */
.sm{
min-width: 73px;
height: 32px;
}
.md{
min-width: 81px;
height: 36px;
}
.lg{
min-width: 93px;
height: 42px;
}

/* classes for the disabled button */
.disabledClass{
background: #E0E0E0; 
color: #9E9E9E;
border:1px solid #E0E0E0;
}
.disabledText{
  color:#9E9E9E;
  background:transparent;
  border:none;
}


/* handling the hover and focus effects */
button:hover{
  cursor:pointer;
}


/* handling the hover and focus effects for the simple variant */
.primary:hover, .primary:focus{
  background:#0039CB;
}
.secondary:hover, .secondary:focus{
  background:#1C313A;
}
.danger:hover, .danger:focus{
  background:#9A0007;
}
.default:hover, .default:focus{
  background:#AEAEAE;
}


/* handling the hover and focus effects for the outline variant*/
.primaryOutlineClass:hover, .primaryOutlineClass:focus{
  background:#2962FF1A;
}
.secondaryOutlineClass:hover, .secondaryOutlineClass:focus{
  background:#1C313A1A;
}
.dangerOutlineClass:hover, .dangerOutlineClass:focus{
  background:#D32F2F1A;
}
.defaultOutlineClass:hover, .defaultOutlineClass:focus{
  background:#AEAEAE1A;
}


/* handling the hover and focus effects for the text variant */
.primaryText:hover, .primaryText:focus{
  background:#2962FF1A;
}
.secondaryText:hover, .secondaryText:focus{
  background:#1C313A1A;
}
.dangerText:hover, .dangerText:focus{
  background:#D32F2F1A;
}
.defaultText:hover, .defaultText:focus{
  background:#AEAEAE1A;
}

/* class to deal with the addition of the icon */
.iconAdded{
  display:flex;
  align-items:center;
  justify-content:center;
  min-width:10em;
}
</style>
