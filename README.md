# Argo Translate GoldenDict Integration

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

A configuration guide and ecosystem for integrating Argo Translate with GoldenDict-ng for offline translation.

## Table of Contents
- [Description](#description)
- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Kardenwort Ecosystem](#kardenwort-ecosystem)
- [License](#license)

---

## Description
This project provides the necessary configuration and environment setup to use Argo Translate as an external program within GoldenDict-ng. It enables offline translation capabilities directly within your dictionary interface.

[Return to Top](#argo-translate-goldendict-integration)

## Features
- **Offline Translation**: Uses Argo Translate for neural machine translation without an internet connection.
- **GoldenDict Integration**: Seamlessly integrates into GoldenDict-ng using external program definitions.
- **Multiple Language Pairs**: Supports configuration for various language pairs (e.g., En-Ru, En-De, De-Ru).

[Return to Top](#argo-translate-goldendict-integration)

## Installation

### 1. Environment Setup
Ensure you have a Python environment with `argos-translate` installed.
```bash
# Example setup
python -m venv venv
.\venv\Scripts\activate
pip install argos-translate
```
*Note: You may need to install language packages for Argo Translate separately.*

### 2. GoldenDict-ng Configuration
To add the translators to GoldenDict-ng:

1. Open GoldenDict-ng.
2. Navigate to **Edit** > **Dictionaries** > **Programs**.
3. Add a new entry for each language pair you wish to support.
4. Use the following configuration patterns (adjust usage of `python.exe` and `argos-translate` paths to match your environment):

**English -> Russian**
- **Name**: `aR En-Ru`
- **Command Line**:
  ```cmd
  "U:\voothi\20241121100211-argotranslate\venv\Scripts\python.exe" "U:\voothi\20241121100211-argotranslate\venv\Scripts\argos-translate" -f en -t ru "%GDWORD%"
  ```

**English -> German**
- **Name**: `aR En-De`
- **Command Line**:
  ```cmd
  "U:\voothi\20241121100211-argotranslate\venv\Scripts\python.exe" "U:\voothi\20241121100211-argotranslate\venv\Scripts\argos-translate" -f en -t de "%GDWORD%"
  ```

**German -> Russian**
- **Name**: `aR De-Ru`
- **Command Line**:
  ```cmd
  "U:\voothi\20241121100211-argotranslate\venv\Scripts\python.exe" "U:\voothi\20241121100211-argotranslate\venv\Scripts\argos-translate" -f de -t ru "%GDWORD%"
  ```

**German -> English**
- **Name**: `aR De-En`
- **Command Line**:
  ```cmd
  "U:\voothi\20241121100211-argotranslate\venv\Scripts\python.exe" "U:\voothi\20241121100211-argotranslate\venv\Scripts\argos-translate" -f de -t en "%GDWORD%"
  ```

**Russian -> English**
- **Name**: `aR Ru-En`
- **Command Line**:
  ```cmd
  "U:\voothi\20241121100211-argotranslate\venv\Scripts\python.exe" "U:\voothi\20241121100211-argotranslate\venv\Scripts\argos-translate" -f ru -t en "%GDWORD%"
  ```

**Russian -> German**
- **Name**: `aR Ru-De`
- **Command Line**:
  ```cmd
  "U:\voothi\20241121100211-argotranslate\venv\Scripts\python.exe" "U:\voothi\20241121100211-argotranslate\venv\Scripts\argos-translate" -f ru -t de "%GDWORD%"
  ```

[Return to Top](#argo-translate-goldendict-integration)

## Usage

Once configured:
1. Search for a word in GoldenDict-ng.
2. The configured "Programs" will appear as dictionary results, showing the translation from Argo Translate.

[Return to Top](#argo-translate-goldendict-integration)

## Kardenwort Ecosystem

This project is part of the **[Kardenwort](https://github.com/kardenwort)** environment, designed to create a focused and efficient learning ecosystem.

[Return to Top](#table-of-contents)

## License
MIT
