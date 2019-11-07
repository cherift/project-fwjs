<template>
    <div class="flipper mb-3" ontouchstart="this.classList.toggle('hover');">
        <card-front :cat-url="catUrl" :cat-name="catName"/>
        <card-back :cat-name="catName" :cat-description="catDescription"/>    
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