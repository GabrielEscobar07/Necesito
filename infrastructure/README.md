# Infraestructura

Esta carpeta almacenará configuraciones de infraestructura reproducibles.

```text
infrastructure/
├── docker/      # Dockerfiles y archivos relacionados
└── database/    # Inicialización, migraciones auxiliares y herramientas de MySQL
```

La instancia local de MySQL se levantará mediante Docker Compose cuando comience el Hito T2.

Cada proyecto y entorno usará una base y credenciales independientes. Necesito no compartirá tablas ni usuarios de base de datos con el Sistema Administrativo La Vieja TATTOO.

Las credenciales, archivos `.env` reales, copias de bases y datos persistentes locales nunca deben confirmarse en Git.