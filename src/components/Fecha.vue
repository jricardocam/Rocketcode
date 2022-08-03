<template>
    <div>
        <h1>¿Cuál es tu Fecha de Nacimiento?</h1>
        <form action="">
            <label>Día 1 al 31
            <input type="number" name="dia" id="dia" min="1" max="31" placeholder="Día" required><br>
            </label>
            <label>Mes 1 al 12
            <input type="number" name="mes" id="mes" min="1" max="12" placeholder="Mes" required><br>
            </label>
            <label>Año 1950 a 2020
            <input type="number" name="año" id="año" min="1950" max="2020" placeholder="Día" required><br>
            </label>
        </form>
        <button>Enviar</button>
    </div>
</template>