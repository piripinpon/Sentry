# Sentry
Sentry es una herramienta de monitoreo de errores y rendimiento para aplicaciones.
¿Que hace?
Detecta errores automáticamente en tu código (excepciones, crashes, fallos).
Guarda información detallada del error:
Mensaje de error y stack trace.
Variables en el momento del fallo.
Usuario afectado (si aplica).
Sistema, navegador o entorno donde ocurrió.
Envía el error a un panel web (dashboard) en sentry.io
Permite a los desarrolladores:
Ver qué errores ocurren con más frecuencia.
Reproducirlos y depurarlos más rápido.
Recibir alertas (email, Slack, Discord, etc.) cuando algo falla.

Aqui esta el codigo de prueba, donde explicare lo que hace el codigo y que devuelve sentry al encontrar un error.
<img width="740" height="375" alt="image" src="https://github.com/user-attachments/assets/ff6cbd55-a753-44bb-82b6-0b31501b28ba" />

sentry_sdk.init(dsn=None)
Inicializa Sentry, pero con dsn=None.
El DSN (Data Source Name) es como la “llave” que conecta tu proyecto local con tu cuenta de Sentry en la nube.
Aquí está en None, así que no se manda a Sentry real, solo queda “activo” en modo local (simulación). 

Bloque try-except
Intenta ejecutar divide(10, 0) → esto produce un ZeroDivisionError.
Como el error ocurre, entra al except.

sentry_sdk.capture_exception(e)
Captura la excepción e y la enviaría al dashboard de Sentry (si tuvieras un DSN configurado).
Aquí solo se simula porque el DSN está en None. 

Como da el error pasamos except donde aparecera un mensaje de mostrando que se ha capturado el error, al momento de compilar da este resultado.
<img width="563" height="432" alt="image" src="https://github.com/user-attachments/assets/b2a15456-7a9f-4aa0-91fd-2bdf81879341" />

Lo excelente de sentry es que te captura los errores, te dice donde y te los reporta.
