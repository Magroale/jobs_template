<template>
    <div class="">
        <ol style="list-style-type: none;">
            <li v-for="(trabajos, indice) in trabajos" :key="indice">
                <div id="contenedorgeneral"
                    class="d-flex flex-row mb-3 align-self-center justify-content-center border rounded-3 sombra">
                    <div id="contenedor imagen" class="text-center ">
                        <img :src="trabajos.rutasImagenes" style="max-block-size: 10rem;" alt="" class="margin-right m-4" />
                    </div>
                    <div class="d-block p-2">
                        <div id="contenedorinfoTrabajo" class="d-flex flex-row mb-3 text-center justify-content-center">

                            <div class="d-flex flex-row mb-3 text-center justify-content-center margin-right m-4">
                                <p class="h1"> {{ trabajos.nombreTrabajo }} </p>
                            </div>
                            <div class="d-flex flex-row mb-3 justify-content-evenly align-self-center margin-right m-1  text-center"
                                v-for="(CapacidadesEmpleo, indice) in trabajos.CapacidadesEmpleo" :key="indice">
                                <p class="align-self-center text-center border rounded-3 "><small>{{ CapacidadesEmpleo }}</small></p>
                            </div>
                        </div>
                        <div id="infoAdicional" class="d-flex flex-row mb-3 text-center justify-content-evenly">
                            <div class="d-flex flex-row mb-3 text-center justify-content-center margin-right m-4">
                                <i class="far fa-building margin-right m-1"></i>
                                {{ trabajos.nombreEmpresa }}
                            </div>
                            <div class="d-flex flex-row mb-3 text-center justify-content-center margin-right m-4">
                                <i class="fas fa-location-dot margin-right m-1"></i>
                                {{ trabajos.lugarEmpleo }}
                            </div>
                            <div class="d-flex flex-row mb-3 text-center justify-content-center margin-right m-4">
                                <i class="fas fa-money-bill-1-wave margin-right m-1"></i>
                                {{ trabajos.salarioEmpleo }}
                            </div>
                            <div class="d-flex flex-row mb-3 text-center justify-content-center margin-right m-4" >
                                <i class="fas fa-user-group margin-right m-1" ></i>
                                {{ trabajos.cantidadVacantes }} 
                                <p class="align-self-center text-center" style="margin-left: 5px;" v-if="trabajos.cantidadVacantes === 1"><small> Vacante</small></p>
                                <p class="align-self-center text-center" style="margin-left: 5px;" v-else><small> Vacantes</small></p>
                            </div>
                            <div class="d-flex flex-row mb-3 text-center justify-content-center margin-right m-4">
                                <i class="far fa-calendar-days margin-right m-1"></i>
                                {{ trabajos.fechaPublicacion }}
                            </div>
                        </div>
                    </div>
                </div>
            </li>
        </ol>
    </div>
</template>
  
<script>
export default {
    name: 'HelloWorld',
    props: {
        msg: String
    },
    data() {
        return {
            trabajos: [
                {
                    nombreTrabajo: 'Desarrollador back-end',
                    CapacidadesEmpleo: ['Linux', 'Django', 'SQL'],
                    nombreEmpresa: 'EPS',
                    lugarEmpleo: 'Remoto',
                    salarioEmpleo: '$3M-4M COP',
                    cantidadVacantes: 1,
                    fechaPublicacion: '1 month ago',
                    rutasImagenes: "../assets/backend.png",
                },
                {
                    nombreTrabajo: 'Gerente de ventas',
                    CapacidadesEmpleo: ['Liderazgo', 'Analisis'],
                    nombreEmpresa: 'CCD compañia de seguros',
                    lugarEmpleo: 'Cali',
                    salarioEmpleo: 'Confidencial',
                    cantidadVacantes: 3,
                    fechaPublicacion: '6 days ago',
                    rutasImagenes: "../assets/gerente.png",
                },
                {
                    nombreTrabajo: 'Administrador de empresas',
                    CapacidadesEmpleo: ['Administracion', 'Capacidad de Analisis', 'SEO'],
                    nombreEmpresa: 'Hotel palaza de oro',
                    lugarEmpleo: 'Bogota',
                    salarioEmpleo: '$3M-4M COP',
                    cantidadVacantes: 1,
                    fechaPublicacion: '3 hours ago',
                    rutasImagenes: "../assets/administrador.png",
                },
                {
                    nombreTrabajo: 'Administrador de empresas',
                    CapacidadesEmpleo: ['Administracion', 'Capacidad de Analisis', 'SEO'],
                    nombreEmpresa: 'Hotel palaza de oro',
                    lugarEmpleo: 'Bogota',
                    salarioEmpleo: '$3M-4M COP',
                    cantidadVacantes: 1,
                    fechaPublicacion: '3 hours ago',
                    rutasImagenes: "../assets/administrador.png",
                },
                {
                    nombreTrabajo: 'Administrador de empresas',
                    CapacidadesEmpleo: ['Administracion', 'Capacidad de Analisis', 'SEO'],
                    nombreEmpresa: 'Hotel palaza de oro',
                    lugarEmpleo: 'Bogota',
                    salarioEmpleo: '$3M-4M COP',
                    cantidadVacantes: 1,
                    fechaPublicacion: '3 hours ago',
                    rutasImagenes: "../assets/administrador.png",
                }
            ],

        }
    },
    methods: {
    },
}
</script>
  
  <!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.sombra {
    transition: box-shadow 0.3s;
    /* Agrega una transición suave para la sombra */
}

.sombra:hover {
    box-shadow: 5px 5px 10px rgba(0, 0, 0, 0.5);
    /* Aplica una sombra al hacer hover */
}

.popup {
    display: none;
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background: rgba(0, 0, 0, 0.5);
    z-index: 1;
}

.contenido-popup {
    background: #fff;
    width: 300px;
    margin: 100px auto;
    padding: 20px;
    text-align: center;
    border-radius: 5px;
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.5);
}

/* Estilos para mostrar el pop-up cuando es necesario */
.popup.v-mostrar {
    display: block;
}
</style>