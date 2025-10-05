# Intune – Endpoint Security Baselines (as Code)

Baseline JSONs + import/validation scripts for Defender AV/EDR, BitLocker, ASR, Firewall.

## Structure
```
baselines/
  windows11-security-baseline.json
scripts/
  Import-Baseline.ps1
  Validate-Assignments.ps1
reports/
  sample-report.csv
```

## Import
```pwsh
Install-Module Microsoft.Graph.Beta -Scope CurrentUser -Force
Connect-MgGraph -Scopes "DeviceManagementConfiguration.ReadWrite.All"
./scripts/Import-Baseline.ps1 -Path ./baselines/windows11-security-baseline.json -AssignTo "All Devices"
```
