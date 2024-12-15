# ScreanMatch-Libros-Estadisticas
Utilizamos API para informacion de libors y analizar su estadisticas

# 📚 Explorador de Libros - Proyecto con la API de Gutendex

Este proyecto es una aplicación que consume la API pública de **Gutendex**, una increíble base de datos que contiene información sobre más de 72,000 libros. La aplicación permite realizar búsquedas específicas, analizar estadísticas, y explorar datos como el título, los autores, el idioma y el número de descargas de los libros. Este desafío pone en práctica habilidades avanzadas de consumo de APIs, manejo de datos y generación de estadísticas.

---

## 🚀 ¿Qué hace esta aplicación?

1. **Consumo de la API de Gutendex**:
   - Obtiene información detallada sobre libros, como el título, los autores, el idioma y el número de descargas.
   - No requiere autenticación ni API Key, lo que simplifica su uso.

2. **Búsquedas Avanzadas**:
   - Permite buscar libros por:
     - ID del libro.
     - Idioma (incluyendo libros en español).
     - Rango de años en los que los autores estuvieron vivos.
     - Términos específicos en el título (e.g., *Quijote*).

3. **Top 10 de Libros Más Descargados**:
   - Calcula y muestra una lista con los libros más descargados en formato digital.

4. **Estadísticas de Descargas**:
   - Genera métricas relevantes sobre las descargas:
     - Media de descargas.
     - Máximo y mínimo número de descargas.
     - Total de registros analizados.

5. **Transformación de Datos**:
   - Convierte los datos de la API en objetos propios de la aplicación para un manejo más eficiente y personalizado.

---

## 📂 Estructura del Proyecto

```plaintext
.
├── src
│   ├── main
│   │   ├── java
│   │   │   ├── com.example.gutendexapp
│   │   │   │   ├── Book.java                 # Modelo para representar un libro
│   │   │   │   ├── Author.java               # Modelo para representar un autor
│   │   │   │   ├── ApiClient.java            # Cliente para consumir la API de Gutendex
│   │   │   │   ├── BookService.java          # Lógica para manejo y filtrado de libros
│   │   │   │   ├── StatisticsService.java    # Servicio para calcular estadísticas
│   │   │   │   ├── GutendexApplication.java  # Clase principal
│   │   │   │   └── Utils.java                # Métodos auxiliares
│   │   ├── resources
│   │   │   ├── application.properties        # Configuración del proyecto
│   │   │   └── books                         # Carpeta con archivos JSON generados
│   ├── test
│   │   ├── java
│   │   │   ├── com.example.gutendexapp       # Tests unitarios
├── README.md                                  # Documentación del proyecto
```

---

## 🛠️ Tecnologías Utilizadas

- **Lenguaje**: Java.
- **Framework**: Spring Framework (Spring Boot).
- **HTTP Client**: RestTemplate (integrado con Spring).
- **Gestión de JSON**: Gson o Jackson para manejar respuestas de la API.
- **Streams y Lambdas**: Para manipulación y filtrado de datos.
- **DoubleSummaryStatistics**: Para generar estadísticas detalladas.
- **Optional**: Para manejar datos faltantes de forma segura.

---

## 🔧 Configuración y Ejecución

1. **Clonar el Repositorio**:
   ```bash
   git clone https://github.com/tuusuario/gutendex-book-explorer.git
   cd gutendex-book-explorer
   ```

2. **Configurar la API**:
   - No se requiere configuración adicional. La API de Gutendex está disponible en:  
     `https://gutendex.com/books/`

3. **Compilar y Ejecutar**:
   - Con **Maven** o **Gradle**, ejecuta:
     ```bash
     mvn spring-boot:run
     ```
   - O usa tu IDE favorito para correr la aplicación.

---

## 📝 Funcionalidades

1. **Buscar Libros**:
   - Búsquedas avanzadas basadas en criterios como:
     - Idioma.
     - Términos en el título.
     - Rango de años de vida de los autores.

2. **Top 10 Libros Más Descargados**:
   - Muestra una lista con los libros digitales más descargados.

3. **Generar Estadísticas**:
   - Calcula métricas clave usando `DoubleSummaryStatistics`:
     - Media de descargas.
     - Máximo y mínimo de descargas.
     - Total de registros analizados.

4. **Exportar Datos**:
   - Guarda los resultados en archivos JSON para un análisis posterior.

---

## 📝 Ejemplo de Salida

### Top 10 de Libros Más Descargados:
```plaintext
1. Título: Don Quijote de la Mancha
   Autor: Miguel de Cervantes
   Descargas: 23,456

2. Título: Pride and Prejudice
   Autor: Jane Austen
   Descargas: 21,890

...
```

### Archivo JSON (books/top_books.json):
```json
[
  {
    "title": "Don Quijote de la Mancha",
    "author": "Miguel de Cervantes",
    "downloads": 23456
  },
  {
    "title": "Pride and Prejudice",
    "author": "Jane Austen",
    "downloads": 21890
  }
]
```

---

## 🎯 Aprendizajes

### 💡 Consumo de API:
- Aprendí a interpretar y consumir una API pública utilizando documentación en inglés, con parámetros de búsqueda avanzados.

### 📊 Análisis de Datos:
- Generación de estadísticas clave con `DoubleSummaryStatistics`.
- Filtrado y manipulación de datos con Streams y Lambdas.

### 📂 Transformación de Datos:
- Manejo eficiente de listas anidadas (listas dentro de listas) y conversión de datos JSON en objetos Java.

### 🔍 Optional y Manejo Seguro:
- Uso de `Optional` para evitar referencias nulas al trabajar con datos faltantes.

---

## 🌟 Funcionalidades Futuras

- Añadir búsquedas basadas en géneros literarios.
- Implementar una interfaz web para mostrar los datos.
- Comparar autores o libros por popularidad a lo largo de los años.

---

## 🏷️ Etiquetas

`#Java` `#APIs` `#Gutendex` `#JSON` `#SpringFramework` `#Streams` `#DoubleSummaryStatistics`

---

Espero que este `README.md` te sea útil para documentar tu proyecto de manera clara y profesional. Si necesitas ajustes o personalizaciones, ¡no dudes en pedírmelo! 🚀📚
