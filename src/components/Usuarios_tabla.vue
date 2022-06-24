<template>
    <section id="vue-section">
        <div id="div-app" class="container">
            <div class="row">
                <div class="col-12 col-md-10 col-lg-8">
                    <div class="mt-5 d-flex flex-row justify-content-around bg-warning">
                        <img :src="ruta_logo" alt="logo" width="50" class="align-self-center p-1">
                        <h2 class="my-0 py-2 text-dark me-5">{{ title }}</h2>
                    </div>
                    <table class="table table-dark table-striped mt-1">
                        <thead>
                            <tr>
                                <th scope="col">#</th>
                                <th scope="col">Nombre</th>
                                <th scope="col">Apellido</th>
                                <th class="text-center" scope="col">RUN</th>
                                <th scope="col">Fecha de Nacimiento</th>
                                <th scope="col">Edad</th>
                            </tr>
                        </thead>
                        <tbody>
                            <tr v-for="(usuario, i) in usuarios" :key="i">
                                <th scope="row">{{ i + 1 }}</th>
                                <td>{{ usuario.nombre }}</td>
                                <td>{{ usuario.apellido }}</td>
                                <td>{{ usuario.RUN }}</td>
                                <td class="text-center">{{ usuario.nacimiento }}</td>
                                <td class="text-center">{{ usuario.edad }}</td>
                            </tr>
                        </tbody>
                    </table>
                </div>
            </div>
        </div>
    </section>
</template>

<script>
export default {
    name: 'Usuarios_tabla',
    data() {
        return {
            title: "Usuarios Nuevos",
            usuarios: [
                {
                    nombre: "Alfonsina M.",
                    apellido: "Pacino",
                    RUN: "15.256.783-3",
                    nacimiento: "04-05-1988",
                    edad: 34,
                },
                {
                    nombre: "Mario",
                    apellido: "Caro",
                    RUN: "14.257.723-4",
                    nacimiento: "07-09-1983",
                    edad: 49,
                },
    
                {
                    nombre: "Alejandro",
                    apellido: "Mancilla",
                    RUN: "14.340.899-1",
                    nacimiento: "09-01-1990",
                    edad: 32,
                }
            ],
            ruta_logo: "favicon.ico"
        }
    },
    props: {

    }
}
</script>

<style scoped>
h3 {
    margin: 40px 0 0;
}

</style>