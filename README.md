# AI IT Automation Starter

Repositorio listo para GitHub con un proyecto práctico orientado a sysadmins, soporte, infraestructura y cloud.

## Objetivo
Automatizar validaciones básicas de salud del sistema:
- CPU
- Memoria
- Disco
- Estado de servicio crítico
- Logs y alertas
- Tareas programadas
- Documentación y prompts reutilizables

## Inicio rápido Linux
```bash
cp config/thresholds.conf.example config/thresholds.conf
chmod +x scripts/linux/install.sh scripts/linux/monitor.sh
./scripts/linux/install.sh
./scripts/linux/monitor.sh
tail -n 20 logs/monitor.log
```

## Inicio rápido Windows
```powershell
Copy-Item .\config\thresholds.conf.example .\config\thresholds.ps1
.\scripts\windows\install.ps1
.\scripts\windows\monitor.ps1
Get-Content .\logs\monitor.log -Tail 20
```

## Subir a GitHub
```bash
git init
git add .
git commit -m "Initial commit: AI IT Automation Starter"
git branch -M main
git remote add origin https://github.com/TU-USUARIO/ai-it-automation-starter.git
git push -u origin main
```
