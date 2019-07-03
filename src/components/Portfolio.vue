<template>
  <v-card>
    <v-img :src="imgSrc" height="200px">
    </v-img>
    <v-card-title primary-title>
      <div>
        <div id="head" class="headline">{{title}}</div>
        <span id="truncate" class="grey--text">{{body}}</span>
		<a href="#" id="favorite" title="즐겨찾기 등록">즐겨찾기</a>
      </div>
    </v-card-title>
  </v-card>
</template>

<style>
#truncate{
		display:inline-block;		
		white-space: nowrap;
		overflow: hidden;
		text-overflow: ellipsis;

		white-space:normal;
		line-height: 1.2;
		height:3.6em;
		text-align: left;
		word-wrap:break-word;
		display:-webkit-box;
		-webkit-line-clamp:3;
		-webkit-box-orient:vertical;
			
	}
	#head{
		display: inline-block;		
		white-space:nowrap;
		overflow:hidden;
		text-overflow: ellipsis;
		white-space:normal;
		line-height: 1.2;
		height:1.2em;
		text-align: left;
		word-wrap:break-word;
		display:-webkit-box;
		-webkit-line-clamp:1;
		-webkit-box-orient:vertical;
			
	}

</style>


<script>
export default {
	name: 'Portfolio',
	props: {
		date: {type: String},
		title: {type: String},
		body: {type: String},
		imgSrc: {type: String},
	},
	data() {
		return {
			//
		}
	}
}
</script>

<script>
	
</script>


