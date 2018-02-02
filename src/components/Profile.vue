<template>
  <v-card color="grey lighten-4" flat>
    <v-toolbar dark id="profileBar" extended>
      <v-toolbar-side-icon></v-toolbar-side-icon>
          <img id="mainLogo" src="../assets/Studd_logo.png" />
          <v-spacer></v-spacer>
      <v-btn icon>
        <v-icon>more_vert</v-icon>
      </v-btn>
    </v-toolbar>
    <v-layout row>
      <v-flex sm8 xs10 offset-sm2 offset-xs1>
          <profile-heder /> 
            <v-layout row wrap>
                <v-flex xs12 md8>
                    
                    <profile-eduction />
                    <profile-experience />
                </v-flex>
                <v-flex xs12 md4>
                    <v-card class="Card elevation-7" >
                    <v-card-text style="height: 200px;"></v-card-text>
                    </v-card>
                </v-flex>
                
            </v-layout>
              
      </v-flex>
      
    </v-layout>
  </v-card>
</template>

<script>
import ProfileHeder from "./ProfileHeader";
import ProfileExperience from "./ProfileExperience";
import ProfileEduction from "./ProfileEduction";
export default {
    components:{
        ProfileHeder,ProfileExperience,ProfileEduction
    },
}
</script>

<style>
#profileBar{
    animation: colorchange 9s infinite;
    background-image: url(../assets/banner.png);
    background-size: contain;
    background-position: right;
    background-color: #d92c64;
    /* IE10+ */ 
/* background-image: -ms-radial-gradient(center bottom, ellipse farthest-corner, #F5C913 0%, #EB7B27 33%, #D92C64 100%); */

/* Mozilla Firefox */ 
/* background-image: -moz-radial-gradient(center bottom, ellipse farthest-corner, #F5C913 0%, #EB7B27 33%, #D92C64 100%); */

/* Opera */ 
/* background-image: -o-radial-gradient(center bottom, ellipse farthest-corner, #F5C913 0%, #EB7B27 33%, #D92C64 100%); */

/* Webkit (Safari/Chrome 10) */ 
/* background-image: -webkit-gradient(radial, center bottom, 0, center bottom, 359, color-stop(0, #F5C913), color-stop(33, #EB7B27), color-stop(100, #D92C64)); */

/* Webkit (Chrome 11+) */ 
/* background-image: -webkit-radial-gradient(center bottom, ellipse farthest-corner, #F5C913 0%, #EB7B27 33%, #D92C64 100%); */

/* W3C Markup */ 
/* background-image: radial-gradient(ellipse farthest-corner at center bottom, #F5C913 0%, #EB7B27 33%, #D92C64 100%); */

}
    @keyframes colorchange
    {
      0%   {background-color: #F5C913;}
      25%  {background-color: #EB7B27;}
      50%  {background-color: #d92c64;}
      75%  {background-color: #EB7B27;}
      100% {background-color: #F5C913;}
    }
  .toolbar__extension{
      height: 150px !important;
  }
  .Card .list{
      padding: 0px !important;
  }
  .Card .list__tile__title{
      font-weight: 600;
      color: #373737;
      display: flex;
    justify-content: space-between;
  }
  .Card{ 
      margin-top: 30px;
      border-left: 8px solid #d92c64;
      transition: 300ms all ease-in-out; 
  }
  .Card:hover{
      /* background-color: #d92c64; */
      border-left: 8px solid #EB7B27;
  }

  .cardHeading{
      color: #373737;
  }
  .listTitle2{
      font-weight: 300;
      padding-left: 10px;
  }
  .listDuration{
      /* background-color: #fff; */
    font-size: 10px;
    font-style: italic;
    padding: 0px 10px;
    /* position: absolute;
    right: 10px; */
    font-weight: 300;
  }

#mainLogo{
    height: 48px;
    position: absolute;
    left: calc( 50% - 55px);
    top: 20px;
}

.timeline{
    height: calc( 100% - 40px );
    border: 2px solid #d92c64;
    position: absolute;
    top: 20px;
    left: 31px;
    z-index: 0;
}
ul.expansion-panel{
    box-shadow: unset !important;
}
.expansion-panel__container{
    flex: initial !important;
    background-color: transparent !important;
    width: 100%;
}
@media only screen and (min-width: 960px) {
  .cardLeft{
      margin-right: 20px;
  }
}
</style>
