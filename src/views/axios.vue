<template>
    <div>
        <table>
            <thead>
            <h1>
                <th>id     </th>
                <th>name     </th>
                <th>status    </th>
                <th>species   </th>
                <th>type      </th>
                <th>gender  </th>
                
              
              
            </h1>
            </thead>
            <br><br>
            <tbody>
                <tr v-for="posts in posts" :key="posts.id">
                    <td>{{posts.id}}</td>
                    <td>{{posts.name}}</td>
                    <td>{{posts.status}}</td>
                    <td>{{posts.species}}</td>
                    <td>{{posts.type}}</td>
                    <td>{{posts.gender}}</td>
                    <td><button @click="actualizar(posts.id)">actualizar</button></td>
                    <td><button @click="eliminar(deletetask.id)">eliminar</button></td>
                    <td><button @click="enviar(posts.id)">enviar</button></td>
                   
                </tr>
            </tbody>
            <button class="botoncancelar" >cancelar</button>
        </table>
    </div>
</template>
<script>
import axios from 'axios'
export default{
    data(){
        return{
            posts:null
        }
    },
    methods:{
        actualizar(id){
            this.$router.push("/actualizar/"+id)
        },
        async eliminar (id){
            await axios.delete("https://rickandmortyapi.com/api/character").then(response=> {

            })
        },
        async enviar (id){
            await axios.posts("https://rickandmortyapi.com/api").then(response=> {

            })

        },
        
    },
    computed:{

    },
    components:{

    },
    mounted(){
        axios.get("https://rickandmortyapi.com/api").then(response=>{
            console.log(response.data)
            this.posts=response.data
        })
    },

}

</script>
