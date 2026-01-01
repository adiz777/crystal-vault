# Crystal Vault Workflow

All scripts should be created in and run from: `C:\Users\Squir\Desktop\crystal-vault\Scripts`

---

## Current Scripts

### 1. download_media.py
**Purpose**: Downloads raw media files from Venezuelan government WordPress APIs
**Sources**: SAIME, SAREN, VTV, AVN, Patria
**Output**: `exfil/media/{source}/` directories

```bash
cd C:\Users\Squir\Desktop\crystal-vault\Scripts
python download_media.py
```

---

### 2. extract_exif.py
**Purpose**: Scans all downloaded media and extracts EXIF metadata (GPS, timestamps, camera info)
**Input**: `exfil/media/` directories
**Output**:
- `exfil/reports/EXIF_REPORT.json`
- `exfil/reports/ALL_GPS_COORDINATES.json`
- `exfil/reports/STAFF_PHONE_GPS_INTEL.json`

```bash
cd C:\Users\Squir\Desktop\crystal-vault\Scripts
python extract_exif.py
```

---

### 3. extract_exif_full.py
**Purpose**: Extended EXIF extraction with additional metadata fields
**Input**: `exfil/media/` directories
**Output**: Full EXIF report with all available tags

```bash
cd C:\Users\Squir\Desktop\crystal-vault\Scripts
python extract_exif_full.py
```

---

### 4. extract_gps_accurate.py
**Purpose**: High-precision GPS coordinate extraction from EXIF data
**Input**: `exfil/media/` directories
**Output**: Accurate GPS coordinates with decimal degree conversion

```bash
cd C:\Users\Squir\Desktop\crystal-vault\Scripts
python extract_gps_accurate.py
```

---

### 5. analyze_exif.py
**Purpose**: Analyzes EXIF data to identify camera equipment, timestamps, and generates reports
**Input**: `exfil/media/` directories
**Output**:
- `exfil/EXIF_REPORT.json`
- `exfil/EXIF_REPORT.txt`

```bash
cd C:\Users\Squir\Desktop\crystal-vault\Scripts
python analyze_exif.py
```

---

### 6. build_dashboard.py
**Purpose**: Generates the interactive HTML dashboard with maps, sanctions data, and media gallery
**Input**: All JSON data files in `exfil/`
**Output**: `index.html` (main dashboard)

```bash
cd C:\Users\Squir\Desktop\crystal-vault\Scripts
python build_dashboard.py
```

---

## Workflow Order

1. **Download Media** - Run `download_media.py` to fetch media files
2. **Extract EXIF** - Run `extract_exif.py` or `extract_exif_full.py` to pull metadata
3. **Analyze Data** - Run `analyze_exif.py` for detailed analysis
4. **Build Dashboard** - Run `build_dashboard.py` to generate HTML output

---

## Dependencies

```bash
pip install pillow requests
```

---

## Adding New Scripts

When creating new scripts:
1. Save to `C:\Users\Squir\Desktop\crystal-vault\Scripts\`
2. Document the script in this workflow file
3. Include: purpose, inputs, outputs, and run command

---

## Data Directories

| Directory | Contents |
|-----------|----------|
| `exfil/` | Exfiltrated raw data (JSON files) |
| `exfil/media/` | Downloaded media files by source |
| `exfil/reports/` | Generated analysis reports |
| `OFAC_Sanctions/` | US Treasury sanctions data |
| `Scripts/` | All Python scripts |

---

## Notes

- All scripts use absolute paths configured for this machine
- Media directory: `C:\Users\Squir\Desktop\crystal-vault\exfil\media`
- Reports directory: `C:\Users\Squir\Desktop\crystal-vault\exfil\reports`
