# Runbook

## Validación Linux
```bash
./scripts/linux/monitor.sh
tail -n 20 logs/monitor.log
```

## Validación Windows
```powershell
.\scripts\windows\monitor.ps1
Get-Content .\logs\monitor.log -Tail 20
```

## Cómo forzar una alerta
Baja el umbral de CPU a 1 y vuelve a ejecutar el script.
