<template>
  <div class="home"> 
    <div class="hero">

        <h1>{{title}}</h1>
        <h2>{{description}}</h2>

        <h4>{{date}}</h4>
        <button class="action-button">{{ctaText}}</button>
    </div>
    
  </div>
</template>

<script>

import NavLink from '../theme/NavLink'

export default {
    components: {NavLink},
    props: ["title", "image", "date", "actionLink", "ctaText", "description"],
    data () {
        return {
        }
    }
}
</script>