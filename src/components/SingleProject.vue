<template>
    <div class="project">
        <div class="d-flex justify-content-between">
            <div>
                <h5 @click="show=!show" class="">{{project.title}}</h5>
            </div>
            <div>
                <i class="fa fa-trash-o p-2 " style="font-size:24px"></i>
                <i class="fa fa-edit p-2 " style="font-size:24px"></i>
                <i class="fa fa-check " style="font-size:24px"></i>
            </div>
            
        </div>
        
        <p v-if="show">{{project.detail}}</p>
    </div>
  
</template>

<script>
export default {
    props:['project'],
    data(){
        return{
            show:false
        }
    }
   
}
</script>

<style>
.project{
    padding:20px;
    background-color: #f2f2f2;
    margin:10px;
    border-radius: 5px;
    box-shadow: 3px;
    border-left: 5px solid crimson;
}
h5{
    color:indigo;
    cursor: pointer;
}
i{
    cursor: pointer;
}
i:hover{
    color:#777;
}
</style>