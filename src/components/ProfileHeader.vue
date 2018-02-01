<template>
    <v-card class="card0 elevation-7" >    
        <v-card-text>
            <v-layout row wrap>
        <v-flex md8 xs12>
        <v-avatar size="120px" class="elevation-5">
            <img src="../assets/user.png" class="elevation-5" alt="Pulkit">
        </v-avatar>
        <div class="userMains">
        <h1> Pulkit Aggarwal </h1>
        <p> Full-stack Developer | UX-UI Designer </p>
        </div>
            </v-flex>
            <v-flex md4 xs12 style="color:#575757;">
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
        <div class="userRank" title="Studd Rank"> # 524 </div>
    </v-card>
</template>

<script>
export default {
    data () {
      return {
        infos: [
          { title: '+91-9817225332', icon: 'phone' },
          { title: 'BashCloud.github.io/', icon: 'http' },
          { title: 'Pulkit.cloud@gmail.com', icon: 'mail_outline' },
          { title: '138-C, Subhash Nagar, Roorkee', icon: 'location_on' }
        ]
      }
    }
}
</script>

<style>
  .card0 {
    margin-top: -100px;
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
.userRank{
    position: absolute;
    bottom: 0px;
    right: 0px;
    background-color: #d92c64;
    padding: 8px 20px 5px;
    text-align: center;
    color: #fff;
    cursor: pointer;
    border-radius: 20px 0px 0px;
    transition: 500ms all ease-in-out;
    font-weight: 700;
    user-select: none;
}
.userRank:hover{
    background-color: #EB7B27;
}
.list__tile{
    color: #797979 !important;
    height: 28px !important;
    user-select: text !important;
}
@media only screen and (max-width: 650px) {
    .avatar{
        margin-left: calc( 50% - 60px);
    }    
    .userMains{
        width: 100%;
        text-align: center;
    }
}
</style>
