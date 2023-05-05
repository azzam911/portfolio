<template>
    <div class="repos">
        <div class="main-div">
            <h2>Projects<span>ON</span>GitHub</h2>
        </div>
        <ul>
            <li v-for="project in projects" :key="project.id">
                <p class="project-name">{{ project.name }}</p>
                <div class="links">
                        <a :href=" project.html_url " target="_blank">Visit</a>
                        <a class="real-website" v-if="project.name === 'Anime-Search'" href="https://anime-search-pro.vercel.app/" target="_blank">Show Website</a>
                </div>
            </li>
        </ul>
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
.repos {
    margin: 100px auto;
}
.repos ul {
    display: flex;
    flex-wrap: wrap;
    gap: 20px;
    justify-content: center;
}
.repos ul li {
    width: 200px;
    background-color: #eee;
    padding: 20px;
    border-radius: 10px;
    height: 200px;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    align-items: center;
    
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
.repos ul li a {
    color: #fff;
    background-color: #42b983;
    width: fit-content;
    padding: 5px 10px;
    border-radius: 5px;
    transition: .5s;
    text-decoration: none;
    
}
.repos ul li a:hover {
    transform: scale(1.1);
    color: #fff !important;
}

.project-name {
    font-size: 17px;
}
</style>