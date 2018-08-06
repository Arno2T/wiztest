<template>
    <div id='timer' :clock="clock()" :clockAgain="clockAgain()" :showTime="showTime()" :truc="truc" :chose="chose"> {{truc}} {{chose}}</div>
</template>

<script>
import * as moment from 'moment'
export default {
  name: 'Timer',
  data(){
      return{
          truc: null,
          chose: null,
      }
  },
  methods: {
    clock () {
      moment.locale('fr')
      let machin = moment().format('LLL')
      this.truc =machin
    },
    clockAgain(){
        let now= new Date()
        let d= now.getDay()
        let m= now.getMonth()
        let y= now.getFullYear()
        let h= now.getHours()
        let mm= now.getMinutes()
        let s= now.getSeconds()
        const jour=["dimanche","lundi","mardi","mercredi","jeudi","vendredi","samedi"]
        const mois=["Janvier","Février","Mars","Avril","Mai","Juin","Juillet","Août","Septembre","Octobre","Novembre","Décembre"]
        let compteur= jour[d] +" "+d+" "+mois[m]+" "+y+" "+h+":"+mm+":"+s
        //this.chose=setTimeout(compteur,500)
        console.log(compteur)
    },
    showTime(){
        setInterval(clockAgain, 1000)
    }

  }
}
</script>

<style lang="less">
#timer{
    font-weight:900;
}
</style>

