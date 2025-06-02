#CONCEPTOS FUNDAMENTALES DE GITHUB ACTIONS

🚀 GitHub Actions: Automatización en tu repositorio

🧩 ¿Qué es GitHub Actions?
GitHub Actions es una herramienta de GitHub que permite automatizar tareas dentro de tu repositorio, como pruebas, construcción de proyectos, despliegues y mucho más.

⚙️ ¿Cómo funciona?
Los workflows (flujos de trabajo) se definen en archivos YAML dentro de la carpeta .github/workflows/.
Estos workflows se activan automáticamente cuando ocurre un evento (por ejemplo, un push o un pull request).


🗝️ Conceptos clave

Workflow:
📄 Conjunto de procesos automatizados definidos en un archivo YAML.

Trigger:
⏰ Evento que activa el workflow (por ejemplo, push, pull request). Se configura con la palabra clave on.

Job:
🧱 Unidad de trabajo dentro del workflow. Los jobs pueden ejecutarse en paralelo y cada uno corre en un entorno independiente.

Step:
🪜 Pasos individuales dentro de un job. Se ejecutan uno tras otro y pueden ser comandos o acciones predefinidas.

Runner:
💻 Máquina virtual donde se ejecutan los jobs. GitHub ofrece runners con Ubuntu, Windows y macOS.


💡 Ejemplo sencillo
El archivo va en .github/workflows/namefile.yaml con el siguiente contenido:

name: CI Example

on: [push]

jobs:
  example-job:
    runs-on: ubuntu-latest
    steps:
      - name: Mostrar mensaje 1
        run: echo "¡Se detectó un nuevo push al repositorio!"

      - name: Mostrar mensaje 2
        run: echo "Ejecutando el workflow de ejemplo..."

      - name: Mostrar mensaje 3
        run: echo "✅ Todo finalizó correctamente."
        
📋 ¿Qué hace este workflow?
Se ejecuta automáticamente cada vez que subes cambios (push) a cualquier rama.
Muestra tres mensajes en la consola, simulando pasos de un proceso automatizado.
Es ideal para aprender la estructura básica de un workflow en GitHub Actions.
