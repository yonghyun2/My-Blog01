<template>
<div>
  
    <v-toolbar fixed="true" v-resize="callback" v-if="flag>1">    
    <v-toolbar-side-icon>
      
    </v-toolbar-side-icon>
    <v-btn @click="movehome" flat><i class="fab fa-earlybirds fa-2x">YONGHYUN</i></v-btn>
    <v-spacer></v-spacer>  
  
    <v-toolbar-items>
      <v-btn flat @click="movePost">Post</v-btn>
      <v-btn flat @click="movePortfolio">Portfolio</v-btn>
      <v-btn flat @click="moveLogin">Login</v-btn>
    </v-toolbar-items>  
  </v-toolbar>

  
 
  <v-toolbar fixed="true" v-resize="callback" v-else>
     <v-toolbar-items class="all">   
        <v-btn class="btn" flat @click="movePost">Post</v-btn>
        <v-btn class="btn" flat @click="movePortfolio">Portfolio</v-btn>
        <v-btn class="btn" flat @click="moveLogin">Login</v-btn>
        
      </v-toolbar-items>  
  </v-toolbar> 
</div>
</template>

<style>
  @media (max-width:500px) {
    .btn{
      width: 33%
    }
    .all{
      width: 100%
    }

  }
  
</style>




<script>
export default {
    name : 'Header',
    components : {

    },
    data() {
      return {
        flag : 2,
        window:{
          width:0,
          height:0
        }    

      }
    },
     mounted(){
      this.callback();
    },
    methods : {
      movehome : function() {         
        this.$router.push('/');
      },
      movePost : function(){
        this.$router.push('/post');

      },
      movePortfolio : function(){
        this.$router.push('/portfolio');

      },
      moveLogin : function(){
        this.$router.push('/login');
      },
      callback : function() {
        this.width = window.innerWidth;
        this.height = window.innerHeight;
        console.log(this.width);

        if(this.width>500) {
          this.flag = 2;
        } else{
          this.flag = 0;
        }
        console.log(this.flag);


      }
    }
   
}
</script>