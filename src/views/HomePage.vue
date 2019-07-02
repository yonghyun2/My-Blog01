<template>
  <div>
    <ImgBanner imgSrc="https://source.unsplash.com/random/1600x900">
      <div style="line-height:1.2em;" slot="text">Slow and Steady<br> Win the Race.</div>
    </ImgBanner>
    <v-container>
      <!-- About Me -->
      <v-layout my-5>
        <v-flex id="aboutme" xs8>
          <h2 class="headline mb-3" id="about">About Me</h2>
          <p class="mr-4" id="me">안녕하세요, 저는 SSAFY1기 정용현입니다.<br/>저의 목표는 경쟁력을 갖춘 웹개발자가 되는 것입니다. 프론트 뿐만 아니라 백엔드,서버까지 개발할수 있는
           Full-Stack개발자가 되도록 열심히 하겠습니다.</p>            
        </v-flex>
        <v-flex hidden-xs-only>
          <v-img :src="getImgUrl('myprofile.jpg')" aspect-ratio="1"/>
        </v-flex>
      </v-layout>

      <!-- Portfolio -->
      <v-layout my-5>
        <v-flex xs12>
          <h2 class="headline my-5 text-xs-center"><router-link to="/portfolio"><i class="fab fa-blogger fa-2x">Portfolio</i></router-link></h2>
          <hr>
          <PortfolioList></PortfolioList>
        </v-flex>
      </v-layout>

      <!-- Post -->
      <v-layout my-5>
        <v-flex xs12>
          <h2 class="headline my-5 text-xs-center"><i class="fab fa-angellist fa-2x">Post</i></h2>     
          <hr>
          <PostList :column="2"></PostList>
        </v-flex>
      </v-layout>


      <!-- Github -->
      <v-layout my-5>
        <v-flex xs12>
          <h2 class="headline my-5 text-xs-center"><i class="fas fa-copy fa-2x">Project</i></h2>
          <RepositoryList></RepositoryList>
        </v-flex>
      </v-layout>
    </v-container>
  </div>
</template>

<style>  
    @media (max-width:500px) {
      #about, #me{
        text-align: center;
      }
      #aboutme{
        margin: 0 auto;
      }
  }

  @media (min-width:960px) {
    body{
      font-size: 25px;
    }

  }
  @media(max-width:959px) and (min-width:600px) {
    body{
      font-size :20px;
    }
  }
  @media (max-width:599px) {
    body{
      font-size:15px;
    }
    
  }
  @media (max-width:500px) {


  }
</style>


<script>
import ImgBanner from '../components/ImgBanner'
import PortfolioList from '../components/PortfolioList'
import PostList from '../components/PostList'
import RepositoryList from '../components/RepositoryList'

export default {
	name: 'HomePage',
	components: {
		ImgBanner,
		PortfolioList,
		PostList,
		RepositoryList
	},
	methods: {
		getImgUrl(img) {
			return require('../assets/' + img)
		}
	},
}
</script>
