# Eigene Fassung (belzadur)

Zweig `belzadur` = wez/govee2mqtt Version 2026.03.25-ab9deb66 plus nur
[wez/govee2mqtt#720](https://github.com/wez/govee2mqtt/pull/720) (Nathan Guenther):
die Bruecke meldet ihre Verfuegbarkeit jede Minute erneut "online". Ohne das bleiben nach
einem HA-Neustart alle Govee-Entitaeten `unavailable`, wenn das einmalige "online" ankommt,
bevor HA das Thema wieder abonniert hat (wez/govee2mqtt #110, #227, #572).

Zweig `main` bleibt der unveraenderte Stand von wez.

App-Quelle in HA: `https://github.com/belzadur/govee2mqtt#belzadur`.
Abbild: `ghcr.io/belzadur/govee2mqtt-addon:<version>`, gebaut von
`.github/workflows/belzadur-addon.yml`. Neue Version = `version` in `addon/config.yaml` erhoehen.
