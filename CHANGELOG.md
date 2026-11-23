# Changelog

All notable changes to this project are documented in this file.

## [3.1.0] - 2025

### Added
- Support for ESP8266 Arduino core 3.x.
  `WiFiClientSecure::verify()` was removed in core 3.x (replaced by
  `setFingerprint()`). The bundled WebSockets client now applies the TLS
  fingerprint via `setFingerprint()` before connecting on core >= 3, and keeps
  the legacy `verify()` path for core < 3. This fixes compilation on current
  ESP8266 cores.

### Changed
- Fork metadata (`library.properties`, `library.json`, README badges) updated
  to point at this fork.
- Removed a duplicate `RemoteDebug_Debugger` example file.