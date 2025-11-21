# Instrucciones para Publicar en GitHub Pages

## 📋 Pasos para Publicar tu Página

### 1. Subir los archivos a GitHub

1. Si aún no tienes un repositorio en GitHub, créalo:
   - Ve a [GitHub](https://github.com)
   - Haz clic en "New repository"
   - Nombra tu repositorio (ejemplo: `mi-podcats` o `noel-ventura-lab`)
   - Selecciona "Public"
   - Haz clic en "Create repository"

2. Sube tus archivos al repositorio:
   ```bash
   git init
   git add .
   git commit -m "Initial commit - Página con videos e imágenes"
   git branch -M main
   git remote add origin https://github.com/TU-USUARIO/TU-REPOSITORIO.git
   git push -u origin main
   ```

### 2. Configurar GitHub Pages

1. Ve a tu repositorio en GitHub
2. Haz clic en **Settings** (Configuración)
3. En el menú lateral, busca **Pages**
4. En "Source", selecciona:
   - **Branch**: `main` (o `master`)
   - **Folder**: `/ (root)`
5. Haz clic en **Save**

### 3. Obtener el Link de tu Página

Después de configurar GitHub Pages, tu página estará disponible en:

**Si tu repositorio se llama `mi-podcats`:**
```
https://TU-USUARIO.github.io/mi-podcats/
```

**Si tu repositorio se llama `TU-USUARIO.github.io`:**
```
https://TU-USUARIO.github.io/
```

**Ejemplo:**
- Usuario: `noelpacheco`
- Repositorio: `mi-podcats`
- Link: `https://noelpacheco.github.io/mi-podcats/`

### 4. Verificar que Funciona

1. Espera 1-2 minutos después de guardar la configuración
2. Visita el link de tu página
3. Verifica que:
   - ✅ Las imágenes se muestren correctamente
   - ✅ Los videos se reproduzcan
   - ✅ Todas las páginas funcionen (index.html, episodios.html, acerca.html, suscripcion.html)

## 🧪 Probar Localmente

Para probar la página antes de subirla a GitHub:

### Opción 1: Servidor Python (Ya iniciado)
El servidor está corriendo en: `http://localhost:8000`

Abre tu navegador y visita:
- `http://localhost:8000/index.html`
- `http://localhost:8000/episodios.html`
- `http://localhost:8000/acerca.html`
- `http://localhost:8000/suscripcion.html`

### Opción 2: Servidor Node.js
```bash
npx http-server -p 8000
```

### Opción 3: Live Server (VS Code)
Si usas VS Code, instala la extensión "Live Server" y haz clic derecho en `index.html` → "Open with Live Server"

## ✅ Checklist de Verificación

Antes de publicar, verifica:

- [ ] Todas las carpetas `images/` y `videos/` están en la raíz del proyecto
- [ ] Todos los archivos HTML tienen rutas con `./images/` y `./videos/`
- [ ] El archivo `.nojekyll` está presente
- [ ] Los archivos están subidos a GitHub
- [ ] GitHub Pages está configurado correctamente

## 🔗 Archivos Importantes

- `index.html` - Página principal
- `episodios.html` - Lista de episodios
- `acerca.html` - Página "Acerca de"
- `suscripcion.html` - Formulario de suscripción
- `images/` - Carpeta con todas las imágenes
- `videos/` - Carpeta con todos los videos
- `.nojekyll` - Archivo necesario para GitHub Pages

## 📝 Notas Importantes

1. **Tiempo de despliegue**: GitHub Pages puede tardar 1-5 minutos en actualizar los cambios
2. **Rutas**: Las rutas relativas con `./` funcionan correctamente en GitHub Pages
3. **Tamaño de archivos**: GitHub tiene límites de tamaño. Si tus videos son muy grandes, considera usar un servicio de hosting de videos como YouTube o Vimeo
4. **HTTPS**: GitHub Pages siempre usa HTTPS, lo cual es seguro y recomendado

## 🆘 Solución de Problemas

**Las imágenes/videos no se muestran:**
- Verifica que las carpetas `images/` y `videos/` estén en la raíz del repositorio
- Verifica que las rutas en los HTML usen `./images/` o `./videos/`
- Asegúrate de que el archivo `.nojekyll` esté presente

**La página muestra 404:**
- Verifica que GitHub Pages esté configurado correctamente
- Asegúrate de que el archivo `index.html` esté en la raíz del repositorio
- Espera unos minutos y recarga la página

**Los cambios no se reflejan:**
- Espera 1-5 minutos después de hacer push
- Limpia la caché del navegador (Ctrl+F5)
- Verifica que los cambios estén en la rama correcta (main/master)

