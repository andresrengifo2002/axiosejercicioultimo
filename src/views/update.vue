<template>
<div>
    <label >id</label>
    <input type="text" v-model="form.id"/>
    <label >name</label>
    <input type="text" v-model="form.name"/>
    <label >status</label>
    <input type="text" v-model="form.status"/>
    <label >species</label>
    <input type="text" v-model="form.species"/>
    <label >type</label>
    <input type="text" v-model="form.type"/>
    <label >gender</label>
    <input type="text" v-model="form.gender"/>
</div>
</template>
<script>
import axios from "axios"
export default {
data(){
    return{
        form:{
            
            id: null,
            name: null,
            status:null,
            species:null,
            type:null,
            type:gender,
              


        }

    }

},
methods(){


},
computed(){

},
mounted() {
    this.axios.get("https://rickandmortyapi.com/api").then(response =>{


})
}


}

</script>
