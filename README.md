# Frases Inspiradoras para la Paz

Esta mini aplicación web genera frases poéticas, inspiradas en los escritos de San Juan de la Cruz y otros místicos, dedicadas a los usuarios que introducen su nombre y una palabra significativa. Utiliza la API de OpenAI para componer mensajes personalizados sobre la paz mundial, la luz y el amor.

## Características

- **Personalización:** El usuario introduce su nombre y una palabra clave que resuene con su interior. La aplicación devuelve una frase dedicada en la que no aparece la palabra exacta, pero sí su resonancia simbólica.
- **Inspiración mística:** Las frases combinan la esencia de San Juan de la Cruz con la sabiduría de otros místicos, siempre evitando negaciones en coherencia con el Principio de Frase Afirmativa Transformadora.
- **Despliegue sencillo:** Diseñada para ser desplegada fácilmente en [Render](https://render.com/) a partir de un repositorio de GitHub. Incluye un `Procfile` y `requirements.txt`.

## Estructura del proyecto

- `app.py`: Aplicación Flask que gestiona la lógica de la web y las llamadas a la API de OpenAI.
- `templates/`: Plantillas Jinja2 con el formulario y la visualización de resultados.
- `static/style.css`: Estilos para una presentación cálida y serena.
- `requirements.txt`: Dependencias de Python necesarias para ejecutar la aplicación.
- `Procfile`: Indica a Render/Gunicorn cómo iniciar la aplicación.

## Variables de entorno necesarias

- `OPENAI_API_KEY`: Clave de la API de OpenAI utilizada para generar las frases. Esta variable debe configurarse en Render o en el entorno local antes de ejecutar la aplicación.

## Uso local

1. Clona este repositorio y entra en la carpeta del proyecto.
2. Crea un entorno virtual (opcional):

   ```bash
   python3 -m venv venv
   source venv/bin/activate
   ```

3. Instala las dependencias:

   ```bash
   pip install -r requirements.txt
   ```

4. Exporta tu clave de OpenAI:

   ```bash
   export OPENAI_API_KEY=sk-...  # reemplaza con tu clave real
   ```

5. Ejecuta la aplicación:

   ```bash
   python app.py
   ```

6. Abre tu navegador en `http://localhost:5000` y prueba la aplicación.

## Despliegue en Render

1. Crea un nuevo servicio web en [Render](https://render.com/) y conéctalo con tu repositorio de GitHub.
2. Configura la variable de entorno `OPENAI_API_KEY` en la sección **Environment**.
3. Selecciona la rama a desplegar (por ejemplo, `main`).
4. Render detectará automáticamente tu aplicación por el `Procfile`. De no ser así, especifica en **Start Command**: `gunicorn app:app`.
5. Haz clic en **Create Web Service** y espera a que termine la construcción y despliegue.
6. Una vez desplegada, comparte la URL de Render con quien quieras para que cualquier persona pueda generar sus frases inspiradoras.

## Contribuciones

Las contribuciones son bienvenidas. Si encuentras algún problema o deseas mejorar el código, puedes abrir un _issue_ o enviar un _pull request_.
