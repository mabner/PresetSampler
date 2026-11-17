# Preset Sampler

**Compare Lightroom Classic Develop presets before applying them to your final photographs.**

Preset Sampler is an Adobe Lightroom Classic plug-in that generates JPEG previews using multiple Develop presets, allowing photographers to compare different editing styles without modifying their original photographs.

Instead of manually applying and exporting each preset, select your photographs, choose the presets you wish to compare, and let Preset Sampler generate the variations.

## Features

- **Batch preset comparison** — Generate a JPEG for every selected photograph and Develop preset combination.
- **Manual preset selection** — Choose exactly which installed Lightroom presets to compare.
- **Two Develop modes** — Preserve existing adjustments or produce an independent result.
- **AI-powered preset support** — Apply compatible presets that use Lightroom's adaptive masks and AI adjustments.
- **Optional identification watermark** — Display the original copyright, Develop mode and preset name directly on comparison images.
- **Original photograph protection** — Process photographs using temporary virtual copies rather than modifying the originals.
- **Automatic clean-up** — Safely remove temporary virtual copies after successful export verification.
- **Organised filenames** — Identify the Develop mode and applied preset from the exported filename.
- **Safe batch processing** — Progress reporting, cooperative cancellation and output verification.

## How It Works

1. Select one or more original photographs in Lightroom Classic's **Library** module.
2. Open **Library > Preset Sampler...**.
3. Select the Develop presets you want to compare.
4. Choose your preferred Develop mode.
5. Enable or disable the identification watermark.
6. Choose a destination folder.
7. Start the export.

Preset Sampler generates a separate JPEG for each photograph and preset combination.

For example, selecting **10 photographs** and **5 presets** produces **50 JPEG previews**.

### Develop Modes

**Preserve Existing Develop Settings**

Applies the selected preset over the photograph's existing Develop adjustments. This is useful when comparing presets against photographs that have already been edited.

**Independent Result**

Resets the temporary virtual copy's Develop adjustments before applying the selected preset. This allows you to compare how each preset performs independently of existing edits.

Both modes keep the original photographs unchanged.

## Identification Watermarks

Preset Sampler can automatically add a native Lightroom Copyright-based watermark to exported comparison images.

The watermark includes:

`Original Copyright | Develop Mode | Preset Name`

Example:

`© 2026 Photographer | Independent | Warm Portrait`

The watermark is **enabled by default** and can be disabled from the plug-in's preset-selection dialogue.

This identification also appears in the exported JPEG's Copyright metadata when watermarking is enabled.

**Important:** These JPEGs are intended as visual comparison proofs, not final photographs for client delivery. Custom watermark designs are not supported; the plug-in prioritises dynamically identifying each photograph and preset.

## Export Settings

| Setting | Value |
|---|---|
| Format | JPEG |
| Colour space | sRGB |
| Image dimensions | Full resolution |
| JPEG quality | 90% |
| Metadata | Preserved, with an identification label in Copyright when watermarking is enabled |
| File collisions | Automatic renaming |
| Destination | User-selected folder |

### File Naming

Exported JPEGs include the Develop mode and preset name.

Examples:

```text
Portrait_001_Preserve_Warm Portrait.jpg
Portrait_001_Independent_Warm Portrait.jpg
```

This makes it easier to organise previews and identify the presets you want to apply during your final editing workflow.

## Download

Download the latest available version from the repository's [Releases](https://github.com/mabner/PresetSampler/releases) page.

Each published release will provide installation files and release notes.

**Current version: 0.9.1**

## Installation

1. Download the appropriate release archive.
2. Extract the archive to a permanent folder on your computer.
3. Open Adobe Lightroom Classic.
4. Navigate to **File > Plug-in Manager**.
5. Click **Add**.
6. Select the extracted Preset Sampler plug-in folder.
7. Confirm that the plug-in is enabled.

Once installed, open the **Library** module and select **Library > Preset Sampler...**.

## Requirements

- Adobe Lightroom Classic
- Lightroom Classic SDK compatibility: 15.3 or later
- Windows (primary tested development platform)

**Compatibility note:** Development and functional testing have been carried out with Lightroom Classic 15.6 on Windows. Compatibility with other Lightroom versions and operating systems is not guaranteed.

Preset Sampler is designed for Lightroom Classic, not the cloud-based Adobe Lightroom application.

## Safety and Original Photograph Protection

Preset Sampler is designed to protect your original photographs throughout the comparison process.

During export, the plug-in creates temporary virtual copies, applies the selected Develop presets, generates the JPEG previews and verifies the exported files.

After successful verification, temporary copies created during the operation are removed.

If an operation fails or is cancelled before safe clean-up can be completed, affected temporary copies may remain in the Lightroom catalogue for manual inspection.

Original photographs and pre-existing virtual copies are preserved.

## Feedback and Bug Reports

If you encounter an issue or have a suggestion, please use the repository's [Issues](https://github.com/mabner/PresetSampler/issues) section.

When reporting a problem, please include:

- Your Lightroom Classic version.
- Your operating system.
- The Preset Sampler version.
- A description of the problem.
- Any relevant error messages.

Please avoid uploading private photographs, catalogues or personal information unless you have explicitly chosen to share them.

## Licence

**Copyright © 2026 Marcos Leite. All rights reserved.**

Preset Sampler is proprietary software. Public availability of its installation packages does not grant permission to redistribute, modify, reverse-engineer or commercially reuse its software beyond the terms of the applicable licence.

A separate end-user licence may accompany future releases.

---

**Preset Sampler** — Compare presets. Choose your look. Keep your originals.
