# 📄 Guía de Actualización de Plantillas (Sistema JSON)

Este simulador permite actualizar los equipos y sus jugadores de forma masiva mediante archivos `.json`. Puedes usar este sistema tanto para añadir equipos nuevos como para actualizar las valoraciones y plantillas de la temporada 2025/26.

---

## 🛠️ Estructura del JSON (Plantilla)

Copia este código y guárdalo como un archivo `.json` (ej: `madrid_update.json`) para importarlo en la app:

```json
{
  "name": "Nombre del Equipo",
  "league": "Mis Equipos",
  "formation": "4-3-3",
  "players": [
    {
      "name": "Nombre Jugador",
      "number": 10,
      "position": "ST",
      "offensiveRating": 85,
      "defensiveRating": 40,
      "form": 75,
      "starter": true
    },
    {
      "name": "Nombre Suplente",
      "number": 22,
      "position": "CM",
      "offensiveRating": 70,
      "defensiveRating": 65,
      "form": 60,
      "starter": false
    }
  ]
}
```

---

## 📋 Especificaciones de Campos

| Campo | Descripción | Valores permitidos |
| :--- | :--- | :--- |
| `name` | Nombre exacto del equipo. | Si el nombre ya existe, se actualizará. |
| `formation` | Formación táctica por defecto. | `4-3-3`, `4-4-2`, `3-5-2`, `4-2-3-1`, etc. |
| `position` | Posición del jugador. | `GK`, `CB`, `LB`, `RB`, `CDM`, `CM`, `CAM`, `LW`, `RW`, `ST`. |
| `ratings` | Valoraciones de 0 a 100. | Enteros entre 0 y 100. |
| `starter` | Define si el jugador es titular. | `true` (titular) / `false` (suplente). |

---

## 🚀 Cómo aplicar la actualización en la App

1. **Prepara tu archivo:** Crea el JSON siguiendo la plantilla anterior con los datos actualizados.
2. **Abre la App:** Ve a la pantalla principal (**Simular**).
3. **Importar:** Toca el icono de **Subida (FileUpload)** en la barra superior.
4. **Selecciona el archivo:** Busca el `.json` en el explorador de archivos de tu dispositivo.
5. **¡Listo!:** 
   - Si el equipo **ya existe**, sus jugadores serán reemplazados por los nuevos datos del JSON.
   - Si el equipo **es nuevo**, se creará automáticamente en la categoría "Mis Equipos".

> [!TIP]
> **Consejo:** Asegúrate de incluir al menos 11 jugadores titulares para que el motor de simulación funcione de forma óptima desde el primer momento.

---

## ¿Por qué usar este sistema?
*   **Actualizaciones Rápidas:** No necesitas editar uno a uno en la UI.
*   **Comunidad:** Puedes compartir tus archivos JSON con otros usuarios para tener las ligas siempre al día.
*   **Precisión:** Permite ajustar los `ratings` de ataque y defensa de forma mucho más granular.
