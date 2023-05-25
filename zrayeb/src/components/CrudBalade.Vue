<template>
    <div>
        <form @submit.prevent="submitForm">
            <label for="nomBateau">Nom du Bateau</label>
            <input type="text" id="nomBateau" v-model="nomBateau" required>

            <label for="comptiter">Comptité</label>
            <input type="text" id="comptiter" v-model="comptiter" required>

            <label for="Num">Numéro</label>
            <input type="number" id="Num" v-model="num" required>

            <label for="largeure">Largeur</label>
            <input type="number" id="largeure" v-model="largeure" required>

            <label for="longeur">Longueur</label>
            <input type="number" id="longeur" v-model="longeur" required>

            <button type="submit">Submit</button>
        </form>
    </div>
</template>
  
<script>
export default {
    data() {
        return {
            nomBateau: '',
            comptiter: '',
            num: null,
            largeure: null,
            longeur: null
        };
    },
    methods: {
        submitForm() {
            const baladeData = {
                nomBateau: this.nomBateau,
                comptiter: this.comptiter,
                num: this.num,
                largeure: this.largeure,
                longeur: this.longeur
            };

            // Do something with the baladeData, such as sending it to a server or processing it further

            // Reset the form fields
            this.nomBateau = '';
            this.comptiter = '';
            this.num = null;
            this.largeure = null;
            this.longeur = null;
        }
    }
};
</script>
  