[![Buy Me a Coffee](https://img.shields.io/badge/Buy%20Me%20a%20Coffee-Donate-orange.svg)](https://www.buymeacoffee.com/oleksandr.belei)

<h1 align="center">Dreame Vacuum Ukrainian Voice Packs</h1>

Enhance your Dreame vacuum cleaner with a custom Ukrainian voice packs. Enjoy voice notifications in the Ukrainian language for cleaning progress, battery status, cleaning scheduling, errors, and more.

## 💡Introduction

Since the official Dreame app lacks native Ukrainian language support, this project was created to provide Ukrainian voice packs for your Dreame vacuum cleaner. These voice packs are created using paid AI voice generation services and then fine-tuned with Audacity to ensure quality audio output.

>In case of any inaccuracies in the translation, please feel free to contribute and help to improve the voice packs.

## 🚀Features

**Available Voice Packs:**

| Voice Pack                                     | Description                                | Hash                            | Size           | Samples                                             |
|-----------------------------------------------|--------------------------------------------|---------------------------------|----------------|-----------------------------------------------------------|
| [uk_female_pensive](voice_packs/uk_female_pensive/) | *Pensive, introspective, soft, and lovely* | `b4da556caad4800eba706dd788bcb560` | `3585546` | <p align="center">[🔗](voice_samples/uk_female_pensive)</p> |


## ⚙️Installation

You can install the Ukrainian voice pack on your Dreame vacuum cleaner using one of the following methods:

### 1. Installing on Official Firmware with [Home Assistant](https://www.home-assistant.io/)
- Install the custom [Dreame vacuum](https://github.com/Tasshack/dreame-vacuum.git)  integration for Home Assistant, created by **@Tasshack**.
- In Home Assistant, navigate to `"Developer Tools"` -> `"Services"` and switch to `YAML mode`.
- Paste the following code:

  ```yaml
  service: dreame_vacuum.vacuum_install_voice_pack
  data:
    lang_id: UK
    url: Raw URL for the voice pack from the "voice_packs" directory in this repository.
    md5: The hash of the voice pack.
    size: The file size of the voice pack in bytes.
  target:
    entity_id: vacuum.dreame
  ```
- Call the service to set the new voice pack.

### 2. Installing on Custom Firmware with [Valetudo](https://valetudo.cloud/)
- Open Valetudo's web interface by entering your vacuum's IP address in a web browser.
- In Valetudo, navigate to `"Robot Settings"`-> `"Misc Settings."`
- Enter the following information in the `"Voice packs"` section:
    - **URL:** Raw URL for the voice pack from the "voice_packs" directory in this repository.
    - **Language Code:** 'UK'
    - **Hash:** The hash of the voice pack.
    - **File size:** The file size of the voice pack in bytes.
- Save the settings by clicking `"Set Voice Pack`."

### 3. Installing on Official Firmware with [Python MIIO](https://python-miio.readthedocs.io/en/latest/)
Detailed installation instructions can be found in the [python-miio](https://github.com/rytilahti/python-miio.git) repository, created by **@rytilahti**.

## 🤝Contribution

Contribute to this project by helping correct any translation errors. If you find any inaccuracies in the translation, please create a pull request with your corrections in the [voice_mapping.csv](voice_mapping.csv) file.

Your input is essential to the improvement of Dreame vacuum cleaner voice packs and your participation is highly appreciated.

## 📜License

This project is open-source and available under the [MIT License](LICENSE). You are free to use and modify it as per the terms of the license.

## 💬Discussions

If you have any questions, suggestions, or feedback, please visit the [Discussion](../../discussions) tab of this repository. Feel free to start a new discussion or join existing ones.

---

❗**Disclaimer:** This project is not affiliated with or endorsed by Dreame or its parent companies. It is an independent, community-driven effort to provide voice packs for Dreame Vacuum Cleaners.

<a href="https://www.buymeacoffee.com/oleksandr.belei" target="_blank"><img src="https://cdn.buymeacoffee.com/buttons/default-orange.png" alt="Buy Me A Coffee" height="41" width="174" align="right"></a>
