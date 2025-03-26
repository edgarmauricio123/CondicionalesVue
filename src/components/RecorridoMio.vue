<script>
export default{

    data(){
        return{
            personas:[
                {id:1, nombrecompleto:'Diego Cruz Cruz', diciplina:'Futbol'},
                {id:2, nombrecompleto:'Jose Luis Sanchez', diciplina:'Beisbol' },
                {id:3, nombrecompleto:'Miguel Ruiz', diciplina:'Futbol' },
                {id:4, nombrecompleto:'Diego Ruiz Ruiz', diciplina:'Box' },
                {id:5, nombrecompleto:'Carmen Hidalgo', diciplina:'Futbol' },
                {id:6, nombrecompleto:'Gabriela Sanchez', diciplina:'Basquetbol' },
                {id:7, nombrecompleto:'Gustavo Cortes', diciplina:'Basquetbol' },
                {id:8, nombrecompleto:'Yael Trinidad', diciplina:'Futbol' },
                {id:9, nombrecompleto:'Angel Reyes', diciplina:'Box' },
                {id:10, nombrecompleto:'Florencia Sarmiento', diciplina:'Box' }


            ]
        }
    }
}
</script>

<template>
    <div class="container">

        <div class="row">
       <div class="cold-md-12">
           <div class="card mt-4">
               <div style="background-color: #f38a8a; border-radius: 5px;" >
                   <h1 class="titulo" >Lista de personas</h1>
               </div>
               <div style="background-color: #f1edd0; border-radius: 5px;" >
                   <ul>
                    <li class="lii" v-for="persona in personas" :key="persona.id"> 
                        <strong>{{ persona.nombrecompleto }}</strong> -- 
                        <strong>{{ persona.diciplina }}</strong>
                    </li>
                   </ul>
                   <br><br>
               </div>
           </div>
       </div>
   </div>
    </div>
    <br><br><br><br><br><br>
</template>
<style>
.card{
    box-shadow: 5px 5px 15px rgba(24, 23, 23, 0.6);
    border-radius: 5px;


}
h3 {
    color: black;
    background-color: rgb(220, 131, 198);
    border-radius: 15px;
    padding: 10px;
}
ul{
    color: blueviolet;
    /* esto es para que no se vean los puntitos */
    list-style-type: none;  
    padding: 0%;
}

.lii{

    color: black;
    background-color: #cde9ca;
    border-radius: 15px;
    padding: 10px;
    margin: 10px;
    text-align: center;
    box-shadow: 5px 5px 15px rgba(24, 23, 23, 0.6);
    font-family: cursive;

}
.titulo{
  text-align: center;
  font-family: Georgia, 'Times New Roman', Times, serif;  
  
}


</style>