PAISAJES DE PERTENENCIA — GUÍA DE INSTALACIÓN

ARCHIVOS
- index.html: página web completa.
- setup.sql: tablas y políticas iniciales de Supabase.
- README.txt: estas instrucciones.

1. CREAR EL PROYECTO
1) Entra en https://supabase.com/ y crea un proyecto.
2) Abre Project Settings / API y copia el Project URL y la publishable key (en proyectos antiguos puede aparecer como anon key).
3) Abre SQL Editor y ejecuta todo el contenido de setup.sql.
4) En Storage, crea un bucket llamado paisaje-fotos y márcalo como Public.
5) Configura un límite de 5 MB y permite image/jpeg, image/png e image/webp.

2. CONECTAR LA PÁGINA
Abre index.html en un editor de texto/código.
Busca estas dos cadenas:
PEGA_AQUI_TU_PROJECT_URL
PEGA_AQUI_TU_PUBLISHABLE_O_ANON_KEY

Reemplázalas con los datos de tu proyecto Supabase.
NO uses ni publiques una service_role key o secret key en el navegador.

3. PUBLICAR LA WEB
Publica index.html en un hosting estático que use HTTPS, por ejemplo Netlify, Cloudflare Pages o GitHub Pages.
El QR debe apuntar a la URL pública final de la web; no a un archivo local de tu computadora.
Prueba la web desde un celular y usando datos móviles.

4. IMPORTANTE ANTES DE ABRIR AL PÚBLICO
Este código es una base funcional, pero las políticas iniciales permiten que visitantes anónimos intenten subir fotos. Antes de usarlo en una exposición real, añade protección contra spam (por ejemplo CAPTCHA/Turnstile validado en servidor), moderación antes de publicar y un mecanismo privado para administrar o eliminar aportes.
Informa claramente que las fotos serán públicas y pide no incluir rostros ni datos personales.
Comprueba los límites y posibles costes de almacenamiento y tráfico.

5. REPRODUCCIÓN
El reproductor muestra las fotos en orden cronológico, aproximadamente una por segundo. Esto es una secuencia animada dentro de la página, NO un archivo MP4 descargable. Para generar un MP4 real se necesita un proceso adicional en servidor.

6. ORDEN DE LAS FOTOS
La base de datos ordena por la hora de recepción. Si varias personas suben fotos casi al mismo tiempo, el orden puede no coincidir exactamente con el orden de pintura. Para mantener un orden estricto, añade una revisión del equipo antes de publicar cada etapa.
