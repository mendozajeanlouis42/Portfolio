<template>

 <v-app-bar app color="#111111" dark flat class="px-8 "  >
     <v-btn icon>
         <v-icon color="#FFD700">fas fa-diamond</v-icon>
     </v-btn>
     <v-spacer></v-spacer>
     <div>

         <v-btn text @click="scroll('home')">Home</v-btn>
         <v-btn text @click="scroll('projects')">Projects</v-btn>
         <v-btn text @click="scroll('skills')">Skills</v-btn>
         <v-btn text @click="scroll('about')">About</v-btn>
         <v-btn text @click="scroll('contact')">Contact</v-btn>
     </div>
 </v-app-bar>
 
</template>

<script>
export default {
    methods:{
        scroll(refName){
            const element = document.getElementById(refName);
            console.log(element)
            element.scrollIntoView({behavior: "smooth"})
        }
    },
    name: 'Burger'
}
</script>

<style>

</style>