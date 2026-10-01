# Fundamentación UX/UI — AlertCom
## “Reporta. Ubica. Mejora.”

### 1. Descripción del proyecto

AlertCom es un prototipo de aplicación móvil orientado a facilitar el reporte ciudadano de baches, hoyos, grietas y otros daños en el pavimento de la ciudad de Temuco. Su propósito es ofrecer una interfaz sencilla para que las personas puedan identificar daños viales, seleccionar su tipo y gravedad, y visualizar información relacionada con los reportes.

La aplicación está desarrollada con Python, Kivy y KivyMD, utilizando componentes de interfaz basados en Material Design 3. El prototipo contempla seis pantallas principales: aviso de seguridad, inicio de sesión, pantalla de inicio con mapa simulado, formulario de reporte, historial de reportes y perfil del usuario.

### 2. Problema identificado y usuarios objetivo

Los daños en el pavimento pueden dificultar el desplazamiento de conductores, ciclistas y peatones, además de representar riesgos para la seguridad vial. Por ello, AlertCom propone una interfaz que permita organizar la información de estos problemas y facilite su comunicación mediante un flujo de navegación sencillo.

Los usuarios objetivo son ciudadanos de Temuco que desean informar sobre daños en las calles y consultar el estado de los reportes. La aplicación busca reducir la dificultad de encontrar una opción para reportar un problema vial y presentar la información de forma comprensible.

### 3. Fundamentación UX (experiencia de usuario)

El diseño de AlertCom prioriza la facilidad de uso, la claridad de las acciones y la reducción de pasos innecesarios.

**Navegación sencilla:** la pantalla principal ofrece acceso al formulario de reporte, al historial y al perfil del usuario. Esto permite identificar las funciones principales sin recorrer múltiples menús.

**Prevención de errores:** el formulario solicita seleccionar el tipo y la gravedad del daño antes de enviar el reporte. Además, la aplicación presenta mensajes informativos cuando faltan datos obligatorios.

**Seguridad del usuario:** la primera pantalla presenta un aviso que recomienda no utilizar la aplicación mientras se conduce y estacionar en un lugar seguro antes de realizar un reporte.

**Retroalimentación:** se utilizan mensajes emergentes para informar sobre la validación del inicio de sesión, la fotografía simulada y el envío del reporte. Así, el usuario recibe una respuesta visual después de realizar una acción.

**Organización de la información:** el historial muestra ejemplos de reportes con su tipo, gravedad y estado, mientras que el perfil presenta información general y estadísticas de actividad.

### 4. Fundamentación UI (interfaz de usuario)

La interfaz utiliza una apariencia visual basada en Material Design 3 mediante KivyMD. Se emplea un tema oscuro y una paleta naranja como color principal para destacar acciones relevantes, como los botones y los elementos de interacción.

Los iconos representan acciones y conceptos conocidos, como seguridad, ubicación, fotografía, envío de reportes, historial y perfil. Los títulos, las etiquetas y los campos de entrada mantienen una jerarquía visual que ayuda a comprender la función de cada sección.

Los botones presentan textos directos, como “Entendido”, “Iniciar Sesión”, “Reportar bache”, “Enviar Reporte” y “Cerrar Sesión”. Los campos del formulario están agrupados por función para facilitar la lectura y el ingreso de información.

El diseño considera una resolución de referencia de 360 × 640 píxeles para simular un dispositivo móvil en el entorno de escritorio. Las pantallas que contienen formularios o información extensa incorporan desplazamiento vertical cuando corresponde.

### 5. Estructura y navegación

El prototipo se organiza en seis pantallas:

1. **SafetyScreen:** muestra un aviso de seguridad antes de utilizar la aplicación.
2. **LoginScreen:** permite ingresar un correo electrónico y una contraseña, con validaciones básicas.
3. **HomeScreen:** presenta una representación visual de un mapa de Temuco y el acceso al formulario de reporte.
4. **ReportScreen:** permite seleccionar el tipo y la gravedad del daño, simular la incorporación de una fotografía y escribir una descripción opcional.
5. **HistoryScreen:** muestra ejemplos de reportes con diferentes estados de seguimiento.
6. **ProfileScreen:** presenta datos de ejemplo del ciudadano, estadísticas y la opción de cerrar sesión.

La navegación se implementa mediante `ScreenManager` y `SlideTransition`, que permiten cambiar entre pantallas con transiciones laterales. También se incorporan botones para regresar a la pantalla principal y una barra de navegación inferior para acceder a Inicio, Mis Reportes y Perfil.

### 6. Validaciones e interacciones

El inicio de sesión comprueba que los campos no estén vacíos, que el correo tenga un formato básico válido y que la contraseña contenga al menos cuatro caracteres.

En el formulario de reporte se exige simular una fotografía y seleccionar un tipo y una gravedad antes de continuar. La descripción es opcional y cuenta con un límite de 250 caracteres.

Estas validaciones buscan prevenir entradas incompletas y proporcionar mensajes comprensibles al usuario. Sin embargo, las comprobaciones implementadas corresponden a un prototipo y no representan un sistema de autenticación seguro ni un servicio real de registro ciudadano.

### 7. Accesibilidad y facilidad de uso

Se utilizan textos descriptivos en los botones, iconos asociados a sus funciones y una distribución visual por secciones. Los campos y controles cuentan con indicaciones que orientan al usuario sobre la información requerida.

Como mejora futura, se propone comprobar el contraste de los textos, evaluar el tamaño de los elementos táctiles, mejorar la adaptación a distintas resoluciones y realizar pruebas de usabilidad con usuarios reales.

### 8. Limitaciones del prototipo y mejoras futuras

AlertCom corresponde a un prototipo funcional de interfaz. Algunas características son representaciones simuladas:

- El inicio de sesión no verifica las credenciales mediante un servidor ni crea cuentas reales.
- El mapa de Temuco es una representación visual estática y no utiliza cartografía interactiva.
- La fotografía y las coordenadas GPS se simulan mediante valores predefinidos; no se accede a la cámara ni a la ubicación real del dispositivo.
- El historial contiene registros de ejemplo y no persiste automáticamente los nuevos reportes.
- Los estados de seguimiento y las estadísticas son datos demostrativos, no información obtenida de una municipalidad.

Como trabajo futuro, se propone incorporar almacenamiento persistente, integración con un servicio de mapas, captura de fotografías, geolocalización real, autenticación segura y un mecanismo de comunicación con las entidades responsables del mantenimiento vial.

### 9. Conclusión

La propuesta UX/UI de AlertCom busca facilitar el reporte ciudadano de daños viales mediante una interfaz organizada, navegación directa, validaciones básicas y retroalimentación visual. El prototipo permite demostrar el flujo principal de interacción y visualizar cómo podría funcionar una aplicación destinada a mejorar la comunicación de problemas de infraestructura vial.

Las decisiones de diseño priorizan la claridad, la facilidad de uso y la seguridad del usuario. Las funciones simuladas y las limitaciones identificadas permiten establecer una base para futuras mejoras técnicas y de experiencia de usuario.