# Plantilla Web API (.NET + Tailwind CSS + Vanilla JS)

Plantilla personalizada de ASP.NET Core Web API. El backend se desarrolla en C# con Web API y el frontend es estático (HTML/JS puro con Tailwind CSS), servido desde la carpeta `wwwroot`.

## Requisitos previos

- .NET SDK (versión 8, 9 o 10, según tu entorno): https://dotnet.microsoft.com/
- Node.js (incluye npm): https://nodejs.org/

## Poner en marcha un proyecto nuevo

La carpeta `node_modules` no se incluye al exportar la plantilla, por lo que hay que restaurarla al crear un proyecto nuevo.

1. Restaurar las dependencias de Node. Desde la raíz del proyecto:

```bash
npm install
```

2. Iniciar el compilador de Tailwind. Dejalo corriendo en una terminal mientras desarrollás, así las clases CSS se compilan automáticamente:

```bash
npm run tailwind:build
```

3. Ejecutar la API. Presioná F5 en Visual Studio o, en otra terminal, ejecutá:

```bash
dotnet run
```

## Estructura del proyecto

- `Controllers/`: endpoints de la API en C#.
- `wwwroot/`: archivos estáticos del frontend.
  - `index.html`: página principal de la aplicación.
  - `css/input.css`: archivo de entrada con las directivas de Tailwind (`@tailwind ...`).
  - `css/site.css`: CSS compilado automáticamente por Tailwind. No editar a mano.
- `tailwind.config.js`: configuración de Tailwind (apunta a la carpeta `wwwroot`).
- `Program.cs`: configuración de la API y habilitación de archivos estáticos mediante `UseDefaultFiles` y `UseStaticFiles`.
