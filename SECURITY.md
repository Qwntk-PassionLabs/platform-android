# 🔐 Política de Seguridad

La seguridad de este proyecto es una prioridad. A continuación se describen las prácticas y lineamientos para reportar y manejar vulnerabilidades.

---

## 📢 Reportar una vulnerabilidad

- **No abras un issue público** para reportar vulnerabilidades.
- Envía un correo a: **security@tu-org.com** (o el canal privado definido por tu organización).
- Incluye:
  - Descripción clara de la vulnerabilidad
  - Pasos para reproducirla
  - Impacto potencial
  - Logs o capturas relevantes

---

## 🔒 Prácticas de seguridad en el repo

- **Protección de secretos**:
  - Push Protection y Secret Scanning están habilitados.
  - Nunca subas claves de API, archivos `google-services.json` ni credenciales.
  - Usa GitHub Secrets o un gestor seguro (Vault, Secret Manager).

- **CI/CD seguro**:
  - Workflows usan credenciales efímeras (OIDC).
  - Solo Actions verificadas y fijadas a commit SHA están permitidas.
  - Environments con aprobaciones para despliegues a producción.

- **Dependencias**:
  - Dependabot alerta y actualiza librerías vulnerables.
  - Dependency Review bloquea PRs con dependencias críticas.

---

## 🛡️ Respuesta a incidentes

1. Revocar credenciales comprometidas inmediatamente.
2. Rotar claves en proveedores (Firebase, Play Store, etc.).
3. Crear un issue privado para seguimiento interno.
4. Documentar la resolución y cerrar la alerta en GitHub.

---

## 📊 Métricas de seguridad

- MTTR (tiempo de respuesta a vulnerabilidades)
- Número de secretos bloqueados por Push Protection
- Vulnerabilidades abiertas vs. resueltas
