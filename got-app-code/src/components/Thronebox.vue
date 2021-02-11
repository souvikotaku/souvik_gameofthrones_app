<template>
<div class="App">  
    <div>
        <img  style="width:70%" src="https://logodix.com/logo/402867.png"/>
        <p style="color:white">Made by Souvik</p>
    </div>
<br/>

    <!-- <button @click='fetchData'>click</button> -->
    <div className="row shapeBox">
        
            <div
              v-for="post in thrones" 
               
              v-bind:key="post"
              style="width:20%;padding:6px"
              className='image-container d-flex justify-content-start'
            >
              <!-- <p>{{index}}. {{post.characterName}}</p> -->
              
             
              <img 
              class="picbox"
              style="width:100%"
              v-bind:src="post.characterImageFull"
              />
              <div className='overlay  '>
               
                <p style="color:white;font-size:15px">Name: {{post.characterName}}</p>
                <h5 style="color:white;font-size:15px">House: {{post.houseName || 'nil'}}</h5>
                <h5 style="color:white;font-size:15px">Nickname: {{post.nickname || 'nil'}}</h5>
                <h5 style="color:white;font-size:15px">Actor/Actress: {{post.actorName || 'nil'}}</h5>
               <!-- <button 
               className='btn btn-info'

               
               >More Info</button> -->
               
                </div>
            </div>
        
    </div>
 </div> 
</template>

<script>

// import {Card} from '@material-ui/core';

export default {


  name: 'Thronebox',
  props: {
    msg: String
  },
  data(){
      return {
        query: '',
        thrones: null,
        
      }
  },


  mounted: async function(){
      const url = `https://raw.githubusercontent.com/jeffreylancaster/game-of-thrones/master/data/characters.json`;
      const response2 = await fetch (url);
      const responseJson2 = await response2.json();
      console.log(responseJson2);

      this.thrones = responseJson2.characters

      
  },

  

  
}


</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>


@import '../assets/bootstrap.css';
@import './thronebox.css'




</style>
