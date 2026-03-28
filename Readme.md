# 📸 TripAlbum — Smart Travel Photo Album Generator

> *Because your travel memories deserve more than a folder on a hard drive.*

---

## 💡 The Idea

Every trip generates hundreds of photos. They pile up on your phone or hard disk, rarely revisited, slowly forgotten. What if you could dump all those photos into a tool and get back a **beautifully laid out, print-ready photo album** — sorted, curated, and designed automatically?

**TripAlbum** is a smart photo album generator that:
- Takes a raw dump of travel photos
- Filters out blurry, duplicate, and low-quality shots
- Sorts photos by date and location using EXIF metadata
- Asks you a few simple questions about your preferences
- Generates a clean, print-ready PDF album — ready to send to any photo printer

The goal is simple: **feel your memories in your hands, not just on a screen.**

---

## 🎯 Core Features (Planned)

### Phase 1 — MVP (Core Pipeline)
- [ ] Ingest a folder of photos (JPG, PNG, HEIC)
- [ ] Parse EXIF metadata (date, GPS location, camera info)
- [ ] Sort photos chronologically
- [ ] Basic quality filtering — detect and remove blurry or very dark photos
- [ ] Remove near-duplicate shots
- [ ] Generate a simple PDF album with a grid layout

### Phase 2 — Customisation
- [ ] Interactive CLI questionnaire:
  - How many pages do you want?
  - How many photos per page? (1, 2, 4, 6...)
  - Do you have a theme in mind? (Minimal, Vintage, Bold, Travel Journal)
  - Do you want captions auto-generated from location data?
- [ ] Multiple layout templates
- [ ] Cover page with trip title, date range, and a hero photo

### Phase 3 — Intelligence Layer
- [ ] AI-powered best-shot selection (face detection, composition scoring)
- [ ] Auto-group photos into "chapters" by day or location
- [ ] Auto-generate location-based captions (e.g. "Day 3 — Kotor, Montenegro")
- [ ] Suggest a cover photo

### Phase 4 — Memorial Video (Optional)
- [ ] Generate a short slideshow video from curated photos
- [ ] Add background music selection
- [ ] Transitions and title cards

---

## 🛠️ Planned Tech Stack

| Layer | Tool / Library | Purpose |
|---|---|---|
| Language | Python 3.10+ | Core application logic |
| Image Processing | OpenCV, Pillow | Blur detection, resizing, filtering |
| Metadata | ExifRead / Pillow | Date, GPS, camera data extraction |
| Duplicate Detection | imagehash | Perceptual hashing for near-duplicates |
| PDF Generation | ReportLab / WeasyPrint | Album layout and export |
| CLI Interface | Typer / Click | User interaction and configuration |
| AI (later) | CLIP / OpenCV DNN | Photo quality and composition scoring |
| Video (later) | MoviePy | Slideshow video generation |

---

## 📁 Project Structure (Planned)

```
tripalbum/
│
├── tripalbum/
│   ├── __init__.py
│   ├── ingest.py          # Load photos from a folder
│   ├── metadata.py        # EXIF parsing and sorting
│   ├── filter.py          # Quality filtering, blur detection, dedup
│   ├── layout.py          # Page layout engine
│   ├── export.py          # PDF generation
│   ├── questionnaire.py   # CLI user input flow
│   └── video.py           # (Phase 4) Video generation
│
├── templates/             # Album layout templates
├── samples/               # Sample photos for testing
├── tests/                 # Unit tests
├── output/                # Generated albums go here
│
├── main.py                # Entry point
├── requirements.txt
└── README.md
```

---

## 🚀 Getting Started (Coming Soon)

```bash
# Clone the repo
git clone https://github.com/yourusername/tripalbum.git
cd tripalbum

# Install dependencies
pip install -r requirements.txt

# Run the album generator
python main.py --input ./my_trip_photos/
```

---

## 🗺️ Roadmap

```
v0.1  ──── Folder ingestion + EXIF sort + basic PDF output
v0.2  ──── Blur detection + duplicate removal
v0.3  ──── CLI questionnaire + layout options
v0.4  ──── Design templates + cover page
v0.5  ──── AI-powered photo selection + location captions
v1.0  ──── Polished MVP — end-to-end album generation
v1.x  ──── Memorial video generation
```

---

## 🧠 Why This Project?

This started from a personal frustration — opening the Photos app, seeing hundreds of travel pictures, and wishing there was an easy way to have them as a **physical album** without spending hours arranging them manually.

This project is being built gradually, one phase at a time, as a side project. Contributions and ideas are welcome!

---

## 📬 Contact

Built by [Govardhan Bali](mailto:govardhanbali@gmail.com) — [LinkedIn](https://linkedin.com/in/govardhanbali)

---

*"The best camera is the one you have with you. The best album is the one you actually make."*
