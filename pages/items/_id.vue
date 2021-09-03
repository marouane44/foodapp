<template>
    <div>
<pre>{{currentItem}}</pre>
    </div>
</template>

<script>
import { mapState } from 'vuex';


    export default {
        data(){
           return {
            id: this.$route.params.id
           };
        },
         computed: {
        ...mapState([
            'fooddata',
        ]),
        currentItem(){
            let results
            
                  for(let i=0;i< this.fooddata.length;i++){

                         for(let j=0;j< this.fooddata[i].menu.length;j++){
                             if(this.fooddata[i].menu[j].id===this.id){
                                 results =this.fooddata[i].menu[j];
                                 break;
                             }

                      
                      }

                  }
 

            return results
        }
    },
    }
</script>

<style lang="scss" scoped>

</style>