<template lang="pug">
  f7-page.theme-white.bg-custom-white(navbar-through, name='Ambil_Data')
    f7-navbar.navbar-v3
      f7-nav-left
      f7-nav-center(style='font-size: 17px;') Ambil Data
      f7-nav-right
    div.container(v-for='genre in genreCoy')
      div.box {{genre.id}} {{genre.title}}
    </template>

<script>
import config from '../config.js';
let self;
export default {
  name: 'coba',
  created(){
    self = this;
	},
	mounted(){
		self.ShowData();
	},
	data(){
		return{
			genreCoy:'',
			authHeaderLogin: {
        headers: {
            'X-DreamFactory-Session-Token': localStorage.getItem('session_token'),
            'X-Dreamfactory-API-Key': config.api_key_login
        }
      },
      authHeaderGuest: {
        headers: {            
            'X-Dreamfactory-API-Key': config.api_key            
        }
      }
		}
	},
  methods:{
		ShowData: async function(){
			try{
        const response = await config.HTTP.get('https://cabaca.id:8443/api/v2/cabaca/_table/genre', this.authHeaderLogin)
				const success = response.data;
				let obj=response.data.resource
				console.log(obj)
        if(!success){
          throw error
				}
				self.genreCoy=obj
			}catch(error){
				console.log(error);
			}
		}
  }
}
</script>

<style scoped>

img{
    width: 50%;
    height: 50%;
}

@media (max-width: 600px) {
    div.box{
        padding: 10px;
    }
    .container{
      width: 100%;
      align-items: center;
      justify-content: center;
    }
  }
  

  @media (max-width: 1024px) and (min-width: 601px) {
    .container{
      width: 75%;
      margin : auto;
      align-items: center;
      justify-content: center;
    }
  }

  @media (min-width: 1025px) {
    .container{
      width: 40%;
      margin : auto;
      align-items: center;
      justify-content: center;
    }
  }
</style>
