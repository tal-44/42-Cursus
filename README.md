# 42-Cursus

Este repositorio contiene los proyectos del cursus de 42, organizados como submódulos de Git.

## Proyectos

- **libft**: Biblioteca de funciones básicas en C
- **printf**: Reimplementación de printf
- **get_next_line**: Función para leer línea por línea de un file descriptor
- **push_swap**: Algoritmo de ordenación usando dos stacks

## Clonar el repositorio

Para clonar este repositorio junto con todos los submódulos:

```bash
git clone --recursive https://github.com/tal-44/42-Cursus.git
```

Si ya clonaste el repositorio sin los submódulos, puedes inicializarlos con:

```bash
git submodule update --init --recursive
```

## Actualizar los submódulos

Para actualizar todos los submódulos a sus últimos commits:

```bash
git submodule update --remote --merge
```

## Trabajar con submódulos individuales

Cada submódulo es un repositorio Git independiente. Para trabajar en un submódulo específico:

```bash
cd <nombre-del-submodulo>
# Hacer cambios, commits, etc.
git add .
git commit -m "mensaje"
git push
```

Después de hacer push en un submódulo, actualiza la referencia en el repositorio principal:

```bash
cd ..
git add <nombre-del-submodulo>
git commit -m "Actualizar referencia de <nombre-del-submodulo>"
git push
```