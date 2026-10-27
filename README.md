# paisaje-colectivo
Instalación artística interactiva en la que los visitantes crean colectivamente un paisaje y registran su evolución mediante fotografías.

## ¿Qué es?

Paisaje Colectivo es una página web para una instalación artística participativa. Cada visitante contribuye a la creación de un paisaje físico y registra el avance de la obra mediante una fotografía.

La página permite subir las fotografías y visualizar la evolución del paisaje en orden cronológico, como una secuencia acelerada.

## 1. Archivos del proyecto

- `index.html`: página web principal.
- `setup.sql`: instrucciones para crear la tabla de datos en Supabase.
- `README.txt`: instrucciones de configuración.

## 2. Servicios necesarios

Para que la página funcione con fotografías compartidas entre distintos visitantes, necesitas:

- **Supabase:** almacenamiento de imágenes y base de datos.
- **Hosting web:** para publicar la página y generar un enlace HTTPS.
- **Código QR:** para que los visitantes accedan a la página desde sus celulares.

## 3. Configuración de Supabase

1. Crea una cuenta en https://supabase.com/.
2. Crea un proyecto.
3. En el apartado SQL Editor, abre el archivo `setup.sql`, copia su contenido y ejecútalo.
4. En Storage, crea un bucket llamado `paisaje-fotos`.
5. Configura las credenciales públicas del proyecto en `index.html`:
   - `SUPABASE_URL`
   - `SUPABASE_PUBLISHABLE_KEY`

Utiliza únicamente la clave pública del proyecto. Nunca coloques la clave secreta o `service_role` en el código de la página.

**Importante:** las políticas de acceso deben permitir las operaciones que necesita la web. Antes de usarla en una instalación pública, conviene añadir controles contra el spam y las subidas automatizadas.

## 4. Publicación de la página

Puedes publicar `index.html` mediante un servicio de hosting estático, como Netlify o GitHub Pages.

Después de publicarla:

1. Abre el enlace HTTPS desde un celular.
2. Comprueba que se puedan subir fotografías.
3. Verifica que las imágenes aparezcan en la secuencia.
4. Genera un código QR con el enlace publicado.
5. Coloca el QR junto al lienzo físico.

## 5. Experiencia del visitante

1. El visitante observa el paisaje creado hasta ese momento.
2. Realiza su contribución al lienzo físico.
3. Toma una fotografía de la obra completa.
4. Escanea el código QR.
5. Sube la fotografía desde su celular.
6. La imagen se incorpora al registro de la evolución colectiva.

## 6. Visualización de la evolución

La página permite recorrer las fotografías para observar cómo cambia el paisaje con cada participación.

La secuencia funciona como una presentación acelerada de imágenes; no equivale a un archivo de video MP4 descargable.

## 7. Consideraciones para la instalación

- Mantén el encuadre de las fotografías lo más constante posible.
- Indica que se debe fotografiar el lienzo completo.
- Evita que aparezcan rostros u otros datos personales en las imágenes.
- Prueba la página con varios celulares antes del evento.
- Asegúrate de contar con conexión a internet durante la actividad.
- No publiques la página hasta verificar que la subida y visualización de imágenes funcionen correctamente.

**Nota:** el sitio requiere configurar Supabase y publicarse en un hosting antes de estar disponible para los visitantes.
