<template>
    <footer class="bg-light">
        <div class="container text-center">
        <i class="far fa-copyright mr-1"></i><label> {{ year }} - {{ universityName }}</label>
        <span class="small font-italic infos"> {{ footerMessage }} </span>
        </div>
    </footer>    
</template>


<script>
export default {
    name: 'Footer',
    props: {
        year: Number,
        universityName: String,
        footerMessage: String
    }
}
</script>