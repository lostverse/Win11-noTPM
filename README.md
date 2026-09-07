# Win11-noTPM

## 🪟 Instalar Windows 11 sin TPM / CPU compatible

Para equipos que no cumplen los requisitos mínimos de Windows 11
(sin TPM 2.0, CPU no soportada, etc.) pero que funcionan perfectamente.

### Método: flag `/product server`

1. Extrae o monta la ISO de Windows 11.
2. Abre CMD o PowerShell **como administrador**.
3. Navega a la carpeta `sources/` de la ISO.
4. Ejecuta:

   ```cmd
   setup.exe /product server   

## ¿Qué implica?
No instala Windows Server. Instala Windows 11 normal (desktop),
pero usando el perfil de instalación "server" que no verifica
TPM, Secure Boot ni generación de CPU.
El sistema resultante es un Windows 11 estándar, con todas las
funcionalidades de escritorio.
No se modifica el registro ni se editan archivos del ISO.
Funciona en builds recientes (24H2, 25H2).

# ⚠️ Aviso
Se debe usar una clave de producto original y legítima (retail u OEM).
Este método no es una forma de activar Windows sin licencia, simplemente
evita la verificación de hardware durante la instalación.
