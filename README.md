# Yggdrasil Platform — Legal Repository (Legal as Code)

Repositorio centralizado de términos de servicio, acuerdos de confidencialidad (NDA), políticas de privacidad y autorizaciones de tratamiento de datos personales para las plataformas y servicios del ecosistema **Yggdrasil Platform** (*Bifrost QA Gate*, *Utgard QA Simulator*, *Midgard QA Entities*, *Valgrind Gateway*, *Glitnir Identity*).

## 🏛️ Marco Jurídico Aplicable

- **Colombia:**
  - **Ley 23 de 1982 y Ley 44 de 1993:** Régimen de Derechos de Autor sobre Software (asimilado a obra literaria).
  - **Decisión Andina 351 de 1993:** Régimen Común sobre Derecho de Autor y Derechos Conexos.
  - **Decisión Andina 486 de 2000 (Arts. 260 a 266):** Protección del Secreto Empresarial e Industrial.
  - **Ley 256 de 1996:** Régimen de Competencia Desleal (Art. 16: Violación de Secretos).
  - **Ley 527 de 1999 y Decreto 2364 de 2012:** Validez jurídica y probatoria de Mensajes de Datos y Firmas Electrónicas.
  - **Ley Estatutaria 1581 de 2012 y Decreto 1377 de 2013:** Régimen General de Protección de Datos Personales (Habeas Data).
  - **Código Penal Colombiano (Ley 599 de 2000):** Arts. 269A-J (Delitos Informáticos) y Art. 308 (Violación de reserva industrial o comercial).
- **Internacional:**
  - **Convenio de Berna:** Protección transfronteriza automática de obras de software.
  - **ADPIC / TRIPS (OMC):** Art. 10 (Software como obra literaria) y Art. 39 (Información no divulgada / Trade Secrets).
  - **Tratados WIPO/OMPI:** WCT (Tratado sobre Derecho de Autor).

## 📂 Estructura del Repositorio

```
yggdrasil-legal/
├── README.md                           # Documentación y lineamientos del repositorio
├── registry.json                       # Manifiesto activo de versiones y hashes SHA-256
├── terms/
│   └── evaluation-terms-v1.0.0.md      # Términos y Condiciones de Evaluación (Sandbox PoC)
├── nda/
│   └── individual-evaluator-nda-v1.0.0.md # Acuerdo Individual de Confidencialidad y Secretos
└── privacy/
    └── habeas-data-v1.0.0.md           # Autorización Tratamiento de Datos (Ley 1581)
```

## 🔐 Integridad y Verificación Criptográfica

Cada versión de documento publicada en este repositorio cuenta con un hash criptográfico **SHA-256** registrado en [`registry.json`](registry.json).

Cuando un usuario o funcionario valida su identidad mediante OTP y acepta las condiciones en la plataforma (*Glitnir Identity* / *Bifrost QA Gate*), el sistema almacena de forma inmutable en el Audit Log de base de datos:
1. El identificador del usuario (`email corporativo`).
2. El commit hash y tag de Git vigente (`v1.0.0`).
3. El hash SHA-256 de cada documento aceptado.
4. Timestamp UTC, IP y huella del agente de usuario.

Esto garantiza el cumplimiento estricto de **equivalencia funcional, no repudio e integridad probatoria** bajo la Ley 527 de 1999 de Colombia y estándares internacionales de contratación electrónica.
