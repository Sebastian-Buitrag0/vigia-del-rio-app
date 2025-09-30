# Vigia del Rio App

Aplicación móvil que se conecta a la API para mostrar la información recibida y generar alertas en tiempo real al usuario.

## Gestión de versiones de Flutter con FVM

Este proyecto utiliza Flutter Version Manager (FVM) para gestionar la versión de Flutter.

### Configuración inicial

1. **Instalar FVM globalmente:**

   ```bash
   dart pub global activate fvm
   ```

2. **La versión de Flutter está configurada en el archivo `.fvmrc`:**
   ```json
   {
     "flutter": "3.35.5"
   }
   ```

### Comandos útiles con FVM

- **Instalar la versión de Flutter del proyecto:**

  ```bash
  fvm install
  ```

- **Usar Flutter a través de FVM:**

  ```bash
  fvm flutter --version
  fvm flutter doctor
  fvm flutter pub get
  fvm flutter run
  ```

- **Compilar para diferentes plataformas:**

  ```bash
  # Web
  fvm flutter build web

  # Android
  fvm flutter build apk

  # iOS (solo en macOS)
  fvm flutter build ios
  ```

### Desarrollo

Para ejecutar la aplicación en modo de desarrollo:

```bash
fvm flutter run
```

Para web específicamente:

```bash
fvm flutter run -d chrome
```

### Estructura del Proyecto

```
├── lib/               # Código principal de la aplicación
├── android/           # Configuración específica para Android
├── ios/               # Configuración específica para iOS
├── web/               # Configuración específica para Web
├── test/              # Pruebas unitarias
├── .fvm/              # Directorio de FVM (ignorado por git)
├── .fvmrc            # Configuración de versión de Flutter
└── pubspec.yaml       # Dependencias del proyecto
```

### Notas importantes

- El directorio `.fvm/` está incluido en `.gitignore` y no debe ser versionado
- Todos los miembros del equipo deben usar `fvm flutter` en lugar de `flutter` directamente
- Para cambiar la versión de Flutter del proyecto: `fvm use <version>`
