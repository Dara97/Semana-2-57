<template>
    <div class="card text-white bg-dark">
                <div class="d-flex justify-content-center p-2">
                    <img :src="member.image" alt="Photo" width="100" height="100">
                </div>
                <div class="card-body">
                    <h5 class="card-title">Team member {{member.codigo}}</h5>
                    <h5 class="card-title">{{member.rol}}</h5>
                    <h5 class="card-title">{{member.nombre}}</h5>

                    <p class="card-text">{{member.descripcion}}</p>
                </div>
               
            </div>
        
</template>

<script>
export default {
  name: "TeamCard",
  props: ["member"],
};
</script>

<style scoped>
</style>
