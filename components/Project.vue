<template>
    <div id="projects">
        <div id="projContainer">
            
            <div v-for="(project, index) in projects" :key="index" :id=id_name+index class="img">
                <h1>{{ project.title }}</h1>
                <img :src="require('../assets/images/'+languages[index]+'.jpg')" alt="image">
                 <h3 v-html="project.description"></h3>
            </div>    
        </div>
    </div>
</template>

<script>
export default{
    data(){
        return{
            id_name: "p_",
            languages: ["c", "arduino", "php", "mysql", "python", "java"],
            projects: [
               {
                title: "Hide and Seek",
                description: "<h3>A survival horror game. It focuses on the survival of the character throughout the game. Its also objective is attempting to scare the player using scary ambience and graphics. In addition, this game is controlled by a single-player, which means that the game is designed to be played by a one person at a time</h3>",
                date: ""
               },
               {
                title: "Development of Segregation of Unrotten Fruit with Computer Vision",
                description: "",
                date: ""
               },
               {
                title: "Online Freelancing Platform",
                description: "<h3>▪ Online Freelancing Platform aim to create a platform where individuals can post their job expertise.<br> ▪  The project aims to help people find a job contract easily amidst the pandemic.<br> ▪ This platform will serve as a form for independent contractors.<br> ▪ This project will help people to easily interact as freelancers from different fields and individuals looking for skilled workers.</h3>",
                date: ""
               },
               {
                title: "Online Freelancing Platform",
                description: "<h3>▪ Online Freelancing Platform aim to create a platform where individuals can post their job expertise.<br> ▪  The project aims to help people find a job contract easily amidst the pandemic.<br> ▪ This platform will serve as a form for independent contractors.<br> ▪ This project will help people to easily interact as freelancers from different fields and individuals looking for skilled workers.</h3>",
                date: ""
               },
               {
                title: "Classification with Sign Language Alphabet using CNN Convolutional Neural Networks",
                description: "<h3>▪ A gesture recognition that recognize American Sign language Alphabet</h3>",
                date: ""
               },
               {
                title: "AICs BusLiner",
                description: "<h3>A local Bus booking system developed using java.</h3>",
                date: ""
               }
            ]
        }
    }
}

</script>