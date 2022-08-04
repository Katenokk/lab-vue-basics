<template>
 <div>My navigation bar</div>
 <p> {{string}}</p>
 <input type="text" v-model="name">
 <button @click="sayHello">Say hello</button>
 <br>
 <input type="checkbox" v-model="isTrue">Is true?
 <br>
 <button v-show="isTrue">Solo se ve si es true</button>
 <h2 :class="size">Prueba cambiar clases</h2>
 <h3 :class="background">Esto cambia de fondo</h3>
 <button @click="changeSize">Cambia tamaño</button>
 <br>
 <button @click="changeColor">Change color</button>
 
 
<br>
<div>
    <div>
    <ul >
        <li v-for="project in projects" :key="project.id" class="none"> 
        {{project.title}} <br>
        {{project.content}}</li>
    </ul>
    </div>
</div>

</template>

<script>
export default {
    
data() {

    return {
        string: "",
        name: "",
        isTrue: false,
        size: "small",
        background: "green",
        projects: [
        {
            id: 1,
            title: "Project1",
            content: "Prueba cutre para ver si funciona"
        },
        {
            id: 2,
            title: "Project2",
            content: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Culpa, optio!"
        },
        {
            id: 3,
            title: "Project3",
            content: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Culpa, optio!"
        }


    ]
        
    }
   
},
methods: {
    sayHello() {
        this.string = "hello " + this.name 
    },
    changeSize() {
        this.size = "big";
    },
    changeColor() {
        if(this.isTrue===true) {
            this.background = "pink"; //solo funciona si está puesto el tick
                console.log("isTrue"); 
        }
    }
},
mounted() {
    this.sayHello;
}

}





</script>

<style>
.small {
    font-size: 15px;
}

.big {
    font-size: 40px;
}

.green {
    background: green;
}
.pink {
    background: pink;
}
.none {
    list-style: none;
    margin: 1em 0;
}

</style>