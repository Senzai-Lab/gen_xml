Generate XML configuration from OpenEphys recordings for NeuroScope.

### Installation
```bash
uv tool install "gen_xml@git+https://github.com/Senzai-Lab/gen_xml.git"
```

### Usage
```bash
gen-xml /path/to/openephys/session
```

Note that by default it uses `--pad_groups 10` which takes the first channel of each shank, turns it invisible and duplicates it to visualize gap between shanks. To avoid this behavior, run:
```gen-xml /path/to/openephys/session --pad_groups 0```