# Pipeline de Reclutamiento Automatizado (n8n + JEV + Airtable)

Este repositorio contiene el flujo de trabajo de n8n para la extracción, clasificación con IA y registro automático de candidatos desde Gmail hacia Airtable.

## 🚀 Arquitectura del Flujo
1. **Gmail Trigger**: Captura correos entrantes con hojas de vida (.docx / .pdf).
2. **Extracción**: Extrae y descomprime el texto del documento.
3. **JEV (TypeSafe AI)**: Clasifica al candidato por Área (Dev, Support, DB, Infra), Nivel Académico y Años de Experiencia.
4. **Switch & Airtable**: Ruta e inserta al candidato en la base de datos correspondiente.

## 🔐 Credenciales Requeridas en n8n
Para hacer funcionar este workflow al importarlo, debes configurar las siguientes credenciales en tu instancia de n8n:
- **Gmail OAuth2 API**: Para lectura de la bandeja de entrada.
- **Airtable Personal Access Token**: Para la inserción de registros.
- **Header Auth / Bearer Token**: Para consumir la API de JEV.