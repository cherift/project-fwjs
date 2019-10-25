<template>
    <div class="flipper mb-3" ontouchstart="this.classList.toggle('hover');">
        <card-front catUrl="" catName=""/>
        <card-back catName="" catDescription=""/>    
    </div>
</template>

<script>
    import CardFront from './CardFront'
    import CardBack from './CardBack'

    export default {
        name: 'CardView',
        props: {
            catUrl: String,
            catName: String,
            catDescription: String
        },
        components: {
            CardFront,
            CardBack
        }
    }
</script>