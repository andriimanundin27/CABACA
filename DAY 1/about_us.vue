<template lang="pug">
  f7-page.theme-white.bg-custom-white(navbar-through, name='about_us')
    f7-navbar.navbar-v3
      f7-nav-left
      f7-nav-center(style='font-size: 17px;') About US
      f7-nav-right
    div.container
      div.box
        center
            img(src='assets/images/gurita-512.png')
        h2 About US
        p Cabaca adalah deskripsikan disini ...
        h4 Mengapa Cabaca?
        h3(class="warna") Keren, asikk, dll
        p Kami menampung blablabla deskripsi
        p Kami memiliki kelebihan
        ul  
            li KElebihan pertamaaaa ini yaaaaa
            li Kelebihan kedua <b> bro </b> hdhdhdh
            li To create a survey, client must create an account in JAKPAT through JAKPAT signup processes.
            li To create a survey, client must create an account in JAKPAT through JAKPAT signup processes.
        p ya itulah dia bro
    </template>

<script>
export default {
  name: 'privacy_policy',
  created(){
    self = this;
  }
}
</script>

<style scoped>
h3.warna{
    color: red;
}

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
