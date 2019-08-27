<template>
    <div class="home">

        <p>Welcome to your new single-page application, built with <a href="https://vuejs.org" target="_blank">Vue.js</a> and <a href="http://www.typescriptlang.org/" target="_blank">TypeScript</a>.</p>

        <fieldset>

            <legend>Ingrese dos numeros para sumar</legend>
            <label for="">Numero 1:</label>
            <input type="number" id="txtN1">
            <br><br>
            <label for="">Numero 2:</label>
            <input type="number" id="txtN2">
            <br><br>
            <input type="button" @click="Sumar();" value="Calucular" />


        </fieldset>
        <fieldset>

            <legend>Ingrese dos numeros para restar</legend>
            <label for="">Numero 1:</label>
            <input type="number" id="txtN2">
            <br><br>
            <label for="">Numero 2:</label>
            <input type="number" id="txtN3">
            <br><br>
            <input type="button" @click="Restar();" value="Calucular" />


        </fieldset>
        <fieldset>

            <legend>Ingrese dos numeros para multiplicar</legend>
            <label for="">Numero 1:</label>
            <input type="number" id="txtN4">
            <br><br>
            <label for="">Numero 2:</label>
            <input type="number" id="txtN5">
            <br><br>
            <input type="button" @click="Multiplicar();" value="Calucular" />


        </fieldset>
        <fieldset>

            <legend>Ingrese dos numeros para dividir</legend>
            <label for="">Numero 1:</label>
            <input type="number" id="txtN6">
            <br><br>
            <label for="">Numero 2:</label>
            <input type="number" id="txtN7">
            <br><br>
            <input type="button" @click="Dividir();" value="Calucular" />


        </fieldset>

    </div>
    
</template>



<script lang="ts">
    import { Component, Prop, Vue } from 'vue-property-decorator';

    @Component
    export default class Home extends Vue {
        @Prop() private msg!: string;

  
        Sumar() {
            var n1 = (document.getElementById('txtN1') as HTMLInputElement).value;

            var n2 = (document.getElementById('txtN2') as HTMLInputElement).value;
            
        var suma = parseFloat(n1) + parseFloat(n2);
        alert("La suma es: " + suma);
        }

         Restar() {
            var n1 = (document.getElementById('txtN1') as HTMLInputElement).value;

            var n2 = (document.getElementById('txtN2') as HTMLInputElement).value;
            
        var resta = parseFloat(n1) - parseFloat(n2);
        alert("La resta es: " + resta);
        }

         Multiplicar() {
            var n1 = (document.getElementById('txtN1') as HTMLInputElement).value;

            var n2 = (document.getElementById('txtN2') as HTMLInputElement).value;
            
        var multi = parseFloat(n1) * parseFloat(n2);
        alert("La multiplicacion es: " + multi);
        }

         Dividir() {
            var n1 = (document.getElementById('txtN1') as HTMLInputElement).value;

            var n2 = (document.getElementById('txtN2') as HTMLInputElement).value;
            
        var divi = parseFloat(n1) / parseFloat(n2);
        alert("La division es: " + divi);
        }
       
    }


</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>
