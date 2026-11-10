# Content Critic

Skill para Claude que evalúa guiones, hooks, posts y Reels **antes de publicarlos** en Instagram, TikTok, LinkedIn o X.

No promete predecir la viralidad: ningún modelo puede hacerlo sin datos reales de rendimiento. Analiza la calidad de ejecución frente a lo que premia cada plataforma y propone mejoras concretas, ya reescritas.

## Qué hace

- Pide en un solo mensaje los datos mínimos: plataforma y formato, nicho y objetivo, tamaño de la cuenta y contenido completo.
- Evalúa por dimensiones (Alto / Medio / Bajo) con un diagnóstico de una línea: hook, retención, valor, emoción, encaje con la plataforma, disparador de acción y tendencia. En texto, la retención se sustituye por estructura.
- Solo puntúa la tendencia si la ha verificado con búsqueda web.
- Distingue lo seguro, lo probable y lo supuesto. No inventa datos ni da notas de 0 a 100.

## Qué devuelve

1. **Veredicto** global con nivel de confianza.
2. **Lo que más lo frena**, lo más incómodo primero.
3. **Tabla de dimensiones.**
4. **Hasta 3 fixes**, cada uno con su versión reescrita.
5. **Pendiente por probar**: qué validar publicando y qué métrica mirar.

## Instalación

### Claude (web o escritorio)

1. Descarga [`content-critic.skill`](content-critic.skill).
2. En Claude, ve a **Configuración → Capacidades → Skills** y sube el archivo.
3. Actívala y pide, por ejemplo: «Evalúa este hook para un Reel de Instagram».

### Claude Code

Copia la carpeta de la skill en tu directorio de skills:

```bash
git clone https://github.com/<tu-usuario>/content-critic.git
cp -r content-critic/content-critic ~/.claude/skills/
```

Reinicia Claude Code; la skill se carga sola cuando pidas puntuar o mejorar contenido.

## Estructura

```
content-critic/
  SKILL.md            # instrucciones de la skill
content-critic.skill  # paquete listo para subir a Claude
```

## Licencia

[MIT](LICENSE)
