# Base de datos

Proyecto Supabase `fiesta-lola` (sa-east-1). El esquema se aplicó por migraciones desde Claude:
tablas con lectura pública (RLS), escritura solo por funciones `security definer` que validan el PIN
del invitado o del árbitro. Los datos secretos (PINs, código de la caja, textos de los carteles,
personajes del dibujo y votos) viven en el esquema `private`, que no se expone por la API.

Nada se borra: "anular", "quitar" y "empezar de nuevo" marcan filas y suben el número de ronda.
