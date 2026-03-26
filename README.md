# AI IT Automation Starter

Proyecto de portafolio orientado a **System Administration, Infrastructure, Cloud Operations, Technical Support y DevOps inicial**.

Este repositorio demuestra la capacidad de diseñar una automatización básica, útil y explicable para monitoreo de infraestructura en **Linux y Windows**, con enfoque en operación, troubleshooting y documentación técnica.

---

## Professional Summary

Este proyecto fue creado para mostrar competencias prácticas en:

- Automatización operativa
- Troubleshooting de sistemas
- Monitoreo básico de infraestructura
- Scripting en Bash y PowerShell
- Documentación técnica y runbooks
- Pensamiento orientado a soporte, continuidad y mejora operativa

En un contexto real, este tipo de solución puede utilizarse como base para:

- chequeos preventivos de salud del sistema,
- alertas iniciales para soporte,
- validaciones previas a escalamiento,
- evidencia técnica en entornos de operación.

---

## Business Value

La solución ayuda a reducir tareas manuales repetitivas al automatizar validaciones de:

- uso de CPU,
- uso de memoria,
- consumo de disco,
- estado de servicios críticos,
- registro de alertas en logs reutilizables.

Esto facilita una respuesta más rápida ante incidentes y mejora la estandarización operativa.

---

## Technical Scope

### Linux
- Bash scripting
- CPU check
- Memory check
- Root disk usage check
- Service status validation with `systemctl`
- Logging
- Scheduling with cron

### Windows
- PowerShell scripting
- CPU check using CIM/WMI
- Memory usage validation
- Disk usage validation on `C:`
- Critical service status validation
- Logging
- Optional scheduling with Task Scheduler

---

## Repository Structure

```text
ai-it-automation-starter/
├── README.md
├── LICENSE
├── .gitignore
├── config/
│   └── thresholds.conf.example
├── docs/
│   ├── runbook.md
│   └── labs/
│       └── week1-labs.md
├── examples/
│   └── sample-alert.log
├── prompts/
│   └── chatgpt-prompts.md
├── scripts/
│   ├── linux/
│   │   ├── install.sh
│   │   └── monitor.sh
│   └── windows/
│       ├── install.ps1
│       └── monitor.ps1
└── .github/
    └── workflows/
        └── shellcheck.yml
```

---

## Use Case

Este proyecto está pensado como laboratorio y también como evidencia de portafolio para roles como:

- Systems Administrator
- Infrastructure Support Engineer
- NOC / Operations Analyst
- Cloud Support Associate
- DevOps / SRE Junior
- Technical Support Engineer

---

## Key Features

- Monitoreo básico multiplataforma
- Umbrales configurables
- Logging de eventos INFO/WARN
- Revisión de servicios críticos
- Instalación inicial sencilla
- Documentación operativa incluida
- Base clara para futuras integraciones con correo, webhooks o dashboards

---

## Quick Start

### Linux

1. Crear archivo de configuración:
```bash
cp config/thresholds.conf.example config/thresholds.conf
```

2. Dar permisos:
```bash
chmod +x scripts/linux/install.sh scripts/linux/monitor.sh
```

3. Ejecutar instalación:
```bash
./scripts/linux/install.sh
```

4. Probar ejecución manual:
```bash
./scripts/linux/monitor.sh
```

5. Revisar evidencia:
```bash
tail -n 20 logs/monitor.log
```

---

### Windows

1. Abrir PowerShell.
2. Ejecutar instalación:
```powershell
.\scripts\windows\install.ps1
```

3. Ejecutar monitoreo manual:
```powershell
.\scripts\windows\monitor.ps1
```

4. Revisar evidencia:
```powershell
Get-Content .\logs\monitor.log -Tail 20
```

---

## Validation Example

Ejemplo de salida esperada en logs:

```text
[2026-03-26 10:00:00] INFO CPU=12.5 MEM=48 DISK=61 SERVICE=active
[2026-03-26 10:05:00] WARN CPU=85.2 threshold=80
```

Esto confirma que el script:

- recoge métricas,
- registra información útil,
- compara umbrales,
- genera alertas cuando corresponde.

---

## Hands-On Lab

Se incluye una guía práctica en:

- `docs/labs/week1-labs.md`

Ese laboratorio permite:

- instalar el proyecto,
- ejecutarlo paso a paso,
- forzar alertas,
- validar resultados,
- generar evidencia para entrevistas o GitHub.

---

## Runbook

Se incluye documentación operativa en:

- `docs/runbook.md`

El runbook cubre:

- validación manual,
- revisión de logs,
- errores comunes,
- cómo forzar alertas,
- mejoras sugeridas.

---

## Example Interview Pitch

> I built a cross-platform starter automation project for Linux and Windows focused on infrastructure health checks.  
> It validates CPU, memory, disk usage, and service status, then logs actionable information for support operations.  
> The project demonstrates scripting, troubleshooting, automation thinking, and operational documentation through runbooks and labs.  
> It is also designed to be extended with email alerts, webhooks, dashboards, or cloud integrations.

---

## Suggested Next Improvements

- Email alerts
- Webhook alerts
- JSON export
- Auto-remediation for failed services
- Integration with Teams, Slack, or Telegram
- Containerized version
- Grafana dashboard
- Azure / AWS integration

---

## Why This Project Matters

Para reclutadores y hiring managers, este repositorio demuestra que el candidato puede:

- convertir tareas manuales en automatizaciones simples,
- trabajar con Linux y Windows,
- documentar procedimientos técnicos,
- validar resultados,
- construir una base reutilizable para operación y soporte.

---

## GitHub Upload

```bash
git init
git add .
git commit -m "Initial commit: AI IT Automation Starter"
git branch -M main
git remote add origin https://github.com/TU-USUARIO/ai-it-automation-starter.git
git push -u origin main
```

---

## License

MIT
