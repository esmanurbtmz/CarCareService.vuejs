<template>
    <div id="completed">
        
        <div v-if="prepared.length > 0 " class=" service-container">
            <h3 class="text-center">Completed</h3>
            <ul class="list-group list-group-flush text-center">
                <li v-for="data in prepared" :key="data.id" class="list-group-item d-flex justify-content-between">
                    <span>{{data.text}}</span>  
                    <button @click="$emit('delete-item',data)" class="btn ms-2"><img src="../assets/trash-can-solid.svg" alt=""></button>  
                </li>
                
            </ul>
        </div>
    </div>
</template>

<script>
export default {
    name: "completed",
    props: ["prepared"]
}
</script>

<style scoped>
.list-group-item{
    background-color: #55828b;
    color: #fff;
}
ul{
    border-radius: 10px;

}
img{
    width: 14px;
}

</style>