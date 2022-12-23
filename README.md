# pyfluidsynth-patch

Patch for [pyFluidSynth](https://github.com/nwhitehead/pyfluidsynth) to enable tuning functions of FluidSynth.


## Source of `pyFluidSynth` and copyright

The original `pyFluidSynth` is located at
https://github.com/nwhitehead/pyfluidsynth

All rights to `pyFluidSynth` belong to the developers of the [pyfluidsynth](https://github.com/nwhitehead/pyfluidsynth).


## What is patched in `pyFluidSynth`

[pyFluidSynth](https://github.com/nwhitehead/pyfluidsynth) is a Python wrapper for FluidSynth C APIs.  Unfortunately, the module does not include tuning
functions.

Refer to [FluidSynth API reference](https://www.fluidsynth.org/api/modules.html) for patching the latest version.

The `FluidSynth` and `pyFluidSynth` versions that are supported by this project:

| FluidSynth | pyFluidSynth |
|:-----------|:-------------|
| 2.3.0      | 1.3.1        |
| 2.1.5      | 1.3.0        |
| 2.1.2      | 1.3.0        |

### Added signatures for cfuncs

| cfunc                                | Comment                              |
|:-------------------------------------|:-------------------------------------|
| fluid_synth_activate_key_tuning()    | Only prior to `pyFluidSynth` `1.3.1` |
| fluid_synth_activate_octave_tuning() |                                      |
| fluid_synth_activate_tuning()        | Only prior to `pyFluidSynth` `1.3.1` |
| fluid_synth_deactivate_tuning()      | Only prior to `pyFluidSynth` `1.3.1` |

### Added Python wrapper functions

| def                      | Comment |
|:-------------------------|:--------|
| activate_key_tuning()    |         |
| activate_octave_tuning() |         |
| activate_tuning()        |         |
| deactivate_tuning()      |         |


## Installation

Suppose that `FluidSynth` version `x.y.z` is installed on your system, and it is verified that a MIDI file can be played as explained on the
[Getting Started](https://github.com/FluidSynth/fluidsynth/wiki/GettingStarted) page.

1. Install [pyFluidSynth](https://github.com/nwhitehead/pyfluidsynth) as described on the official site.  

2. Copy the `patches/fs-x.y.z/fluidsynth.py` to where the `fluidsynth.py` is installed:

macOS: `/Library/Frameworks/Python.framework/Versions/3.x/lib/python3.x/site-packages/fluidsynth.py`

Linux:
- `/usr/lib/python3.x/site-packages/fluidsynth.py`
or
- `~/.local/lib/python3.x/site-packages/fluidsynth.py`

If you use `pypoetry`:
- `~/.cache/pypoetry/src/pyfluidsynth/fluidsynth.py`
- `~/.cache/pypoetry/virtualenvs/myproject-py3.x/lib/python3.x/site-packages/fluidsynth.py`
- `~/.cache/pypoetry/virtualenvs/myproject-py3.x/src/pyfluidsynth/build/lib/fluidsynth.py`
- `~/.cache/pypoetry/virtualenvs/myproject-py3.x/src/pyfluidsynth/fluidsynth.py`
