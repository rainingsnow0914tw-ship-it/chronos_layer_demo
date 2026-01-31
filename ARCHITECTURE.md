# Chronos Layer - System Architecture

## 📐 Technical Flow Diagram

```
┌─────────────────────────────────────────────────────────────────┐
│                     CHRONOS LAYER ARCHITECTURE                  │
│                  Multimodal Time Reconstruction                 │
└─────────────────────────────────────────────────────────────────┘

                              USER INPUT
                                  │
                                  ▼
                    ┌─────────────────────────┐
                    │   Photo Upload          │
                    │   (Modern Landmark/     │
                    │    Person at Location)  │
                    └───────────┬─────────────┘
                                │
                                ▼
┌───────────────────────────────────────────────────────────────────┐
│                        STAGE 1: ANALYSIS                          │
└───────────────────────────────────────────────────────────────────┘
                                │
                ┌───────────────┴────────────────┐
                ▼                                ▼
    ┌─────────────────────┐        ┌─────────────────────┐
    │ Gemini Vision API   │        │ Google Maps         │
    │                     │        │ Geocoding API       │
    │ • Scene Analysis    │        │                     │
    │ • Object Detection  │        │ • Location ID       │
    │ • Facial Features   │        │ • Coordinates       │
    └──────────┬──────────┘        └──────────┬──────────┘
               │                               │
               └───────────────┬───────────────┘
                               ▼
┌───────────────────────────────────────────────────────────────────┐
│                     STAGE 2: RESEARCH                             │
└───────────────────────────────────────────────────────────────────┘
                               │
               ┌───────────────┴────────────────┐
               ▼                                ▼
   ┌──────────────────────┐        ┌──────────────────────┐
   │ Google Books API     │        │ Google Search API    │
   │                      │        │                      │
   │ • Historical Texts   │        │ • Historical Context │
   │ • Costume Reference  │        │ • Era Verification   │
   │ • Architecture Data  │        │ • Cultural Details   │
   └──────────┬───────────┘        └──────────┬───────────┘
              │                               │
              └───────────────┬───────────────┘
                              ▼
┌───────────────────────────────────────────────────────────────────┐
│                   STAGE 3: REASONING                              │
└───────────────────────────────────────────────────────────────────┘
                              │
                              ▼
                 ┌──────────────────────────┐
                 │ Gemini 2.0 Flash         │
                 │ Thinking                 │
                 │                          │
                 │ • Validate Era           │
                 │ • Cross-Reference Data   │
                 │ • Infer Costume Details  │
                 │ • Generate Assumptions   │
                 │ • Historical Reasoning   │
                 │   (e.g., 1868 = B&W)     │
                 └────────────┬─────────────┘
                              │
                              ▼
┌───────────────────────────────────────────────────────────────────┐
│                   STAGE 4: GENERATION                             │
└───────────────────────────────────────────────────────────────────┘
                              │
                              ▼
                 ┌──────────────────────────┐
                 │ Imagen 3                 │
                 │ (nano banana Pro)        │
                 │                          │
                 │ • Preserve Face          │
                 │ • Transform Clothing     │
                 │ • Reconstruct Background │
                 │ • Apply Era Filters      │
                 │ • High-Fidelity Output   │
                 └────────────┬─────────────┘
                              │
                              ▼
┌───────────────────────────────────────────────────────────────────┐
│                   STAGE 5: PRESENTATION                           │
└───────────────────────────────────────────────────────────────────┘
                              │
                              ▼
                 ┌──────────────────────────┐
                 │ Interactive UI           │
                 │                          │
                 │ • Before/After Slider    │
                 │ • Narrative Timeline     │
                 │ • Assumptions Panel      │
                 │ • Confidence Metrics     │
                 └──────────────────────────┘
                              │
                              ▼
                        USER OUTPUT


═══════════════════════════════════════════════════════════════════

## 🔑 Key Technical Components

### Google APIs Used:
1. **Gemini Vision API**: Image analysis and scene understanding
2. **Google Maps Geocoding API**: Location identification
3. **Google Books API**: Historical document research
4. **Google Search API**: Contextual historical data
5. **Gemini 2.0 Flash Thinking**: Multimodal reasoning engine
6. **Imagen 3**: High-fidelity image generation

### Data Flow:
```
Photo → Vision Analysis → Location ID → Historical Research 
     → Reasoning & Validation → Image Generation → Interactive UI
```

### Example: Himeji Castle Transformation (1600)

```
INPUT: Modern tourist photo at Himeji Castle
  ↓
VISION: Detects person, castle, lighting, composition
  ↓
MAPS: Identifies "Himeji Castle, Hyogo Prefecture, Japan"
  ↓
BOOKS: Retrieves《日本戰國史料集》for 1600 Sengoku attire
  ↓
REASONING: Validates armor style (Tosei-gusoku), family crest placement
  ↓
IMAGEN 3: Generates Sengoku warrior with preserved facial features
  ↓
OUTPUT: Person in period-accurate armor + castle town background
```

### Historical Accuracy Validation:

Each reconstruction includes:
- **Cited Sources**: Historical texts, architectural records
- **Assumptions**: Explicit hypotheses (e.g., "Red clay tile roof")
- **Confidence Score**: 0.85-0.95 based on source quality
- **Era Metadata**: Year, cultural context, verification method

═══════════════════════════════════════════════════════════════════

## 💡 Innovation Highlights

1. **Multimodal Intelligence**: Combines Vision, Text, Geospatial, and Historical data
2. **Evidence-Based**: Every pixel justified by historical documentation
3. **Person-Aware**: Preserves facial identity while transforming context
4. **Temporal Reasoning**: AI understands "1868 = Black & White photography"
5. **Educational Value**: Teaches history through participation, not observation

═══════════════════════════════════════════════════════════════════

## 🎯 Use Cases

- **Tourism**: Virtual time-travel experiences at heritage sites
- **Education**: Students "become" historical figures
- **Museums**: Interactive exhibits with visitor participation
- **Cultural Preservation**: Document endangered sites with temporal context
- **Entertainment**: Historical role-play, period drama visualization

═══════════════════════════════════════════════════════════════════

## 📊 Technical Specifications

- **Platform**: Web-based (HTML5 + JavaScript)
- **Deployment**: Static HTML (no server required)
- **File Size**: 2.4MB (optimized images + single HTML)
- **Compatibility**: Modern browsers (Chrome, Edge, Safari, Firefox)
- **Offline Capable**: Embedded assets for exhibition mode
- **Response Time**: 3-5s per reconstruction (API-dependent)

═══════════════════════════════════════════════════════════════════

Built for Gemini 3 Hackathon 2026
By: Chloe (Developer) + Claude (AI Collaborator)
