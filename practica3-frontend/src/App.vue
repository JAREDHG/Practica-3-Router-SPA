<template>
  <router-view />
</template>

<style>
/* 1. Importamos Bootstrap para que tu diseño se vea profesional */
@import url('https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css');

/* 2. Forzamos a que la caja principal ocupe toda la pantalla */
html, body, #app {
  margin: 0 !important;
  padding: 0 !important;
  width: 100% !important;
  max-width: 100% !important;
  min-height: 100vh !important;
  background-color: #f8fafc;
}

/* 3. Mantenemos intactos los estilos de tu Login para que no se deforme */
.auth-container {
  max-width: 400px;
  margin: 50px auto;
  padding: 30px;
  background: white;
  border-radius: 8px;
  box-shadow: 0 4px 6px rgba(0,0,0,0.1);
  /* Le agregamos una fuente limpia para que no desentone con Bootstrap */
  font-family: Arial, sans-serif; 
}

.auth-container div {
  margin-bottom: 15px;
}

.auth-container label {
  display: block;
  margin-bottom: 5px;
  font-weight: bold;
}

.auth-container input {
  width: 100%;
  padding: 8px;
  border: 1px solid #ccc;
  border-radius: 4px;
  box-sizing: border-box;
}

.auth-container button {
  width: 100%;
  padding: 10px;
  background-color: #3b82f6;
  color: white;
  border: none;
  border-radius: 4px;
  cursor: pointer;
  font-weight: bold;
}

.auth-container button:hover {
  background-color: #2563eb;
}
</style>