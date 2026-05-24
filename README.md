# FootballSim
⚽ Simulador de partidos de fútbol para Android. Motor probabilístico con modelo xG, distribución de Poisson y Monte Carlo. 114 clubes reales · Top 5 ligas europeas · Generación de alineaciones con sistema de lesiones y disponibilidad. Kotlin · Jetpack Compose · Room · MVVM.
{
  "guide_title": "Guía de Actualización de Plantillas (Sistema JSON)",
  "description": "Usa este archivo como plantilla para importar o actualizar equipos en Football Simulator.",
  "how_to_use": [
    "1. Modifica los campos de este JSON con la información de tu equipo.",
    "2. Guarda el archivo con extensión .json.",
    "3. En la app, ve a la pestaña Simular y toca el icono de Importar (Nube/Flecha).",
    "4. Si el nombre del equipo coincide con uno existente, se actualizará. Si no, se creará uno nuevo."
  ],
  "fields_reference": {
    "name": "Nombre exacto del equipo.",
    "league": "Categoría donde aparecerá (ej: Mis Equipos).",
    "formation": "Formación táctica: 4-3-3, 4-4-2, 3-5-2, 4-2-3-1, 5-3-2, 4-5-1, 3-4-3.",
    "players": {
      "position": "GK, CB, LB, RB, CDM, CM, CAM, LW, RW, ST.",
      "ratings": "Valor de 0 a 100 para offensiveRating, defensiveRating y form.",
      "starter": "true para el 11 inicial, false para suplentes."
    }
  },
  "template_example": {
    "name": "Ejemplo FC",
    "league": "Mis Equipos",
    "formation": "4-3-3",
    "players": [
      {
        "name": "Portero Estrella",
        "number": 1,
        "position": "GK",
        "offensiveRating": 10,
        "defensiveRating": 90,
        "form": 80,
        "starter": true
      },
      {
        "name": "Capitán Centro",
        "number": 8,
        "position": "CM",
        "offensiveRating": 75,
        "defensiveRating": 75,
        "form": 85,
        "starter": true
      },
      {
        "name": "Goleador Rápido",
        "number": 9,
        "position": "ST",
        "offensiveRating": 92,
        "defensiveRating": 20,
        "form": 90,
        "starter": true
      },
      {
        "name": "Suplente Promesa",
        "number": 20,
        "position": "LW",
        "offensiveRating": 70,
        "defensiveRating": 30,
        "form": 65,
        "starter": false
      }
    ]
  }
}
