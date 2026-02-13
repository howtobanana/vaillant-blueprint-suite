# Kompatibilität der Suite

## Architektur
- `vaillant_heizungs-steuerung.yaml` ist das zentrale Backbone.
- `vaillant_geofencing.yaml` steuert den Away-Status (Helper-basiert).
- `vaillant_lüftungs-steuerung.yaml` ist unabhängig von der Kern-Heizlogik.
- `vaillant_system-diagnose.yaml` überwacht und benachrichtigt, greift nicht direkt in die Kernsteuerung ein.

## Integrationsprinzip
- Gemeinsame Helper/Entities zwischen Modulen müssen konsistent konfiguriert werden.
- Geofencing und Core sollen denselben Away-Helper verwenden.

## Versionsmanagement
- Modulversionen über Git-Tags dokumentieren.
- Keine Versionssuffixe in Dateinamen verwenden.
