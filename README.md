# Home Assistant integration for Nature Remo

Yet another [Home Assistant](https://www.home-assistant.io) component for [Nature Remo](https://en.nature.global/en/).

⚠️This integration is neither Nature Remo official nor Home Assistant official. **Use at your own risk.** ⚠️

## Supported features

- [x] Air Conditioner
  - [x] Set mode (e.g. cool, warm, blow etc.)
  - [x] Set temperature
  - [x] Set fan mode
  - [x] Set swing mode
  - [x] Show current temperature
  - [x] Remember previous target temperatures when switching modes back and forth

Tested on Home Assistant Core 2021.3.3 on Docker

## Installation

### Install via HACS Custom repositories

https://hacs.xyz/docs/faq/custom_repositories

Enter the following information in the dialog and click ADD button.

Repository: https://github.com/yutoyazaki/hass-nature-remo
Category: Integrations

### Manual Install

1. Download this repository
2. Create `custom_components/nature_remo_nano` folder at your config directory
3. Copy files into it (Just drag&drop whole files would be fine)

```
{path_to_your_config}
├── configuration.yaml
└── custom_components
    └── nature_remo_nano
        ├── __init__.py
        ├── climate.py
        └── manifest.json
```

### Install via git submodule

If you have set up git, you can also install this component by adding submodule to your git repository.

```sh
git submodule add https://github.com/hldh214/hass-nature-remo-nano.git {path_to_custom_component}/nature_remo_nano
```

## Configuration

1. Go to https://home.nature.global and sign in/up
2. Generate access token
3. Add following codes to your `configuration.yaml` file

```yaml
nature_remo_nano:
  access_token: YOUR_ACCESS_TOKEN
```
