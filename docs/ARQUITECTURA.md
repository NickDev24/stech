# 🏗️ ARQUITECTURA — Visión General

> Documento público de alto nivel. Detalles técnicos y configuración en el repositorio privado `stech-core`.

## Stack tecnológico

```
┌─────────────────────────────────────────────────────────┐
│                     APPS NATIVAS (Android)               │
│   Pasajeros (Kotlin/Compose)   Conductores (Kotlin)     │
│            Google Play — prueba cerrada v10.7            │
└──────────────────────────┬──────────────────────────────┘
                           │ HTTPS
┌──────────────────────────▼──────────────────────────────┐
│                     FRONTENDS WEB (Next.js 16)           │
│   Pasajeros PWA (PWA)   Conductores PWA   Panel Admin    │
└──────────────────────────┬──────────────────────────────┘
                           │
┌──────────────────────────▼──────────────────────────────┐
│                   BACKEND (Next.js API)                  │
│   269 endpoints · 22.000+ líneas de esquema Prisma       │
│   Auth JWT · Rate-limiting · Matching · Tarifas · Pagos  │
└───────┬──────────────────────┬──────────────────┬────────┘
        │                      │                  │
┌───────▼───────┐   ┌──────────▼───────┐  ┌───────▼────────┐
│  PostgreSQL    │   │  Redis (SSE +    │  │  OSRM local    │
│  (Supabase)    │   │  cache)          │  │  (ruteo Salta) │
│  49 modelos    │   │                  │  │  sin costo     │
└───────────────┘   └──────────────────┘  └────────────────┘
```

## Componentes

| Capa | Tecnología | Rol |
|---|---|---|
| **Backend** | Next.js 16 (standalone) | API REST + panel admin |
| **Web pasajeros** | Next.js 16 PWA | Solicitar viajes, pagar, calificar |
| **Web conductores** | Next.js 16 PWA | Aceptar viajes, navegación, cobrar |
| **Apps nativas** | Kotlin + Jetpack Compose | Versión nativa de pasajeros y conductores |
| **Base de datos** | PostgreSQL (Supabase) | 49 modelos Prisma |
| **Cache/SSE** | Redis | Cache + pub/sub streaming en vivo |
| **Ruteo** | OSRM self-hosted | Cálculo de rutas y tiempos (datos de Salta) |
| **Pagos** | MercadoPago + MobbeX | Checkout, webhooks, billetera |
| **Push** | Firebase FCM | Notificaciones push |
| **Email** | Resend | Emails transaccionales |
| **Geocoding** | Geoapify + Georef | Búsqueda de direcciones |
| **IA** | Groq + Cohere | Asistencia y marketing (Zernio) |
| **Infra** | AWS EC2 + Docker + Cloudflare Tunnel | Despliegue y exposición HTTPS |

## Funcionalidades principales

- **Viajes**: en tiempo real, compartidos (algoritmo de compatibilidad, Ruta Madre) y semanales (suscripción)
- **Tarifas**: dinámicas por franja horaria (día/noche × semana/fin de semana), editables sin deploy
- **Pagos**: tarjeta, QR, billetera interna, efectivo; webhooks verificados con firma HMAC
- **Matching**: asignación automática de conductores por proximidad y disponibilidad
- **Tracking en vivo**: streaming SSE de posición en tiempo real
- **Regulatorio**: habilitaciones vehiculares con QR, panel de tránsito, panel policial, panel municipal
- **Seguridad**: JWT + refresh, bcrypt, rate-limiting, verificación facial local (LBPH/OpenCV)
- **Operación**: command center con KPIs, scoring de conductores, penalizaciones, emergencias

---

*Detalle técnico completo en el repositorio privado `stech-core`.*
