# Holocure-Spanish
Traduccion del holocure usando https://github.com/PippleCultist/HoloCureLanguagePackMod

# Paquete de idiomas de Holocure Mod
## Traduccion directa del readme original
Un mod de Holocure que permite utilizar paquetes de idiomas dentro del juego. Esto también permite importar archivos .ttf para admitir cualquier idioma.

## Pasos de instalación
- Descarga `HoloCureLanguagePackMod.dll` y `CallbackManagerMod.dll` desde la última versión del mod https://github.com/PippleCultist/HoloCureLanguagePackMod/releases
- Descarga `AurieInstaller.exe`, `AurieLoader.exe` y `AurieCore.dll` desde la última versión de Aurie https://github.com/AurieFramework/Aurie/releases
 - Nota: Este lanzador puede ser marcado como un troyano por tu antivirus (Posiblemente porque estamos haciendo que un ejecutable cargue dll externos). YYToolkit es de código abierto y ha sido utilizado en varias comunidades de modificación sin problemas.
- Descarga `YYToolkit.dll` desde la última versión de YYToolkit https://github.com/AurieFramework/YYToolkit/releases
- Lanza `AurieInstaller.exe`, haz clic en `Instalar AurieFramework` y selecciona `HoloCure.exe`
 - Puedes encontrar `HoloCure.exe` a través de Steam haciendo clic en `Explorar archivos locales`
- Copia `CallbackManagerMod.dll`, `HoloCureLanguagePackMod.dll` y `YYToolkit.dll` a `mods/Aurie`
- Copia `AurieCore.dll` a `mods/Native`
- Copia `AurieLoader.exe` a `mods`
- Ejecutar el juego utilizando el ejecutable o a través de Steam debería lanzar los mods también

## Agregar un paquete de idiomas
Después de lanzar el juego con el mod instalado, debería crear una carpeta llamada `LanguagePacks` en la misma carpeta que `HoloCure.exe`. Coloca el paquete de idiomas y el archivo ttf correspondiente en esa carpeta.

## Crear un paquete de idiomas
Crea un archivo en el formato `nombreArchivo.lang`. Lo que pongas como `nombreArchivo` aparecerá como el nombre del idioma en el juego. La primera línea del archivo debe ser `NONE` o el nombre del archivo ttf que utilizarás. (Puedes ver el Spanish.lang como ejemplo)
Cada línea después de eso asignará el texto que deseas en el juego. El texto que pongas debe ser un arreglo de cadenas o una cadena, y debe coincidir con el tipo de lo que originalmente estaba allí para no hacer que el juego se bloquee.

Por ejemplo, para reemplazar el texto de los botones del título, lo tendrías en el formato `titleButtons ["Jugar", "Holo House", "Tienda", "Clasificación", "Logros", "Configuración", "Créditos", "Salir"]`, y reemplazar el texto de Half Angel estará en el formato `HalfAngelName "Media Ángel"`.
Cada mapeo diferente debe estar en su propia línea en el formato mencionado anteriormente. `TextContainer.out` se creará cada vez que el juego se ejecute con el mod instalado, que puedes utilizar para crear tu propio paquete de idiomas.

Algunos textos pueden no estar en el contenedor de texto debido a que están codificados en el juego. En esos casos, puedes utilizar la función de mapeo directo que estará en el formato `"HP" "testHP"`. Debe ser exactamente igual al texto que deseas reemplazar, lo que incluye la capitalización.
