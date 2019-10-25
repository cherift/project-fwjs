<template>
    <div class="front card text-center shadow-sm">
        <img class="card-img-top" :src="catUrl" alt="Cat image" width="250" height="200" />
        <div class="card-body">
            <h5 class="card-title"> {{ catName }}</h5>
        </div>
    </div>
</template>

<script>
    export default {
        name : "CardFront",
        props: {
            catUrl : String,
            catName : String
        }
    }
</script>