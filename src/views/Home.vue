<template>
    <div class='row'>
        <div class='column'>
            <h1>Eeli Hernesniemi</h1>
            <p>Studies <b>information technology</b> in <b>Tampere University</b>.</p>
            <p>{{ age }} years old.</p>
            <p>Famous for creating and maintaining MarkkuBot.</p>
        </div>
        <div class='column'>
            <img src="../assets/portrait.jpg" alt="Pic of Me">
        </div>
    </div>
</template>

<script>
export default {
    props: ["age"],
    created() {
        this.age = this.calculateAge()
    },
    methods: {
        calculateAge() {
            var year = 365 * 24 * 60 * 60 * 1000;
            var birthday = new Date("1996.12.24")
            var ageMs = Date.now() - birthday.getTime();
            var age = ageMs / year;
            return Math.round( age * 10 ) / 10;
        }
    }
}
</script>

<style scoped>
.column {
    float: left;
    width: 45%;
    padding: 10px
}

img {
    max-width: 100%;
    float: right;
}

p {
    padding-left: 10px;
}

</style>
