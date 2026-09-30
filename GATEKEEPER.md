# Cómo abrir Quantro Time en tu Mac

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

### Conectar tu cuenta

Quantro Time está incluida en los planes **Pro** y **Enterprise** de Quantro.

1. Al abrirla por primera vez aparece su ventana. Pulsa **Conectar cuenta**.
2. Inicia sesión con tu cuenta de Quantro en la ventana que se abre. Se cierra sola en cuanto la sesión queda conectada.
3. La ventana principal mostrará **Activo**. Tu tiempo se envía a Quantro cada 5 minutos; si no hay internet, se guarda y se envía después.

Si tu plan no incluye Quantro Time, la app te lo dirá y dejará el registro en pausa. Si ves **Reconecta tu cuenta**, tu sesión expiró: vuelve a iniciar sesión y lo que ya se registró se enviará.

### Permisos que pide

Quantro Time vive en la barra de menús y también tiene icono en el Dock: con cualquiera de los dos abres su ventana. Para registrar tu tiempo, macOS te pedirá permisos la primera vez; actívalos en **Configuración del Sistema → Privacidad y seguridad**:

- **Accesibilidad**: para medir tu nivel de actividad. Solo cuenta eventos de teclado y ratón; nunca registra lo que escribes ni dónde haces clic.
- **Grabación de pantalla**: macOS la exige para leer el nombre de la ventana activa. Quantro Time no graba ni envía capturas de pantalla.
- **Automatización** (Safari, Chrome…): para leer la dirección de la pestaña activa del navegador y registrar el tiempo por sitio web.

**Si actualizas desde una versión anterior**, quita Quantro Time de **Accesibilidad** y de **Grabación de pantalla** (botón **−**) y vuelve a darle permiso: los permisos anteriores pueden verse activados pero no funcionan con la versión nueva.

Si cambias un permiso, cierra Quantro Time (menú de la barra de menús → **Salir**, o **Salir de Quantro Time** en su ventana) y vuelve a abrirla.
