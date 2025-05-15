<template>
    <div class="container">
        <h1>Contador</h1>
        <p>{{ numero }}<sup>2</sup>={{ numero * numero }}</p>
        <p>{{ this.numero }}<sup>2</sup>={{ calCuadrado }}</p>
        <p>{{ this.numero }}<sup>2</sup>={{ calCuadrado }}</p>
        <p>{{ this.numero }}<sup>2</sup>={{ calCuadrado }}</p>
       
        <p>{{ this.numero }}<sup>2</sup>={{ calCuadrado }}</p>
        <p>{{ this.numero }}<sup>2</sup>={{ calCuadrado }}</p>
        <!--<p>{{ numero }}</p>
    <p>{{ numero+1 }}</p>
    <p>{{ texto }}</p>
    <p>{{ activo }}</p>
    <p>{{ usuario.nombre }}</p>
    <p>{{ arreglo[1] }}</p>
    1+1
    {{ 1+1 }}
    {{ true?'Es verdadero':'Es falso' }}-->
    </div>

    <div>
        <button v-on:click="incrementar()">+1</button>
        <button v-on:click="decrementar()">-1</button>
    </div>


</template>
 
<script>
 
export default {
    data() {
        return {
            numero: 5,
            texto: 'Erick Enriquez',
            activo: true,
            usuario: {
                nombre: 'Erick Enriquez',
                edad: 26,
                genero: 'Masculino'
            },
            arreglo: ["Amarillo", "Azul"],
        };
    },
    methods: {
        calcularCuadrado() {
            console.log("Entro al metodo");
            return this.numero * this.numero;
        },

        incrementar() {
            this.numero++;
        },
        decrementar () {
            this.numero--;
        }
    },
    computed: {
        calCuadrado() {
            console.log("Entro a la propiedad computada");
            return this.numero * this.numero;
        },
    },
};
 
</script>
 
<style>
h1 {
    background: rgb(205, 206, 116);
    color: antiquewhite;
}
 
p {
    background: rgb(106, 112, 141);
}
</style>
 