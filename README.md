# UiPath RPA – Automatización de descarga y organización documental

Proyecto de portafolio desarrollado con **UiPath** para automatizar un flujo repetitivo de consulta, descarga y organización de documentos desde aplicaciones web.

## Objetivo

El robot automatiza un proceso que, de forma manual, requiere:

1. Leer un identificador desde una hoja de cálculo.
2. Enviar la consulta correspondiente a una aplicación web.
3. Detectar dinámicamente los documentos/imágenes generados.
4. Descargar las dos caras del documento.
5. Renombrar los archivos siguiendo una convención estable.
6. Moverlos a una carpeta de salida.
7. Marcar el registro como procesado.
8. Continuar automáticamente con el siguiente registro.

## Tecnologías y conceptos utilizados

- UiPath Studio
- UI Automation
- Selectores dinámicos
- Google Sheets / navegador
- Automatización de Telegram Web
- Lectura del portapapeles
- Bucles `While`
- Variables y expresiones Visual Basic
- Manejo, renombrado y movimiento de archivos
- Identificación dinámica de elementos del DOM
- Control de registros procesados

## Decisión técnica destacada

Durante el desarrollo se evitó depender de selectores visuales asociados a una imagen concreta.  
El flujo localiza dinámicamente los últimos elementos de tipo imagen dentro del contenedor de conversación y trabaja con esos elementos en tiempo de ejecución. Esto permite que el robot continúe funcionando aunque cambie el contenido visual de cada documento.

## Privacidad y versión pública

**Esta es una versión saneada para portafolio.**

El proyecto original fue desarrollado sobre un entorno real. Por protección de datos:

- se eliminaron las capturas de pantalla del entorno real;
- se retiraron cachés y datos temporales de ejecución;
- el identificador real de la hoja de cálculo fue sustituido;
- el nombre del bot utilizado en el entorno real fue sustituido;
- las URLs/sesiones específicas fueron anonimizadas;
- no se incluyen documentos ni identificadores personales reales.

La lógica principal del flujo se conserva. Para ejecutarlo en otro entorno deben configurarse los endpoints y datos propios.

> La anonimización es intencional y forma parte de las buenas prácticas de seguridad al publicar automatizaciones desarrolladas con datos reales.

## Flujo simplificado

```text
Hoja de cálculo
      ↓
Leer registro pendiente
      ↓
Consultar aplicación web
      ↓
Detectar documentos generados
      ↓
Descargar frente y reverso
      ↓
Renombrar y mover archivos
      ↓
Marcar registro como procesado
      ↓
Siguiente registro
```

## Archivos principales

- `Main.xaml`: flujo principal de la automatización.
- `project.json`: configuración y dependencias del proyecto.
- `project.uiproj`: definición del proyecto UiPath.
- `.objects/`: repositorio de objetos/selectores, con referencias sensibles anonimizadas.

## Dependencias

El proyecto utiliza, entre otras:

- UiPath.GSuite.Activities
- UiPath.System.Activities
- UiPath.UIAutomation.Activities

## Nota para revisión técnica

Las referencias anonimizadas aparecen con valores como:

- `REDACTED_GOOGLE_SHEET_ID`
- `PORTFOLIO_BOT`
- `REDACTED_SESSION`

Estos valores sustituyen únicamente información del entorno real; no representan una limitación de la lógica implementada.
