<template>
  <div class="py-3">
    <v-layout>

      <v-flex xs8>
        <h2 id="path" class="font-weight-regular">{{repos.path_with_namespace}}</h2>
        <p class="subheading mb-1 grey--text text--darken-1 font-weight-light">{{repos.namespace.name}}</p>
      </v-flex>

    </v-layout>
  </div>
</template>
<style>
	#path{
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
import GitlabService from '@/services/GitlabService'

export default {
	name: 'Repository',
	props: {
		repos: {type: null}
	},
	data() {
		return {
			stats: {}
		}
	},
  mounted() {
		this.drawStatGraph()
  },
	methods: {
		async drawStatGraph() {
			this.commits = await GitlabService.getCommits(this.repos.id)
		}
	}
}
</script>
