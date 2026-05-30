# MovilPeak: Contexto de la Empresa

**Industria**: Ride-Hailing (transporte privado urbano)

## Quiénes somos
MovilPeak conecta pasajeros con conductores particulares mediante una aplicación móvil en Lima.

**Métricas operativas**:
* Comisiones de conductores: entre 23% y 25% en febrero, y de 25% a 27% en los demás meses.
* Tarifa base promedio: S/ 1.50 por kilómetro, ajustada por un factor de precio variable y multiplicada por el factor de surge.
* Zonas de operación: 12 distritos de Lima Metropolitana.

## El problema
El crecimiento de los ingresos se ha desacelerado. El volumen de viajes aumenta, pero la tarifa final tiene una alta variabilidad por factores climáticos y decisiones de precios aleatorias sin una estructura optimizada por hora o zona. Se requiere diseñar una estrategia de precios para mejorar los ingresos sin perder participación de mercado.

## Archivos de datos disponibles
Todos los archivos corresponden al primer trimestre de 2024 (Q1 2024).

| Archivo | Descripción y Columnas |
| :--- | :--- |
| `trips_2024.csv` | Registro detallado de viajes realizados.<br>Columnas: `trip_id`, `fecha`, `hora`, `zona_origen`, `zona_destino`, `distancia_km`, `duracion_min`, `tarifa_soles`, `surge_multiplier`, `demanda_estimada_hora`, `choferes_disponibles`, `segmento_cliente` |
| `weather.csv` | Datos meteorológicos diarios por zona.<br>Columnas: `date`, `zone`, `temp_c`, `condition`, `rain_mm`, `humidity_pct` |
| `driver_payouts.csv` | Detalle de pagos e ingresos de conductores por viaje.<br>Columnas: `driver_id`, `trip_id`, `date`, `zone`, `distance_km`, `fare_collected`, `commission_pct`, `driver_payout`, `bonus_surge`, `platform_fee` |
| `competitor_scrape.csv` | Tarifas y tiempos de espera de la competencia.<br>Columnas: `date`, `competitor`, `price_per_km`, `wait_time_min`, `source` |
| `marketing_spend.csv` | Inversión mensual en adquisición de usuarios.<br>Columnas: `month`, `channel`, `spend_soles`, `new_users`, `cac_soles` |

## Preguntas para el análisis
1. ¿Cuál es la elasticidad precio de la demanda según la hora del día y la zona de origen?
2. ¿Cómo afecta la lluvia a la demanda y a la disposición a pagar de los usuarios?
3. ¿Es óptimo el multiplicador de surge aplicado durante las horas pico?
4. ¿Qué canales de marketing digital muestran el menor costo de adquisición de clientes (CAC) y cómo se correlacionan con los viajes generados?
5. ¿Cómo se comparan nuestras tarifas frente a las de la competencia?