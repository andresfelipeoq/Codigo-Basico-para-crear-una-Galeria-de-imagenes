# Codigo-Basico-para-crear-una-Galeria-de-imagenes

Crear una galería de imágenes en JavaScript es un proyecto que implica mostrar una colección de imágenes en una página web y permitir a los usuarios interactuar con ellas, como navegar entre imágenes o ver una versión ampliada de cada una. Aquí tienes un ejemplo básico de cómo puedes crear una galería de imágenes en JavaScript:

1. Configuración del proyecto:

   - Crea una carpeta para tu proyecto.
   - Coloca todas las imágenes que deseas mostrar en la galería en la misma carpeta.
   - Crea un archivo HTML llamado "index.html" y un archivo JavaScript llamado "app.js" en la carpeta.

2. Estructura básica del archivo HTML (index.html):

```html
<!DOCTYPE html>
<html>
<head>
    <title>Galería de Imágenes</title>
</head>
<body>
    <h1>Galería de Imágenes</h1>
    <div id="imageGallery"></div>

    <script src="app.js"></script>
</body>
</html>
```

3. Código JavaScript (app.js):

```javascript
const imageGallery = document.getElementById('imageGallery');
const images = [
    'imagen1.jpg',
    'imagen2.jpg',
    'imagen3.jpg',
    // Agrega aquí las rutas de tus imágenes
];

function createImageElement(imagePath) {
    const image = document.createElement('img');
    image.src = imagePath;
    image.classList.add('gallery-image');
    return image;
}

function displayImages() {
    images.forEach(imagePath => {
        const imageElement = createImageElement(imagePath);
        imageGallery.appendChild(imageElement);
    });
}

displayImages();
```

4. Estilo CSS (opcional):

Puedes personalizar el estilo de la galería agregando CSS. Aquí hay un ejemplo de CSS básico para estilizar las imágenes:

```css
.gallery-image {
    width: 200px;
    height: 200px;
    margin: 10px;
}
```

Este ejemplo básico crea una galería de imágenes que muestra las imágenes listadas en el arreglo `images` en el archivo JavaScript. Asegúrate de cambiar las rutas de las imágenes en el arreglo `images` para que coincidan con las imágenes que deseas mostrar en tu galería.

Puedes expandir esta galería agregando funcionalidades como la capacidad de hacer clic en una imagen para ver una versión ampliada, navegar entre imágenes, o agregar descripciones, dependiendo de tus necesidades y habilidades de desarrollo.
