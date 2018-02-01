<template>
    <v-card class="Card elevation-7 cardLeft" >
        <v-card-text>
            <h3 class="cardHeading"> EXPERIENCE: </h3>
        </v-card-text>
        <v-list two-line dense>
          <div class="exprItem" v-for="item in items" :key="item.title">
            <v-list-tile avatar >
                <div class="exprIcon" v-html="item.key"></div>
              <v-list-tile-content style="padding-left:10px;">
                <v-list-tile-title v-html="item.title"></v-list-tile-title>
                <v-list-tile-sub-title v-html="item.subtitle"></v-list-tile-sub-title>
              </v-list-tile-content>
            </v-list-tile>
          </div>
        </v-list>
        
    </v-card>
</template>

<script>
  export default {
    data () {
      return {
        items: [
          {
            key: 'A',
            title: 'B.Tech. CSE',
            subtitle: 'Jaypee University of Information Technology, Waknaghat'
          },
          {
            key: 'B',
            title: 'Intermediate ',
            subtitle: 'Anand Swaroop Arya Saraswati Vidya Mandir, Roorkee'
          },
          {
            key: 'C',
            title: 'High School',
            subtitle: 'Anand Swaroop Arya Saraswati Vidya Mandir, Roorkee'
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
    background-color: #eee;
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
