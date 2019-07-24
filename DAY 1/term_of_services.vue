<template lang="pug">
  f7-page.theme-white.bg-custom-white(navbar-through, name='term_of_services')
    f7-navbar.navbar-v3
      f7-nav-left
      f7-nav-center(style='font-size: 17px;') Term of Services
      f7-nav-right
    div.container
      div.box
        h3 SYARAT DAN KETENTUAN
        h4 Definition
        ol
            li 
                b Client
                div Any individual or company or organization representation that creates survey in JAKPAT.
            li
                b Client
                div Any individual or company or organization representation that creates survey in JAKPAT.
            li
                b Client
                div Any individual or company or organization representation that creates survey in JAKPAT.
            li
                b Client
                div Any individual or company or organization representation that creates survey in JAKPAT.
        h4 Creating An Account in JAKPAT
        ol(type="A")  
            li To create a survey, client must create an account in JAKPAT through JAKPAT signup processes.
            li To create a survey, client must create an account in JAKPAT through JAKPAT signup processes.
            li To create a survey, client must create an account in JAKPAT through JAKPAT signup processes.
            li To create a survey, client must create an account in JAKPAT through JAKPAT signup processes.
        h4 Target Respondents and Respondent Management
        ol(type="a")
            li JAKPAT respondents has been profiled based on
            ol(type="I")
                li Basic demography profile
                li Basic demography profile
                li Basic demography profile
                li Basic demography profile
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
