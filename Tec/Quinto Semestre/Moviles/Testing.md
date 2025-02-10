Links: [[Moviles]]

Las pruebas son una parte fundamental en el ciclo de vida del desarrollo de aplicaciones Android, ya que permiten garantizar la calidad y el correcto funcionamiento de la aplicación. Las herramientas y frameworks disponibles en el ecosistema Android permiten realizar pruebas automáticas y eficaces. Este resumen se centra en los aspectos más importantes de las pruebas en Android, abarcando desde los fundamentos hasta las herramientas avanzadas.

### Fundamentos de las pruebas en Android

Las pruebas en Android se dividen en varias categorías según el tipo de pruebas y los objetivos que se buscan alcanzar. Los principales tipos de pruebas incluyen:

1. **Pruebas Unitarias**: Validan el comportamiento de unidades de código pequeñas y aisladas, como funciones individuales. Estas pruebas se ejecutan de forma local en la máquina del desarrollador sin depender del framework Android.
    
2. **Pruebas de Instrumentación**: Son aquellas que se ejecutan en un dispositivo o emulador Android, y que interactúan con la interfaz de usuario o recursos del sistema operativo. Estas pruebas permiten validar cómo funciona la aplicación en su entorno real.
    
3. **Pruebas de Integración**: Se enfocan en verificar que diferentes componentes de la aplicación interactúen correctamente entre sí. Este tipo de pruebas asegura que los módulos combinados funcionen como se espera.
    

Dentro de las pruebas instrumentadas, existen herramientas como **AndroidX Test**, que proporciona un conjunto de APIs y herramientas para escribir y ejecutar pruebas en dispositivos Android. Algunas de las bibliotecas más usadas en este contexto son:

- **Espresso**: Es una herramienta diseñada para escribir pruebas funcionales que interactúan con la interfaz de usuario.
- **JUnit**: Es el framework de pruebas unitarias que permite organizar y ejecutar pruebas.

### Duplicados de pruebas

Para evitar las dependencias reales que pueden hacer que las pruebas sean lentas o inestables, es común utilizar "doubles" o sustitutos en las pruebas, tales como mocks o stubs. Estos elementos imitan el comportamiento de las dependencias reales, pero en un entorno controlado, permitiendo a los desarrolladores enfocarse en la lógica de su código.

### Pruebas locales y pruebas instrumentadas

Las pruebas locales se ejecutan directamente en la máquina de desarrollo sin necesidad de un dispositivo o emulador Android. Estas pruebas suelen ser más rápidas porque no requieren acceso a APIs o componentes del sistema operativo.

Por otro lado, las pruebas instrumentadas se ejecutan en un dispositivo real o un emulador, lo que permite probar la interacción de la aplicación con el entorno Android. Es posible utilizar varias bibliotecas, como las de **Espresso**, para interactuar con la interfaz de usuario o servicios de la aplicación.

### Pruebas de interfaz de usuario con Espresso

Espresso es una de las bibliotecas más importantes para realizar pruebas de interfaz de usuario en aplicaciones Android. Su simplicidad para interactuar con elementos de la UI y su robustez al sincronizarse automáticamente con la interfaz la convierten en una herramienta esencial.

Entre las características principales de Espresso se incluyen:

- Interacciones con la UI mediante métodos sencillos, como `onView()`, que permite realizar acciones como clics o verificaciones de texto.
- Soporte para la automatización de tareas complejas como la gestión de listas o la simulación de múltiples procesos.
- Posibilidad de trabajar con recursos inactivos (idling resources), lo que garantiza que las pruebas esperen hasta que la aplicación esté lista antes de interactuar con la UI.

### Pruebas en diferentes componentes y pantallas

Android permite realizar pruebas específicas para componentes como **servicios** y **content providers**. Además, las pruebas en múltiples tamaños de pantalla o configuraciones de dispositivos se vuelven cruciales para garantizar que la aplicación funcione correctamente en diferentes dispositivos.

Herramientas como **UI Automator** permiten ejecutar pruebas funcionales en aplicaciones incluso si no tenemos acceso al código fuente, lo cual es útil para validar interacciones complejas entre aplicaciones y el sistema operativo Android.

### Integración continua y automatización de pruebas

La integración continua (CI) es un proceso que permite integrar cambios de código de forma continua y automática, asegurando que todo funcione correctamente en conjunto. Herramientas como **Jenkins** o **GitLab CI** son muy usadas para configurar pipelines de pruebas automáticas.

La automatización de pruebas dentro de un entorno de integración continua ayuda a identificar problemas rápidamente, asegurando que los desarrolladores reciban retroalimentación casi en tiempo real.
