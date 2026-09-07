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

---

> ⚠️ Este método puede dejar de funcionar en futuras builds de Windows 11
> si Microsoft decide parchearlo. Si deja de funcionar, la alternativa
> más fiable es [Rufus](https://rufus.ie) con la opción
> "Remove requirement for 4GB+ RAM, Secure Boot, and TPM 2.0". 

---

### ⚠️ Disclaimer

Este contenido es **solo orientativo** y se proporciona "tal cual", sin garantía de
ningún tipo. El uso de estas instrucciones, scripts o configuraciones es
**bajo tu propia responsabilidad**.

No me hago responsable de:

- Daños al sistema, pérdida de datos o cualquier otro problema derivado de
  seguir estas indicaciones.
- El uso que se les dé a estas configuraciones en equipos que no son los
  descritos aquí.
- Problemas de compatibilidad con hardware o software distinto al probado.

Si algo se rompe, es tuyo. 😄   
