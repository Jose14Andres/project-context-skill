# Project Context

Skill para Claude Code que levanta el contexto de un repositorio antes de planificar cambios. Resume el entorno y su estado, las funcionalidades y el alcance, la estructura y convenciones, y las restricciones explícitas o por confirmar.

## Instalación en un proyecto

Desde la raíz del proyecto, clona este repositorio en la carpeta de skills:

```bash
git clone https://github.com/Jose14Andres/project-context-skill.git .claude/skills/project-context
```

Para instalarla globalmente en tu usuario:

```bash
git clone https://github.com/Jose14Andres/project-context-skill.git ~/.claude/skills/project-context
```

## Uso

En Claude Code, ejecuta:

```
/project-context
```

La skill también puede activarse automáticamente cuando pidas entender un proyecto o establecer su contexto antes de planificar trabajo.

## Archivo principal

- [SKILL.md](SKILL.md): instrucciones para inspeccionar el proyecto y presentar los hallazgos con evidencia, sin modificar archivos durante el análisis.
