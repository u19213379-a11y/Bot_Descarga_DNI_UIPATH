# Nota sobre la anonimización del proyecto

Este repositorio corresponde a una automatización desarrollada y probada en un entorno real.

Para poder mostrar el trabajo técnico públicamente sin exponer información de terceros, se aplicaron las siguientes medidas:

- Eliminación de screenshots que contenían información visual del entorno real.
- Eliminación de archivos locales y datos temporales de ejecución.
- Sustitución de identificadores y URLs del Google Sheet.
- Sustitución del nombre del bot utilizado en producción/pruebas.
- Anonimización de identificadores de sesión de Telegram Web.
- Exclusión de identificadores personales usados durante las pruebas.

La arquitectura, las actividades de UiPath, los bucles, la lógica de descarga, los selectores dinámicos y el manejo de archivos permanecen visibles para revisión técnica.

## Para ejecutar el proyecto

El revisor debe sustituir los placeholders públicos por recursos propios:

- `REDACTED_GOOGLE_SHEET_ID`
- `PORTFOLIO_BOT`
- cualquier endpoint marcado como `REDACTED_SESSION`

Esta decisión permite demostrar el funcionamiento y diseño del proyecto sin publicar datos privados.
