# 🌌 CieloObs 

<div align="center">

![Flutter](https://img.shields.io/badge/Flutter-02569B?style=flat&logo=flutter&logoColor=white)
![Dart](https://img.shields.io/badge/Dart-0175C2?style=flat&logo=dart&logoColor=white)
![SQLite](https://img.shields.io/badge/SQLite-003B57?style=flat&logo=sqlite&logoColor=white)
![Platform](https://img.shields.io/badge/Platform-Android%20%7C%20iOS-lightgrey?style=flat)
![Status](https://img.shields.io/badge/Estado-En%20desarrollo-orange?style=flat)

**Diario de observaciones del cielo para República Dominicana 🇩🇴**  
Registra, documenta y comparte lo que ves en el cielo nocturno

[Reportar un bug](https://github.com/FJSaladin/skywatch_rd/issues)

</div>

---

## 📋 Descripción

CieloObs es una aplicación móvil desarrollada con Flutter que permite registrar y documentar observaciones del cielo: fenómenos atmosféricos, eventos astronómicos, aves migratorias, objetos luminosos y más. Cada observación puede incluir fotos, notas de voz, coordenadas GPS y condiciones del cielo, todo almacenado localmente en el dispositivo con SQLite.

---

## ✨ Funcionalidades

### Registro de observaciones
| Campo | Descripción |
|-------|-------------|
| 📝 **Título y descripción** | Texto libre con detalles del evento observado |
| 📅 **Fecha y hora** | Selector de fecha/hora con formato en español |
| 🏷️ **Categoría** | Fenómeno atmosférico, Astronomía, Aves migratorias, Aeronave, Fenómeno luminoso, Otro |
| ☁️ **Condiciones del cielo** | Despejado, parcialmente nublado, nublado, bruma, lluvia ligera |
| ⏱️ **Duración** | Duración estimada del evento en segundos |

### Multimedia
- 📸 **Foto** — captura desde cámara o elige desde galería, con vista previa en el formulario
- 🎙️ **Nota de voz** — grabación de audio `.m4a` con reproducción integrada
- 🗺️ **Mapa** — visualización de la ubicación exacta en OpenStreetMap (flutter_map)

### Ubicación
- 📍 **GPS automático** — captura de coordenadas con alta precisión (Geolocator)
- 📝 **Ubicación en texto** — descripción manual del lugar (ej: "Sector La Julia, Santo Domingo")
- Manejo de permisos con `permission_handler`

### Gestión del diario
- 📋 **Lista de observaciones** — ordenadas por fecha, con ícono por categoría y badges de foto/audio
- 🔍 **Filtro por categoría** — bottom sheet con chips para filtrar rápidamente
- 📤 **Exportar observación** — comparte los datos en formato JSON con `share_plus`
- 🗑️ **Eliminar** — por observación individual o borrado total con confirmación


---

## 🛠 Stack tecnológico

**Framework:** Flutter / Dart

**Dependencias principales:**

| Paquete | Uso |
|---------|-----|
| `sqflite` | Base de datos SQLite local |
| `provider` | Gestión de estado (ChangeNotifier) |
| `flutter_map` + `latlong2` | Mapa interactivo con OpenStreetMap |
| `geolocator` | Obtención de coordenadas GPS |
| `permission_handler` | Solicitud de permisos (cámara, mic, ubicación) |
| `image_picker` | Captura de fotos desde cámara/galería |
| `record` | Grabación de audio `.m4a` |
| `audioplayers` | Reproducción de notas de voz |
| `share_plus` | Exportar observaciones como JSON |
| `intl` | Formato de fechas en español |
| `path_provider` | Acceso al directorio de documentos |

---

## 🚀 Instalación y ejecución local

### Prerrequisitos
- [Flutter SDK](https://docs.flutter.dev/get-started/install) >= 3.0.0
- Android Studio o VS Code con extensión Flutter
- Dispositivo físico o emulador (Android / iOS)

### Pasos

```bash
# 1. Clonar el repositorio
git clone https://github.com/FJSaladin/skywatch_rd.git
cd skywatch_rd

# 2. Instalar dependencias
flutter pub get

# 3. Ejecutar en dispositivo/emulador
flutter run
```

### Permisos requeridos

La app solicita los siguientes permisos en tiempo de ejecución:

- **Ubicación** — para capturar coordenadas GPS de la observación
- **Cámara** — para tomar fotos del evento observado
- **Micrófono** — para grabar notas de voz



<div align="center">
  Hecho con ❤️ desde República Dominicana 🇩🇴
</div>
