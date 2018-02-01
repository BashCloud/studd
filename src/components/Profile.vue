<template>
  <v-card color="grey lighten-5" flat>
    <v-toolbar dark id="profileBar" extended>
      <v-toolbar-side-icon></v-toolbar-side-icon>
    </v-toolbar>
    <v-layout row>
      <v-flex sm8 xs10 offset-sm2 offset-xs1>
        <v-card class="card--flex-toolbar elevation-7" >
          
          <v-card-text>
              <v-layout row wrap>
            <v-flex md8 xs12>
            <v-avatar size="120px" class="elevation-5">
             <img id="userPic" src="../assets/user.png" class="elevation-5" alt="Pulkit">
            </v-avatar>
            <div class="userMains">
            <h1> Pulkit Aggarwal </h1>
            <p> Full-stack Developer | UX-UI Designer </p>
            </div>
             </v-flex>
             <v-flex md4 xs12>
                <v-list dense>
                    <v-list-tile v-for="info in infos" :key="info.title">
                        <v-list-tile-action>
                            <i class="material-icons">{{ info.icon }}</i>
                        </v-list-tile-action>
                        <v-list-tile-content>
                        <v-list-tile-title>{{ info.title }}</v-list-tile-title>
                        </v-list-tile-content>
                    </v-list-tile>
                </v-list>
             </v-flex>
                </v-layout>
          </v-card-text>
        </v-card>
        
        <v-card class="Card elevation-7" >
          <v-card-text style="height: 400px;"></v-card-text>
        </v-card>
      </v-flex>
    </v-layout>
  </v-card>
</template>

<script>
export default {
    data () {
      return {
        infos: [
          { title: 'Pulkit.cloud@gmail.com', icon: 'mail_outline' },
          { title: '+91-9817225332', icon: 'phone' },
          { title: '138-C, Subhash Nagar, Roorkee', icon: 'location_on' }
        ]
      }
    }
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
  .card--flex-toolbar {
    margin-top: -100px;
  }
  .toolbar__extension{
      height: 150px !important;
  }
  .Card{
      margin-top: 40px;
  }
  .avatar{
      margin: 8px;
      cursor: pointer;
  }
.userMains{
    display: inline-block;
    vertical-align: bottom;
    padding-left: 20px;
    color: #575757;
}
.list__tile__action{
    min-width: 36px !important;
}
</style>
