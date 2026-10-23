# ElectroStock — Canal de Distribución Oficial de Actualizaciones

Este repositorio público es utilizado exclusivamente para la distribución estática de instaladores y manifiestos de actualización firmados para el software **ElectroStock**.

## Estructura de Actualización

- `version.json`: Manifiesto firmado con metadatos de la última versión pública disponible (número de versión, tamaño en bytes, hash SHA-256 del instalador y notas de versión).
- `version.json.sig`: Firma criptográfica digital desprendida en formato **ECDSA P-256 (IEEE P1363)** correspondiente al contenido binario exacto de `version.json`.
- **Releases**: Cada versión publicada se distribuye a través de GitHub Releases con su instalador de Windows (`ElectroStock_Setup_vX.X.X.exe`).

> **Seguridad e Integridad**: Las aplicaciones clientes de ElectroStock verifican la firma criptográfica del manifiesto antes de confiar en cualquier dato y revalidan el hash SHA-256 del instalador inmediatamente antes de iniciar cualquier actualización en el equipo del usuario.
