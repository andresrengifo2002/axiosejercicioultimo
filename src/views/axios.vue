<template>
    <div>
        <table>
            <thead>
            <h1>
                <th>Id</th>
                <th>nombre</th>
                <th>descripcion</th>
                <th>foto</th>
            </h1>
            </thead>
            <br><br>
            <tbody>
                <tr v-for="posts in posts" :key="posts.Id">
                    <td>{{posts.id}}</td>
                    <td>{{posts.nombre}}</td>
                    <td>{{posts.descripcion}}</td>
                    <td>{{posts.foto}}</td>
                    <td><button @click="update(posts.Id)">actualizar</button></td>
        <!--             <td><button @click="delete(delete.Id)">eliminar</button></td> --> 
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
        actualizar(Id){
            this.$router.push("/update/"+Id)
        }
    },
    computed:{

    },
    components:{

    },
    mounted(){
        axios.get().then(respomse=>{
            console.log(response.data)
            this.posts=response.data
        })
    },

}

</script>
