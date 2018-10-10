<template>
    <div id="hero" :style="{'background-image': 'url(' + bgImage + ')'} ">

        <div class="container">
            <h1>{{title}}</h1>
            <h2>{{description}}</h2>

            <h4>{{date}}</h4>
            <a :href="ctaLink" target="_blank" class="action-button">{{ctaText}}</a>
        </div>

    </div>
</template>

<script>

import NavLink from '../theme/NavLink'

export default {
    components: {NavLink},
    props: ["title", "image", "date", "actionLink", "ctaText","ctaLink", "description", "bgImage"],
    data () {
        return {
        }
    }
}
</script>