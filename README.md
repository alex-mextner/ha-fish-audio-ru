# Fish Audio (RU)

Custom Home Assistant integration extending the official [Fish Audio](https://www.home-assistant.io/integrations/fish_audio) TTS service with **Russian language support**.

## Problem

The upstream Fish Audio integration does not declare `"ru"` in `TTS_SUPPORTED_LANGUAGES`. Because Home Assistant's voice pipeline UI filters TTS engines by language, the J.A.R.V.I.S voice (or any Fish Audio voice) is **invisible** in Russian-language assist pipelines — even though Fish Audio itself is language-agnostic.

## Fix

This custom component overrides the official `fish_audio` integration and adds `"ru"` to `TTS_SUPPORTED_LANGUAGES`. After installing and restarting Home Assistant, Fish Audio voices become selectable in Russian assist pipelines.

## Installation

### Method 1: HACS

1. Add this repository as a custom repository in HACS (type: Integration).
2. Install **Fish Audio (RU)**.
3. Restart Home Assistant.

### Method 2: Manual

1. Copy the `custom_components/fish_audio` folder into your Home Assistant `config/custom_components/` directory.
2. Restart Home Assistant.

## Usage

No additional configuration is required beyond the standard Fish Audio integration setup. Existing API keys and voice entries continue to work.

## Upstream PR

A pull request to add Russian language support to the official Home Assistant core integration has been submitted. Once merged, this custom component will no longer be necessary.

## License

Same as Home Assistant core — Apache 2.0.
