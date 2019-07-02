<template>
  <v-card>
    <v-img :src="imgSrc" height="200px">
    </v-img>
    <v-card-title primary-title>
      <div>
        <div class="headline">{{title}}</div>
        <span id="truncate" class="grey--text">{{body}}</span>
      </div>
    </v-card-title>
  </v-card>
</template>

<style>
	#truncate {
		display:block;
		max-height: 100%;
		overflow: hidden;
		

		display: -webkit-box;
		-webkit-line-clamp : 3;
		-webkit-box-orient : vertical;
	}
	.headline{
		display:block;
		max-width: 100%;
		overflow: hidden;

		display: -webkit-box;
		-webkit-line-clamp : 1;
		-webkit-box-orient : vertical;

		
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

