# Ukrainian Voice Packs for Dreame Vacuums

Ukrainian voice prompts for compatible Dreame robot vacuums. The pack covers cleaning, charging, errors, and other status announcements. The voice was generated with AI and edited in Audacity.

## Listen and download

| Voice pack | Voice | Audio samples |
| --- | --- | --- |
| [`uk_female_pensive`](https://raw.githubusercontent.com/oleksandr-belei/dreame-vacuum-uk-voice-packs/main/voice_packs/uk_female_pensive) | Soft female voice | [Sample MP3s](voice_samples/uk_female_pensive/) |

## Install with Home Assistant

Your vacuum must support custom voice packs and be set up with the [Dreame Vacuum integration](https://github.com/Tasshack/dreame-vacuum). The pack has no verified compatibility list. Support can vary by vacuum model and firmware.

1. Open **Settings → Tools → Actions**. Older Home Assistant versions label this area **Developer Tools**.
2. Switch to **YAML mode** and paste the example below.
3. Replace `vacuum.dreame` with your vacuum’s entity ID, then select **Perform action**.

```yaml
action: dreame_vacuum.vacuum_install_voice_pack
target:
  entity_id: vacuum.dreame
data:
  lang_id: "UK"
  url: https://raw.githubusercontent.com/oleksandr-belei/dreame-vacuum-uk-voice-packs/main/voice_packs/uk_female_pensive
  md5: "55bfe4272ce1e77d9bbafebf9ec99330"
  size: 3585448
```

## Other installation methods

- **Valetudo.** If your model supports voice pack management, open the voice pack controls in Valetudo and use the download URL, language ID, MD5, and byte count shown above. [Valetudo’s model and capability list](https://valetudo.cloud/pages/usage/implementation-overview/)
- **python-miio.** For models supported by its Dreame integration, see the [`set_voice` API reference](https://python-miio.readthedocs.io/en/latest/api/miio.integrations.dreame.vacuum.dreamevacuum_miot.html#miio.integrations.dreame.vacuum.dreamevacuum_miot.DreameVacuum.set_voice) for the required arguments. Check device support before using this method.

## Contributing

To suggest a translation correction, open a pull request editing [the Ukrainian voice mapping](ua_voice_mapping.csv). Include your vacuum model and firmware version when reporting an installation issue.

For questions and feedback, use [GitHub Discussions](https://github.com/oleksandr-belei/dreame-vacuum-uk-voice-packs/discussions).

## License

[MIT](LICENSE). This is an independent project and has no affiliation with Dreame.

[Support the project](https://www.buymeacoffee.com/oleksandr.belei)
