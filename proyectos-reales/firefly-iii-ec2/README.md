# 💰 Firefly III en AWS EC2 — Proyecto Real

Despliegue de un gestor de finanzas personales (Firefly III) en una instancia EC2 real de AWS, expuesto de forma segura a través de mi dominio propio usando Cloudflare Tunnel.

## 🎯 Objetivo

Migrar un servicio que ya operaba en mi homelab (NUC local) hacia infraestructura en la nube real, aplicando los conceptos aprendidos en AWS Cloud Practitioner Essentials.

## 🏗️ Arquitectura

## 🛠️ Stack utilizado

- **Amazon EC2** — instancia con imagen Debian 13
- **Docker** — motor de contenedores
- **Firefly III** — gestor de finanzas personales, en contenedor
- **MariaDB** — base de datos del servicio, en contenedor
- **Cloudflare Tunnel** — exposición segura del servicio sin abrir puertos públicos en el firewall de AWS
- **Dominio propio** — noelmarkets.com

## 💵 Gestión de costos (AWS Free Tier)

- Cuenta creada bajo el programa de créditos AWS Free Tier ($100 USD, vigencia 12 meses)
- Monitoreo activo del consumo vía AWS Billing Console
- Estrategia: detener (stop) la instancia EC2 cuando no está en uso activo, para minimizar el consumo de crédito, dado que el servicio se usa de forma poco frecuente

## 📚 Qué aprendí

- Diferencia entre detener y terminar una instancia EC2, y su impacto en el costo
- Cómo el almacenamiento EBS genera costo incluso con la instancia detenida
- Exponer un servicio en la nube sin abrir puertos directamente, usando un túnel en vez de una IP pública expuesta
- Cómo migrar un servicio ya funcional desde un entorno self-hosted (NUC local) hacia infraestructura cloud real
