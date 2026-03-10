# Proyecto Integrador k-NN — Predicción de abandono académico

Proyecto integrador de aprendizaje automático (k-NN) con el dataset *Predict Students' Dropout and Academic Success* (UCI 697).

## Cómo subir a GitHub y que se vea como un libro (barra lateral, búsqueda, tabla de contenidos)

El aspecto de “libro” (barra izquierda, Contents a la derecha, búsqueda) se consigue publicando el proyecto con **MyST** en **GitHub Pages**. Los pasos son:

### 1. Inicializar Git (si aún no lo has hecho)

```bash
cd /home/yisusparker/Dev/machine-learning/repos/proyecto-knn-dropout-book
git init
git add .
git commit -m "Proyecto k-NN + despliegue MyST en GitHub Pages"
```

### 2. Crear el repositorio en GitHub

- Entra en [github.com/new](https://github.com/new).
- Nombre del repo, por ejemplo: `proyecto-knn-dropout-book`.
- **No** marques “Add a README” (ya tienes uno local).
- Crea el repositorio.

### 3. Enlazar y subir

Si tu rama por defecto es `main`:

```bash
git branch -M main
git remote add origin https://github.com/TU_USUARIO/proyecto-knn-dropout-book.git
git push -u origin main
```

Si usas `master`:

```bash
git remote add origin https://github.com/TU_USUARIO/proyecto-knn-dropout-book.git
git push -u origin master
```

Si usas `master`, edita `.github/workflows/deploy.yml` y cambia `branches: [main]` por `branches: [master]`.

### 4. Activar GitHub Pages

- En el repo: **Settings** → **Pages**.
- En **Source** elige **GitHub Actions**.
- Guarda.

### 5. Ver el resultado

- Tras el primer `push`, en **Actions** se ejecutará el workflow “MyST GitHub Pages Deploy”.
- Cuando termine, el sitio estará en:
  **`https://TU_USUARIO.github.io/proyecto-knn-dropout-book/`**

Ahí verás el notebook con el diseño de libro (navegación lateral, tabla de contenidos, búsqueda), como en la referencia que compartiste.

---

## Ejecución local del libro

```bash
pip install mystmd   # o: npm install -g mystmd
myst build --html     # genera _build/html
# Para previsualizar: sirve _build/html con cualquier servidor estático
```

El directorio `_build/` está en `.gitignore`; GitHub Actions hace el build al hacer push.
