<template>
    <div class="back card text-center shadow-sm">
        <div class="card-body">
            <h6 class="card-subtitle mb-2 text-muted">{{ catName }}</h6>
            <p class="card-text">{{ catDescription }}</p>
        </div>
        <div class="card-footer">
            <button href="#" class="btn btn-primary card-link">Edit that cat</button>
        </div>
    </div>
</template>

<script>
    export default {
        name: "CardBack",
        props: {
            catName : String,
            catDescription : String
        }
    }
</script>