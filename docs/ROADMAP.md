# 🗺️ HOJA DE RUTA — STECH

> Estado real del proyecto y próximos pasos. Última actualización: agosto 2026.

## ✅ Completado

- [x] Backend completo (269 endpoints, 49 modelos de datos)
- [x] Algoritmo de viajes compartidos
- [x] Tarifas dinámicas por franja horaria (editables sin deploy)
- [x] Web pasajeros, web conductores y panel admin
- [x] Apps nativas Android (v10.7) publicadas en Google Play
- [x] Módulo municipal completo (habilitaciones QR, tránsito, policía, municipal)
- [x] Seguridad: Redis con contraseña, CORS restringido, webhooks con firma HMAC
- [x] 280 tests automatizados
- [x] Monitoreo externo (UptimeRobot)
- [x] Documentación pública y privada

## 🟡 En curso / pendiente

- [ ] Credenciales de pago en PRODUCCIÓN (MercadoPago `APP_USR-...`)
- [ ] Redimensionar servidor para bajar costos (ahorro potencial ~US$180/mes)
- [ ] Backup offline de keystores de firma Android
- [ ] Liberar espacio en disco del servidor

## 🔜 Próximos hitos

1. **Lanzamiento comercial** en Salta: reclutar 5–10 remiseros, 100 viajes reales
2. **Alianza municipal** (piloto 3 meses): licencia, red de conductores, difusión
3. **Escala**: de 50 a 2.000 viajes/día
4. **Expansión** a otras ciudades (el sistema es multi-ciudad por diseño)

---

*Hoja de ruta pública. El detalle técnico de cada hito vive en `stech-core`.*
