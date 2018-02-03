<template>
  <v-card class="Card elevation-7" >
    <v-expansion-panel expand focusable>
      <v-expansion-panel-content ripple :value="true">
        <div slot="header"> 
          <h3 class="cardHeading"> Skills: </h3>
        </div>
        <v-card style="padding-bottom:20px;">
                <div class="skillItem" v-for="skill in skills" :key="skill.title">
                    <span class="skillTitle"> {{skill.title}} </span>
                    <v-progress-linear :value="skill.value" height="20" color="error"></v-progress-linear>
                </div>
        </v-card>
      </v-expansion-panel-content>
    </v-expansion-panel>
  </v-card>
</template>

<script>
  export default {
    data () {
      return {
        skills: [
          { title: 'CSS3', value: '85' },
          { title: 'Jvascript', value: '65' },
          { title: 'AngulrJS', value: '45' },
          { title: 'VueJS', value: '75' },
          { title: 'Php', value: '35' },
          { title: 'Bootstrap', value: '65' },          
          { title: 'HTML5', value: '95' },
        ]
      }
    }
  }
</script>

<style>
.skillItem{
  margin: 10px 20px 0px;
  cursor: pointer;
}
.skillTitle{
position: absolute;
z-index: 2;
color: #fff;
padding: 0px 10px;
font-size: 10px;
line-height: 20px;
font-weight: 500;
user-select: none;

}
.progress-linear{
    margin: 0px !important;
}
.progress-linear .error{
  background-color: #D92D63 !important;
}
</style>
