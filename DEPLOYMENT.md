# Despliegue en Render - AirSafe App

## Pasos para desplegar en Render

### 1. Preparación del repositorio
- Asegúrate de que tu código esté en un repositorio Git (GitHub, GitLab, etc.)
- El repositorio debe contener todos los archivos del proyecto

### 2. Configuración en Render
1. Ve a [render.com](https://render.com) y crea una cuenta
2. Haz clic en "New +" y selecciona "Static Site"
3. Conecta tu repositorio de Git
4. Configura el servicio:
   - **Name**: `airsafe-app` (o el nombre que prefieras)
   - **Build Command**: `npm run build`
   - **Publish Directory**: `dist`
   - **Environment**: `Node.js 18.17.0`

### 3. Variables de entorno (si las necesitas)
Si tu aplicación usa variables de entorno, agrégalas en la sección "Environment Variables" de Render.

### 4. Despliegue
- Render detectará automáticamente los cambios en tu repositorio
- Cada vez que hagas push a la rama principal, se desplegará automáticamente
- La URL de tu aplicación será: `https://tu-app-name.onrender.com`

## Comandos útiles

```bash
# Construir localmente para probar
npm run build

# Iniciar desarrollo
npm start

# Probar en web
npm run web
```

## Notas importantes
- Asegúrate de que todas las dependencias estén en `package.json`
- El archivo `render.yaml` ya está configurado para el despliegue automático
- La aplicación se construirá como una aplicación web estática 