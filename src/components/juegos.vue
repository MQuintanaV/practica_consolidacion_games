<template>
    <div id="juegos">
        <h1>componente juegos</h1>
        <div class="contenedorPadre">
            <div class="card" style="width: 18rem;">
                    <img src="../assets/logo.png" class="card-img-top" alt="...">
                    <div class="card-body">
                        <h5 class="card-title">Card title</h5>
                        <p class="card-text">Some quick example text to build on the card title and make up the bulk of the card's content.</p>
                    </div>
                    <ul class="list-group list-group-flush">
                        <li class="list-group-item">An item</li>
                        <li class="list-group-item">A second item</li>
                        <li class="list-group-item">A third item</li>
                    </ul>
                    <div class="card-body">
                        <a href="#" class="card-link">Card link</a>
                        <a href="#" class="card-link">Another link</a>
                    </div>
        </div>                

</div>
        
    </div>
</template>

<script>
import axios from 'axios';
export default{
    name:'juegos',
    data:function(){
        return{

        }
    },
    methods:{
        consumirApi:function(){

            let url='https://api.rawg.io/api/platforms?key=bc355598c96a47c59cb5b8e8efbce746'
            axios(url)
            .then(respuesta =>{
                console.log(respuesta);
               
            })
            .catch(error=>{
                console.log(error);
            });

        },
    },
    created(){
        this.consumirApi();
    }
}
</script>
<style scoped>
#juegos{
    background-color: #F3E5F5;
}
.contenedorPadre{
    display:flex;
    flex-wrap: wrap;
    justify-content: center;
}
</style>