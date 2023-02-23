# ovos-PHAL-plugin - alsa volume control

## Install

```sh
python -m pip install git+https://${GITHUB_USER}:${GITHUB_TOKEN}@github.com/OpenVoiceOS/ovos-PHAL-plugin-alsa
```

## Configure

In your mycroft.conf

```json
"PHAL": {
    "ovos-PHAL-plugin-alsa": {"enabled": true}
}
```

## Companion skill
[skill-ovos-volume](https://github.com/OpenVoiceOS/skill-ovos-volume)

## controls system volume with alsa

```python
self.bus.on("mycroft.volume.get", self.handle_volume_request)
self.bus.on("mycroft.volume.set", self.handle_volume_change)
self.bus.on("mycroft.volume.mute", self.handle_mute_request)
self.bus.on("mycroft.volume.unmute", self.handle_unmute_request)
```
