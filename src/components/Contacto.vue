<template>
    <div>
        <h1>Contacto</h1>
        <form action="">
            <label>Telefono
                <input type="tel" name="telephone" id="telefono" placeholder="Ingresa tu Telefono" pattern="\([0-9]{3}\) [0-9]{3}[ -][0-9]{4}" required><br>
            </label>
            <label>Email
                <input type="email" name="email" id="email" placeholder="Ingresa tu Email" required><br>
            </label>
        </form>
        <button>Enviar</button>
    </div>
    
</template>