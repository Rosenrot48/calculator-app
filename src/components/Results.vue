<template>
    <div class="result-header hh">
        <h1>{{name}}!</h1>
        <h2 >Рады приветствовать Вас на нашем математическом тренинге<br>Ваша статистика за последние 7 дней</h2>
    </div>
</template>


<script>
    export default {
        name: 'Results',
        data: () => {
            return {
                name: 'Мария',
            }
        }
    }
</script>


<style>
    .result-header {
        margin-left: 2%;
        margin-top: 5%;
        width: 80%;
    }
    .hh {
        color: cornflowerblue;
    }
</style>
