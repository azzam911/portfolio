<template>
    <div >
        <div class="main-div">
            <h2>Projects<span>ON</span>GitHub</h2>
        </div>
        
    </div>
    
        <div class="container">
            <div class="card" v-for="project in projects" :key="project.id">
                    <div class="card-body">
                        <h5 class="card-title">{{ project.name }}</h5>
                        <a :href=" project.html_url " class="btn btn-primary" target="_blank">Visit</a>
                        <a v-if="project.name === 'Anime-Search'" href="https://anime-search-pro.vercel.app/" class="btn btn-primary" target="_blank">WebSite</a>
                    </div>
            </div>
        </div>
    

</template>

<script>
import axios from "axios"
export default {
    name: "MyProjects",
    data() {
        return {
            projects: []
        }
    },
    created() {
        axios.get("https://api.github.com/users/azzam911/repos")
        .then(response => {
            this.projects = response.data;
            console.log(this.projects)
        })
    }
}
</script>

<style>
.main-div {
    margin: 40px auto;
}
.main-div h2 {
    color: #8b8b8b;
}
.main-div h2 span {
    color: #000;
    font-weight: 700;
}
.real-website {
    display: block;
}
.links {
    display: flex;
    justify-content: center;
    flex-direction: column;
    gap: 20px;
    align-items: center;
}



.project-name {
    font-size: 17px;
}

@media screen and (max-width: 500px) {
    .repos ul li {
        width: 180px;
    }
}

.container {
    display: flex;
    flex-wrap: wrap;
    margin: 100px auto;
}
.card-body {
    display: flex;
    flex-direction: column;
    justify-content: space-around;
    width: 180px;
}
.card {
    height: 200px !important;
    margin: 10px auto;
}

@media screen and (max-width: 400px) {
    .card-body {
    width: 150px;
}
}
</style>