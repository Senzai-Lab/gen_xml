Generate XML configuration from OpenEphys recordings for NeuroScope.

### Installation
```bash
uv tool install "gen_xml@git+https://github.com/Senzai-Lab/gen_xml.git"
```

### Usage
For OpenEphys sessions. (Path to folder containing Record node)
```bash
gen-xml --from_openephys /path/to/openephys/session
```

From SpikeInterface recording (concatenated files)
```bash
gen-xml --from_si /path/to/si
```

From ProbeInterface configuration (JSON file).
Sampling rate should be passed with `--fs`
```bash
gen-xml --from_probe /path/to/probe.json --fs 1250 --name eeg.xml
```

Note that by default it uses `--pad_groups 10` which takes the first channel of each shank, turns it invisible and duplicates it to visualize gap between shanks. To avoid this behavior, add:
```--pad_groups 0```