# Descargas de Quantro

Instaladores oficiales de las apps de [Quantro](https://quantroos.com).

## Quantro Time para Mac

Registra automáticamente tu tiempo y tu actividad y los envía al módulo de Tiempo de Quantro. Requiere macOS 11 (Big Sur) o posterior y una cuenta de Quantro.

| Tu Mac | Descarga |
|---|---|
| Apple Silicon (M1, M2, M3, M4…) | [Quantro-Time-mac-arm64.dmg](https://github.com/josh0797/quantro-downloads/releases/latest/download/Quantro-Time-mac-arm64.dmg) |
| Intel | [Quantro-Time-mac-x64.dmg](https://github.com/josh0797/quantro-downloads/releases/latest/download/Quantro-Time-mac-x64.dmg) |

¿No sabes cuál es tu Mac? Menú Apple → **Acerca de esta Mac**: si dice *Chip Apple M…*, es Apple Silicon; si dice *Procesador Intel*, es Intel.

Los enlaces de arriba siempre descargan la versión más reciente. Todas las versiones están en [Releases](https://github.com/josh0797/quantro-downloads/releases), con su archivo `SHA256SUMS.txt` para verificar la descarga (`shasum -a 256 Quantro-Time-mac-arm64.dmg`).

## Abrir Quantro Time por primera vez (Gatekeeper)

Quantro Time todavía no está firmada ni notarizada por Apple, así que macOS la bloquea la primera vez que la abres. Solo tienes que desbloquearla una vez.

### Opción A: con Terminal (recomendada, funciona siempre)

1. Arrastra **Quantro Time** a la carpeta **Aplicaciones** (desde el `.dmg`).
2. Abre **Terminal** (Aplicaciones → Utilidades → Terminal), pega esta línea y pulsa Intro:

   ```
   xattr -dr com.apple.quarantine "/Applications/Quantro Time.app"
   ```

3. Abre Quantro Time normalmente.

El comando solo quita a Quantro Time la marca de "descargado de internet" que macOS pone a cada archivo. No desactiva Gatekeeper para ninguna otra app.

### Opción B: sin Terminal

1. Abre Quantro Time desde **Aplicaciones**. macOS mostrará un aviso y no la abrirá; pulsa **OK** o **Listo**.
2. Ve a **Configuración del Sistema → Privacidad y seguridad** y baja hasta **Seguridad**.
3. Junto a *Se bloqueó el uso de "Quantro Time"*, pulsa **Abrir de todos modos** y confirma con tu contraseña o Touch ID.

Si el aviso dice que la app **"está dañada y no se puede abrir"**, no aparece el botón *Abrir de todos modos*: usa la opción A. La app no está dañada; macOS muestra ese mensaje a las apps que no tienen la firma de un desarrollador registrado con Apple.

### Permisos que pide

Quantro Time vive en la barra de menús (no aparece en el Dock). Para registrar tu tiempo, macOS te pedirá permisos la primera vez; actívalos en **Configuración del Sistema → Privacidad y seguridad**:

- **Accesibilidad**: para medir tu nivel de actividad. Solo cuenta eventos de teclado y ratón; nunca registra lo que escribes ni dónde haces clic.
- **Grabación de pantalla**: macOS la exige para leer el nombre de la ventana activa. Quantro Time no graba ni envía capturas de pantalla.
- **Automatización** (Safari, Chrome…): para leer la dirección de la pestaña activa del navegador y registrar el tiempo por sitio web.

Si cambias un permiso, cierra Quantro Time desde la barra de menús y vuelve a abrirla.

## Soporte

Escríbenos a soporte@quantroos.com.

Windows y Android: próximamente.
