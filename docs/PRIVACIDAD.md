# 🔐 POLÍTICA DE PRIVACIDAD — STECH

*Última actualización: agosto 2026*

## 1. Datos que se recopilan

- **Datos de cuenta**: nombre, teléfono, email (según el rol: pasajero, conductor, admin)
- **Datos de viaje**: origen, destino, ruta, hora, monto
- **Datos del conductor/vehículo**: licencia, habilitación, VTV, seguro
- **Ubicación**: necesaria para conectar pasajeros con conductores

## 2. Uso de los datos

- Conectar pasajeros con conductores y procesar viajes
- Calcular tarifas y procesar pagos
- Verificar habilitaciones vehiculares (requisito regulatorio)
- Enviar notificaciones de estado del viaje
- Mejorar la seguridad y prevenir fraude

## 3. Lo que NO hacemos

- ❌ No vendemos datos personales
- ❌ No compartimos datos de pasajeros con terceros (salvo requisito legal)
- ❌ No usamos datos para publicidad de terceros

## 4. Seguridad

- Contraseñas cifradas (bcrypt)
- Tokens JWT con expiración y refresh
- Rate-limiting contra ataques de fuerza bruta
- Webhooks de pago verificados con firma criptográfica
- Acceso a datos de pasajeros restringido por roles (la policía solo ve habilitaciones)

## 5. Retención

Los datos se conservan mientras la cuenta esté activa. El usuario puede solicitar la eliminación de su cuenta y datos.

## 6. Contacto

Para consultas sobre privacidad, ver [CONTACTO.md](CONTACTO.md).

---

*Esta política aplica a la plataforma STECH operada por su propietario. Puede actualizarse periódicamente.*
