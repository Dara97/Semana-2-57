<template>
  <div id="app">
    <div class="container-fluid">
        
               <sec-noticias></sec-noticias>
            </div>
      

    <div class="container-fluid">
    <div class="row justify-content-center mb-5">

        <div class="col mt-5" v-for="(item,index) of member" :key="index">
      
    <team-card v-bind:member="item"></team-card>
    </div>
    </div>
    </div>
  </div>
  
</template>

<script>
import SecNoticias from "./components/SecNoticias.vue";
import TeamCard from "./components/TeamCard.vue";

export default {
  name: "App",
  components: {
    SecNoticias,
    TeamCard,
  },
  data() {
    return {
      member: [
        {
          codigo: 1,
          nombre: "Andrea Viviana Yanza Hurtado",
          descripcion:
            "Estudiante y trabajadora de 20 años de edad con gran interés en el área de la computación y el autoaprendizaje, donde refuerza sus habilidades cognitivas con las herramientas de la natación y el yoga.",
          rol: "Scrum Master",
          image:
            "https://cdn.pixabay.com/photo/2020/10/04/05/45/woman-5625298__480.png",
        },

        {
          codigo: 2,
          nombre: "Brian Alejandro Corredor León",
          descripcion:
            "Programador autodidacta y con resultados aprobatorios del ciclo I y II de la Misión Tic 2022 en la UTP, con profundo gusto por el cine. Su edad es de 27 años.",
          rol: "Product owner",
          image:
            "https://cdn.pixabay.com/photo/2018/08/28/13/29/avatar-3637561__480.png",
        },

        {
          codigo: 3,
          nombre: "Dara Mileth Inampuez Lopez",
          descripcion:
            "Estudiante y trabajadora con intereses en las áreas del baile, el ejercio físico y el aprendizaje desde la investigación continuada, luego de graduarse del ciclo I y II de la Misión Tic cursa actualmente el ciclo III de esta.",
          rol: "Development Team",
          image:
            "https://cdn.pixabay.com/photo/2020/10/04/05/44/woman-5625296__480.png",
        },

        {
          codigo: 4,
          nombre: "Santiago José Marmolejo Mendoza",
          descripcion:
            "Programador autodidacta y con resultados aprobatorios del ciclo I y II de la Misión Tic 2022 en la UTP, con profundo gusto por el cine. Su edad es de 27 años.",
          rol: "Development Team",
          image:
            "https://cdn.pixabay.com/photo/2020/11/22/22/17/male-5768177__480.png",
        },

        {
          codigo: 5,
          nombre: "Daniela Sthepanny Jimenez Navarro",
          descripcion:
            "Estudiante y trabajadora con intereses en las áreas del baile, el ejercio físico y el aprendizaje desde la investigación continuada, luego de graduarse del ciclo I y II de la Misión Tic cursa actualmente el ciclo III de esta.",
          rol: "Development Team",
          image:
            "https://cdn.pixabay.com/photo/2020/10/04/05/51/woman-5625312__480.png",
        },
      ],
    };
  },
};
</script>

