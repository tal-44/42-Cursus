# 42-Cursus

Este repositorio contiene los proyectos del cursus de 42, organizados como submódulos de Git.

## Estructura de Proyectos

### Submódulos Principales

1. **gnl** (get_next_line)
   - Función para leer línea por línea de un file descriptor
   - Repositorio: https://github.com/tal-44/get_next_line.git

2. **libft**
   - Biblioteca de funciones básicas en C
   - Incluye **ft_printf** integrado (no como submódulo)
   - Contiene **gnl** como submódulo anidado
   - Repositorio: https://github.com/tal-44/libft.git

3. **push_swap**
   - Algoritmo de ordenación usando dos stacks
   - Utiliza **libft** como submódulo (con gnl y ft_printf incluidos)
   - Repositorio: https://github.com/tal-44/push_swap.git

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

**Nota importante sobre submódulos anidados:**
- `libft` contiene `gnl` como submódulo anidado
- Usa siempre `--recursive` para asegurar que todos los niveles de submódulos se inicialicen

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