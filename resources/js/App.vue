<template>
    <div>
        <Header/>
        <Main/>
        <Footer/>
    </div>
</template>

<script>
import Header from './components/Header.vue';
import Main from './components/Main.vue';
import Footer from './components/Footer.vue'

export default {
    name : 'App',

    components : {
        Header,
        Main, 
        Footer
    },

    data() {
        return {
            posts : [] 
        }
    },

    created() {
        axios.get('http://localhost:8000/api/posts')

        axios.get('http://localhost:8000/api/posts')
            .then( response => {
                this.posts = response.data;
            })
    }
    
}
</script>

<style>

</style>