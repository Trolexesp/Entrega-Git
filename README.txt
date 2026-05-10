````md id="qndm4m"
# Documentación de Git

## ¿Qué es Git?

Git es un sistema de control de versiones que sirve para guardar los cambios realizados en un proyecto. Permite trabajar de forma organizada y recuperar versiones anteriores de los archivos si es necesario.

También facilita el trabajo en equipo, ya que varias personas pueden trabajar sobre el mismo proyecto y sincronizar los cambios mediante un repositorio remoto como GitHub.

Git trabaja principalmente con:
- Directorio local
- Repositorio local
- Repositorio remoto

![Repositorio Git](/Images/repositorio.jpg)

---

## Flujo de trabajo de Git

El funcionamiento básico de Git sigue estos pasos:

1. Modificar archivos en el ordenador.
2. Añadir los cambios con `git add`.
3. Guardar los cambios con `git commit`.
4. Subir los cambios al repositorio remoto con `git push`.
5. Descargar cambios del repositorio remoto con `git pull`.

### Esquema

```text
Directorio local → Repositorio local → Repositorio remoto
       git add         git commit          git push
```

Para actualizar el proyecto:

```text
Repositorio remoto → git pull → Directorio local
```

![Flujo Git](/Images/flujo_git.jpg)

---

## Comandos utilizados en la práctica

### Git add

El comando `git add` se utiliza para añadir archivos al área de preparación antes de hacer un commit.

```bash
git add .
```

Con el punto se añaden todos los archivos modificados.

![Git add](/Images/git_add.jpg)

---

### Git commit

El comando `git commit` guarda los cambios en el repositorio local.

```bash
git commit -m "Primer commit"
```

El texto entre comillas es el mensaje descriptivo del commit.

![Git commit](/Images/git_commit.jpg)

---

### Git push

El comando `git push` sirve para subir los cambios al repositorio remoto.

```bash
git push
```

De esta forma los cambios quedan guardados en GitHub.

![Git push](/Images/git_push.jpg)

---

### Git pull

El comando `git pull` descarga los cambios del repositorio remoto y actualiza el proyecto local.

```bash
git pull
```

![Git pull](/Images/git_pull.jpg)

---

### Git fetch

El comando `git fetch` descarga los cambios del repositorio remoto, pero no los aplica automáticamente.

```bash
git fetch
```

Sirve para revisar los cambios antes de mezclarlos con nuestra rama.

![Git fetch](/Images/git_fetch.jpg)

---

### Git merge

El comando `git merge` se utiliza para combinar ramas o cambios.

```bash
git merge main
```

![Git merge](/Images/git_merge.jpg)

---

## Conflictos en Git

Un conflicto ocurre cuando dos personas modifican la misma parte de un archivo y Git no puede decidir automáticamente qué cambios conservar.

### Causas de un conflicto

- Dos usuarios modifican la misma línea.
- Se realizan cambios incompatibles.
- Un archivo es eliminado por un usuario y modificado por otro.

### Ejemplo de conflicto

```text
<<<<<<< HEAD
Mi cambio
=======
Cambio del compañero
>>>>>>> main
```

### Cómo solucionar un conflicto

1. Revisar el archivo que tiene el conflicto.
2. Elegir qué cambios se quieren mantener.
3. Guardar el archivo corregido.
4. Añadir los cambios con:

```bash
git add .
```

5. Finalizar el proceso con:

```bash
git commit
```

![Conflicto Git](/Images/conflicto_git.jpg)

---

## Conclusión

Git es una herramienta muy útil para organizar proyectos y trabajar en equipo. Gracias al control de versiones es posible guardar cambios, recuperar versiones anteriores y sincronizar el trabajo entre varios usuarios.
````
