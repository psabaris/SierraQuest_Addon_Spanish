# Sierra Quest — Traducción al español

Addon no oficial que agrega el idioma **español** a [Sierra Quest](https://pointandclick.studio/games/sierra-quest), con instaladores para **Windows**, **macOS** y **Linux**.

## Descarga

Descargá el paquete de tu sistema desde la carpeta [`instaladores/`](instaladores):

| Sistema | Paquete |
|---|---|
| Windows | [SierraQuest_ES_Windows.zip](instaladores/SierraQuest_ES_Windows.zip) |
| macOS | [SierraQuest_ES_macOS.zip](instaladores/SierraQuest_ES_macOS.zip) |
| Linux | [SierraQuest_ES_Linux.tar.gz](instaladores/SierraQuest_ES_Linux.tar.gz) |

Cada paquete trae un `LEEME - LEER PRIMERO.txt` con estos mismos pasos.

## Windows

1. Descomprimí el `.zip` (clic derecho → *Extraer todo*). No lo ejecutes desde adentro del `.zip`.
2. Doble clic en `SierraQuest_Instalador_ES.exe`.
   Si aparece **«Windows protegió su PC»**: *Más información* → *Ejecutar de todas formas*.
3. El instalador busca el juego solo. Si no lo encuentra, elegí la carpeta donde está `Sierra Quest.exe`.
4. Si el juego está en *Archivos de programa*, Windows te pide permiso de administrador: aceptá.
5. Iniciá Sierra Quest: ya está en español.

## macOS

1. Descomprimí el `.zip` y hacé doble clic en `SierraQuest_Instalador_ES.app`.
2. macOS avisa que no puede verificar la app. Tocá *Aceptar*.
3. Andá a **Configuración del Sistema → Privacidad y seguridad**, bajá hasta el final y tocá **«Abrir igualmente»**. Confirmá con tu contraseña o Touch ID.
   En macOS 14 o anterior también sirve: clic derecho sobre la app → *Abrir*.
4. El instalador encuentra el juego → *Instalar*.
5. Si macOS dice que el instalador **no puede modificar apps**: *Privacidad y seguridad → Gestión de apps* → activá `SierraQuest_Instalador_ES` y volvé a abrirlo.
6. Abrí Sierra Quest: ya está en español.

**Si la app no abre**, usá la Terminal: escribí `bash `, arrastrá el archivo `instalar_es_mac.sh` a la ventana y presioná Enter.

> En macOS el instalador vuelve a firmar el juego en tu Mac. Es necesario porque agregar la traducción dentro de la app invalida la firma original, y sin esto macOS no abre el juego.

## Linux

```bash
tar xzf SierraQuest_ES_Linux.tar.gz
bash Linux/instalar_es_linux.sh
```

El script busca el juego solo. Si no lo encuentra, pedí la ruta, o pasala directamente:

```bash
bash Linux/instalar_es_linux.sh "/ruta/a/Sierra Quest"
```

También funciona con la versión de Windows bajo Wine o Proton: indicá la carpeta donde está `Sierra Quest.exe`.

## Instalación manual

Si preferís no usar el instalador, el archivo de traducción está en [`traduccion/es.tra`](traduccion/es.tra):

1. Copiá `es.tra` a la carpeta de datos del juego:
   - Windows: junto a `Sierra Quest.exe`.
   - Linux: donde está el archivo `.ags` (suele ser `data/`).
   - macOS: `Sierra Quest.app/Contents/Resources`. Después hay que volver a firmar el juego desde Terminal:
     `codesign --force --deep --sign - "/Applications/Sierra Quest.app"`
2. En la configuración del juego (`acsetup.cfg`), dejá la sección así:
   ```ini
   [language]
   translation=es
   ```

## Volver al inglés

Borrá `es.tra` de la carpeta del juego. En macOS, también podés correr en Terminal:
`bash instalar_es_mac.sh --uninstall "/Applications/Sierra Quest.app"`

Si actualizás el juego, volvé a ejecutar el instalador.

## Licencia

Publicado bajo la licencia [Apache 2.0](LICENSE).

Sierra Quest y todos sus contenidos pertenecen a sus autores. Esta es una traducción hecha por fans, sin relación oficial con el desarrollador. Para jugar necesitás tu propia copia del juego.
