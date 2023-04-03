<template>
    <div>
    <nav id="navigation">
        <div id="navContainer">
            <div id="logoContainer">
                <a href="javascript:void(0)">
                    <img alt="hi" id="logo" src="../assets/logo/logo.png">
                    <span id="lname">&nbspA K U&nbsp;&nbsp;&nbsp;D E V&nbsp;</span>
                </a>
            </div>
            <ul id="navOptions" class="navbar-nav me-auto">
                <li><a @click="show()" href="#header">Home</a></li>
                <li><a @click="show()" href="#feature">Skills</a></li>
                <li><a @click="show()" href="#projects">Project</a></li>
                <li><a @click="show()" href="#footer">Contact</a></li>
            </ul>
        </div>
    </nav>
    </div>
</template>

<script>
export default {
  methods: {
    show() {
        console.log("show")
        document.getElementById("hContainer").style.opacity = 1;
        document.getElementById("navigation").style.backgroundColor = "rgba(18,18,18,1)";
        document.getElementById("navContainer").style.backgroundColor = "rgba(18,18,18,1)";
        document.getElementById("skills").style.opacity = 1;
        document.getElementById("projects").style.opacity = 2;
    }
  }
}
</script>