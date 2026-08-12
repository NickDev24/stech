# 💼 MODELO DE NEGOCIO — STECH

## Propuesta de valor

STECH es una plataforma de **movilidad urbana con gobernanza municipal incorporada**. A diferencia de Uber, DiDi o Cabify —que operan como plataformas cerradas sin visibilidad para la Municipalidad— STECH entrega al gobierno local las herramientas para **regular, fiscalizar y planificar** la movilidad de la ciudad.

## Fuentes de ingreso

| Fuente | Detalle |
|---|---|
| **Comisión por viaje** | Porcentaje del precio base de cada viaje completado |
| **Tarifa mínima** | Valor mínimo por viaje que garantiza rentabilidad en trayectos cortos |
| **Penalizaciones** | Multas por cancelación (30%) y no-show (50%) de pasajeros |
| **Suscripción semanal** | Prepago con descuento (25% + 50% anticipado) — flujo de caja recurrente |
| **Licencia municipal** | Modelo B2G: fijo mensual + royalty para el municipio |
| **Cesión de derechos** | Operación comercial por territorio y plazo, con piso anual garantizado |
| **Venta total** | Transferencia completa de código, marca, dominios y cuentas |

## Estructura de comisión

```
Precio base  = distancia × precio/km   (piso: tarifa mínima)
Comisión     = 10% del precio base
Reparto 65/35:
  → Pasajero paga      = base + 6,5%
  → Conductor recibe   = base − 3,5%
  → Plataforma gana    = 10% del base
```

## Tarifas por franja horaria

| Franja | Realtime | Compartido | Semanal | Mínima |
|---|---|---|---|---|
| Día laboral | $780/km | $640/km | $950/km | $2.500 |
| Noche laboral | $850/km | $740/km | $1.200/km | $2.500 |
| Día fin de semana | $850/km | $690/km | $1.050/km | $2.500 |
| Noche fin de semana | $950/km | $770/km | $1.350/km | $2.500 |

*(Valores ARS. Editables en tiempo real desde el panel admin, sin deploy.)*

## Canales de pago

- **Efectivo** (directo al conductor)
- **Billetera interna** (prepago — canal más rentable)
- **Tarjeta** (MercadoPago / MobbeX)
- **QR**

## Modelo B2G (Gobernanza Municipal)

STECH incluye módulos regulatorios únicos:
- Habilitaciones vehiculares con **QR oficial** escaneable por la policía
- **Panel de tránsito** (AMT): cortes de calle, zonas de peligro, feriados
- **Panel policial**: verificación en calle, sin acceso a datos privados
- **Panel municipal**: KPIs en tiempo real, series de tiempo AR, emergencias
- **Reportes regulatorios** exportables

### Opciones de contratación municipal
| Opción | Esquema |
|---|---|
| **A — Licencia** | Fijo US$500/mes, datos 100% del municipio |
| **B — Adquisición** | US$50.000–75.000, transferencia total |
| **C — Piloto** | 3 meses gratis, solo costos de infra (~US$200/mes) |

## Economía de la plataforma

- **Infraestructura actual**: ~US$414/mes (servidor sobredimensionado; redimensionando → ~US$61/mes)
- **Punto de equilibrio**: ~110–130 viajes/día con la tarifa actual, o ~50 viajes/día redimensionando el servidor
- **Estrategia de rentabilidad**: incentivar billetera, efectivo y QR (fees bajos); desincentivar crédito directo (fee ~7,85% consume la comisión)

---

*Documento público con fines de divulgación. Los detalles técnicos operativos residen en el repositorio privado `stech-core`.*
