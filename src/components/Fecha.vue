<template>
<div class="space">
    <div class="bubble bubble-bottom-left">
        <h1>¿Cuál es tu Fecha de Nacimiento?</h1>
        <form action="">
            <input type="number" name="dia" id="dia" min="1" max="31" placeholder="Día" required>
            <input type="number" name="mes" id="mes" min="1" max="12" placeholder="Mes" required>
            <input type="number" name="año" id="año" min="1950" max="2020" placeholder="Día" required>   
        </form>
        <button class="btn" type="submit">Enviar</button>
    </div>
</div>
</template>

