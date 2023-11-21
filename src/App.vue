<script>
import {SparklineComponent,SparklineTooltip} from '@syncfusion/ej2-vue-charts';

export default{
 components :{
    'ejs-sparkline': SparklineComponent
  },
  data : function(){
    return{
      dataSource:[
        { month: 'January', value: 34},
        { month: 'February', value: 36 },
        { month: 'March', value: 32},
        { month: 'April', value:35 },
        { month: 'May', value: 40 },
        { month: 'June', value: 38 },
        { month: 'July', value: 33 },
        { month: 'August', value: 37 },
        { month: 'september', value: 34 },
        { month: 'October', value: 31},
        { month: 'November', value: 30 },
        { month: 'December', value: 28 }
      ],
      markerSettings: {
        visible:['All']
      },
      dataLabelSettings: {
        visible:['Start','End']
      },
      tooltipSettings:{
        visible:true
      }
    }
  },
  provide:{
    sparkline:[SparklineTooltip]
  } 
}
</script>

<template>
 <ejs-sparkline :dataSource="dataSource" xName="month" yName="value" 
 valueType="Category" height="150px" width="80px" type="Line" 
 :markerSettings="markerSettings" :dataLabelSettings="dataLabelSettings"
 :tooltipSettings="tooltipSettings"></ejs-sparkline>
</template>

<style>

</style>
