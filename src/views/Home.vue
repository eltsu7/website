<template>
    <div class='row'>
        <div class='flex-item'>
            <h1>Eeli Hernesniemi</h1>
            <p>Studying my third year of information technology in Tampere University.</p>
            <p>{{ age }} years old.</p>
            <p>Buzzwords: Python, C++, Linux, PostgreSQL, DigitalOcean, Docker</p>
        </div>
        <div class='flex-item'>
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
            var birthday = new Date("1996-12-24T00:00:00")

            // age in milliseconds
            var ageMs = Date.now() - birthday.getTime();

            // age in years
            var age = ageMs / year;

            // rounded to 1 decimal
            return Math.round( age * 10 ) / 10;
        }
    }
}
</script>

<style scoped>

.row {
    display: flex;
    flex-direction: row;
    flex-wrap: wrap;
    justify-content: space-around;
    align-items: center; 
}

.flex-item {
    max-width: 300px;
    padding: 10px;
    margin-top: 10px;
}

img {
    max-width: 100%;
}

p {
    padding-left: 10px;
    font-size: 17px;
}

h1 {
    margin-top: 0px;

}

</style>
