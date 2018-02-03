<template>
  <v-card class="Card elevation-7 cardLeft" >
    <v-expansion-panel expand focusable>
      <v-expansion-panel-content ripple>
        <div slot="header"> 
          <h3 class="cardHeading"> Volunteer Experience: </h3>
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
            title: 'T.I.E. Development Cell',
            title2: '| Cordintor',
            subtitle: 'Jaypee University of Information Technology, Waknaghat',
            duration: "(April 17 – Present)"
          },
          {
            key: 'B',
            title: 'Microsoft Student Partner',
            title2: '| Reagional Head',
            subtitle: 'Microsoft India Pvt. Ltd.',
            duration: "(Dec 15 – Present)"
          },
          {
            key: 'C',
            title: 'IEEE JUIT Student Branch',
            title2: '| Web-master',
            subtitle: 'Jaypee University of Information Technology, Waknaghat',
            duration: "(Sept 16 – June 17)"
          }
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
