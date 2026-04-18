# cicd-pipeline-python

1. ¿Qué ventajas le proporciona a un proyecto el uso de un pipeline de CI? Menciona al menos tres ventajas específicas y explica por qué son importantes.
- Permite detectar errores de forma temprana para que no lleguen a producción.
- Automatiza pruebas y validaciones para reducir las tareas manuales. 
- Mejora la calidad del código al integrar herramientas de análisis continuo.


2. ¿Cuál es la diferencia principal entre una prueba unitaria y una prueba de aceptación? Da un ejemplo de algo que probarías con una prueba unitaria y algo que probarías con una prueba de aceptación (en el contexto de cualquier aplicación que conozcas, descríbela primero).
La prueba unitaria sirve para probar funciones específicas, únicamente viendo si funciona. Las pruebas de aceptación verifican en el contexto completo, como si fuera un usuario final.
Para el ejemplo, una prueba unitaria para Amazon puede ser que el carrito calcule correctamente la suma de los precios de los productos y muestre el total del pedido, mientras que la prueba de aceptación puede ser que un uusario pueda entrar a la página hacer un pedido correctamente.


3. Describe brevemente qué hace cada uno de los steps principales de tu workflow de GitHub Actions (desde el checkout hasta el push de Docker). Explica el propósito de cada uno (qué hace y para qué se hace).
Se empieza con el checkout del código y configuración del entorno, luego instala las dependencias y ejecuta las herramientas de calidad del código. Después corre pruebas unitarias y de aceptación. Finalmente, realiza el análisis en SonarCloud y si todo está correcto construye y publica la imagen Docker en Docker Hub.


4. ¿Qué problemas o dificultades encontraste al implementar este taller? ¿Cómo los solucionaste? (Si no encontraste ningún problema, describe algo nuevo que hayas aprendido).
La mayor dificultad que encontramos fue que pasara la prueba de calidad de SonarCloud, se solucionó investigando el por qué no pasó las pruebas de calidad y corrigiendo los errores directamente. Algo que aprendimos todos fue el uso de herramientas como black que modifican el código para que tenga ciertos estándares de la industria.


5. ¿Qué ventajas ofrece empaquetar la aplicación en una imagen Docker al final del pipeline en lugar de simplemente validar el código?
2 ventajas que detectamos son qué permite que la app funcione en cualquier máquina/entorno, ya que el empaquetado define las dependencias y sobre qué tecnologías va a trabajar. Otra ventaja es que al generar la imágen al final del pipeline, hace más fácil y rápido el proceso de despliegue.