Erick Segura Sánchez A01613821
Links:[[Algoritmos Avanzados]]
# E1. Actividad integradora 1

`TC2038.606`

### Profesor

- Dr. Jesús Guillermo Falcón Cardona

### Integrantes

- Erick Segura Sánchez
- Alvaro Eduardo Lozano Medina

# Manual de Usuario: Procesador de Textos

## Requerimientos de instalación

Antes de ejecutar la aplicación, asegúrate de tener instalado:

1. Python 3
2. Streamlit

Para instalar Streamlit, puedes usar pip:

```
pip install streamlit
```

## Uso de la aplicación

1. **Iniciar la aplicación:**
   Ejecuta el siguiente comando en la terminal:
   
   ```
   streamlit run main.py
   ```


2. **Cargar archivos:**
   - Utiliza los botones "Cargar primer archivo" y "Cargar segundo archivo" para subir archivos de texto (.txt).
   - El contenido de los archivos se mostrará en áreas de texto.

3. **Búsqueda de patrones:**
   - Ingresa un patrón en el campo "Buscar patrón".
   - Haz clic en "Buscar" para encontrar coincidencias en el primer texto.
   - Las coincidencias se resaltarán en amarillo.

4. **Auto-completar:**
   - Escribe en el campo "Auto-completar" para ver sugerencias basadas en las palabras del primer texto.


5. **Encontrar palíndromo más largo:**
   - Haz clic en "Encontrar palíndromo más largo" para resaltar el palíndromo más largo en el primer texto (en verde).

6. **Encontrar similitud entre textos:**
   - Después de cargar dos archivos, haz clic en "Encontrar similitud".
   - La subcadena común más larga se resaltará en azul claro en ambos textos.

¡Disfruta usando el procesador de texto!
## Notas Adicionales

- La aplicación utiliza el algoritmo KMP para la búsqueda de patrones.
- El auto-completado se basa en una estructura de datos Trie.
- El algoritmo de Manacher se usa para encontrar el palíndromo más largo.
- La similitud entre textos se calcula usando el algoritmo LCS (Longest Common Subsequence).

## Contribuciones

Erick Segura Sánchez
- Implementación de algoritmo Trie
- Main.py
- Documentación

Alvaro Eduardo Lozano Medina
- Implementación de algoritmos KMP, Manacher y lcs