<template>
  <v-card class="Card elevation-7" >
    <v-expansion-panel expand focusable>
      <v-expansion-panel-content ripple>
        <div slot="header"> 
          <h3 class="cardHeading"> Awards & Honours: </h3>
        </div>
        <v-card>
        <v-list two-line dense>
           <v-list-tile class="exprItem" v-for="item in items" v-bind:key="item.title">
            <v-list-tile-content>
              <v-list-tile-title>{{ item.title }}</v-list-tile-title>
              <v-list-tile-sub-title>{{ item.subtitle }}</v-list-tile-sub-title>
            </v-list-tile-content>
            <v-list-tile-action>
              <v-btn icon ripple>
                <v-icon color="grey lighten-1">info</v-icon>
              </v-btn>
            </v-list-tile-action>
          </v-list-tile>
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
          { icon: 'folder', iconClass: 'grey lighten-1 white--text', title: 'Yuva Sampadak', subtitle: 'State Winner' },
          { icon: 'folder', iconClass: 'grey lighten-1 white--text', title: 'PIK-CELL-ART', subtitle: '1st Position' },
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
</style>
