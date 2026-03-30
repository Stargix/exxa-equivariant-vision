# EXXA Notebooks (Plug-and-Play)

Este repo contiene 2 notebooks listos para ejecutar:

- `exxa_sequential.ipynb`
- `exxa_general.ipynb`

## Requisitos

```bash
python -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
```

## Datos incluidos

El subset de datos está incluido dentro de:

- `continuum_data_subset/continuum_data_subset/*.fits`

No hace falta descargar nada adicional para correr el notebook general con ese subset.

## Ejecución

1. Abrir Jupyter en la carpeta del repo.
2. Ejecutar `exxa_general.ipynb` o `exxa_sequential.ipynb` de arriba a abajo.
3. Si `lightkurve` no tiene conexión, el notebook secuencial sigue en modo sintético.
