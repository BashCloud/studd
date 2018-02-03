<template>
  <v-card class="Card elevation-7" >
    <v-expansion-panel expand focusable>
      <v-expansion-panel-content ripple :value="true">
        <div slot="header"> 
          <h3 class="cardHeading"> Major Projects: </h3>
        </div>
        <v-card>
          <v-list two-line dense>
            <div class="timeline"></div>
            <div class="exprItem" v-for="item in items" :key="item.title">
              <v-list-tile avatar >
                  <div class="exprIcon" v-html="item.key"></div>
                <v-list-tile-content style="padding-left:10px;">
                    <v-list-tile-title >
                      <div><span class="listTitle" v-html="item.title"> </span>
                      <span class="listTitle2" v-html="item.title2"> </span></div>
                      <span class="listDuration" v-html="item.duration"> </span>
                    </v-list-tile-title>
                  <v-list-tile-sub-title v-html="item.subtitle"></v-list-tile-sub-title>
                </v-list-tile-content>
              </v-list-tile>
            </div>
          </v-list>
        </v-card>
      </v-expansion-panel-content>
    </v-expansion-panel>
  </v-card>
</template>

<script>
  export default {
    data () {
      return {
        items: [
          {
            key: 'A',
            title: 'Cryptanalysis over OAuth’s Secret Key',
            title2: '| User Authentication | REST APIs | Azure Cloud',
            subtitle: 'A network security based cryptanalysis over the secret key of the Open Authentication protocol.',
            duration: "(2017 - Present)"
          },
          {
            key: 'B',
            title: 'DIGI-Suchna App',
            title2: '| PhoneGap | Framework7 | Firebase | Push Notifications',
            subtitle: 'A cross-platform mobile application aimed to direct all the official notices tothe student’s mobile synchronously.',
            duration: "(June 17 – Sept 17)"
          },
          {
            key: 'C',
            title: 'Project Kalpana (a.k.a Alfred)',
            title2: '| UWP | Voice Recognition | Voice Synthesis | Home Security',
            subtitle: 'A Universal Windows Application, build to do, what a user can Imagine andcan act as a smart personal assistance.',
            duration: " (2016 - Present)"
          },
          {
            key: 'D',
            title: 'Smart Car Parking System',
            title2: '| RFID | IR Sensor | Ultrasonic Sensor | L293D | Arduino',
            subtitle: 'A fully automated car parking solution that communicates with the autonomous cars, allocate a slot and track them meanwhile.',
            duration: "(2014 - 2016)"
          },
          {
            key: 'E',
            title: 'Sudoku Game',
            title2: '| Sudoku Solver | Debugger | Score Board| Synchronized State',
            subtitle: 'A C++ console based Sudoku Puzzle game, with minimal graphics.',
            duration: "(2012 - 2014)"
          },
          {
            key: '+',
            title: 'Add new'
          },
        ]
      }
    }
  }
</script>

<style>
.exprItem{
    cursor: pointer;
}
.exprItem:hover{
    background-color: #ddd;
}
.exprIcon{
    min-height: 24px;
    min-width: 24px;
    border-radius: 50%;
    background-color: #d92c64;
    color: #fff;
    text-align: center;
    line-height: 24px;
    margin: 5px;
    font-size: 14px;
}

</style>
