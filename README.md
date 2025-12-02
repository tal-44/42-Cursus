# 42-Cursus

Este repositorio contiene los proyectos del cursus de 42, organizados como submódulos de Git.

## Estructura de Proyectos

### Submódulos Principales

1. **gnl** (get_next_line)
   - Función para leer línea por línea de un file descriptor
   - Repositorio: https://github.com/tal-44/get_next_line.git

2. **libft**
   - Biblioteca de funciones básicas en C
   - Incluye **ft_printf** y **gnl** integrados
   - Repositorio: https://github.com/tal-44/libft.git

3. **push_swap**
   - Algoritmo de ordenación usando dos stacks
   - Contiene copia local de libft (solo funciones necesarias)
   - Repositorio: https://github.com/tal-44/push_swap.git

4. **pipex**
   - Simulación del comportamiento de pipes de Unix
   - Repositorio: https://github.com/tal-44/pipex.git

5. **fract-ol**
   - Explorador de fractales usando MiniLibX
   - Contiene copia local de libft y MiniLibX

## Clonar el repositorio

Personalmente recomiendo por facilidad clonar solo el repositorio que necesites.

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

**Nota sobre dependencias:**
- Los proyectos individuales (fract-ol, push_swap) contienen copias locales de sus dependencias
- No hay submódulos anidados en los proyectos individuales

## Compilar los Proyectos

### Compilar libft
```bash
cd libft
make
```

### Compilar push_swap
```bash
cd push_swap
make
```
Esto compilará automáticamente libft como dependencia.

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
