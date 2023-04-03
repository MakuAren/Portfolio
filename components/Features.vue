<template>
    <div id="feature">
        <ul id="skills">
            <h1>Skills</h1>
            <li v-for="(language, index) in languages" :key="index" @click="showProj(index)">
                <img v-if="index === 0" :class=className+status[index] :id=language+colored :src='require("../assets/logo/"+language+"_colored.png")'>
                <img v-else :class=className :id=language+colored :src='require("../assets/logo/"+language+"_colored.png")' style="display: none;">
                <img v-if="index === 0" :class=className :id=language :src='require("../assets/logo/"+language+".png")' style="display: none;">
                <img v-else :class=className+status[0] :id=language :src='require("../assets/logo/"+language+".png")'>
            </li>
        </ul>
    </div>
</template>

<script>
export default {
    data(){
        return{
            className: "btn",
            colored: "_colored",
            languages: ["c", "arduino", "php", "mysql", "python", "java"],
            status: [" active", "", "", "", "", ""],
            type: ["_colored", "", "", "", "", ""],
            past: 0
        }
    },
    methods: {
        showProj(index){
            for(let i=0; i < this.languages.length; i++){
                if(i === index){
                    document.getElementById(this.languages[i]).style.display = "none";
                    document.getElementById(this.languages[i]+this.colored).style.display = "";
                    document.getElementById("p_"+i).style.display = "block";
                    
                } else {
                    document.getElementById(this.languages[i]).style.display = "";
                    document.getElementById(this.languages[i]+this.colored).style.display = "none";
                    document.getElementById("p_"+i).style.display = "none";
                }
            }
        }
//         {
//     let actPic = document.getElementById("p"+past);
//     let skillNum = i+1;
//     current[0].src = "./images/logo/"+past+".png";
//     actPic.style.display = "none";
//     actPic.className = actPic.className.replace(" active", "");
//     current[0].className = current[0].className.replace(" active", "");

//     console.log(skillNum);

//     let currentPic = document.getElementById("p"+skillNum);
//     past = skillNum;
//     currentPic.style.display = "block";
//     this.className += " active";
//     this.src = "./images/logo/"+skillNum+"c.png";
//   }
    }
}
</script>