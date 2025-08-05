# Video Podcast Room Setup & Workflow Guide

## Overview
This document outlines a complete video podcast production system designed for daily recording with efficient post-production turnaround. The setup supports 4 podcast microphones, 3 cameras with live switching capabilities, and maintains individual track recording for maximum flexibility in post.

---

## Audio Equipment

### Microphones
- **Primary Choice:** Shure SM7B (4 units)
  - Industry-standard podcast microphone
  - Excellent background noise rejection
  - Requires good preamp/cloudlifter
  - Consistent sound across all hosts

### Audio Interface/Mixer Options

#### Option 1: Zoom PodTrak P8 (Recommended)
- 6 XLR inputs with phantom power
- Individual track recording to SD card
- Built-in sound pads for intro/outro music
- Individual headphone outputs for each host
- USB interface capability for backup recording
- Price: $300 (B&H Photo)

#### Option 2: Rodecaster Pro II (Premium)
- 4 XLR inputs + wireless capability
- Advanced processing and effects
- Touchscreen interface
- Price: ~$700

#### Option 3: Tascam Model 12 (Hybrid)
- Full mixing console with faders
- 10-track recording capability
- More complex but very flexible
- Price: ~$600

### Additional Audio Gear
- **XLR Cables:** Kopul Studio Elite 4000 Series (4x 25'): $99.80
  - Professional Neutrik connectors
  - 25' length for flexible positioning in 20x20ft room
  - $24.95 each x 4 cables
- **Boom Arms:** Elgato Wave Mic Arm LP (4x): $399.96
  - Low-profile design perfect for podcasting
  - Premium build quality
  - Cable management system
  - $99.99 each x 4 arms (B&H Photo)
- **Pop Filters:** Universal pop filters (4x): ~$100
  - Essential for SM7B plosive protection
  - ~$25 each
- **Headphones:** Sony MDR-7506 (1 pair): ~$100
  - Industry-standard monitoring
  - Closed-back design
- **Headphone Amplifier** (Only needed for Option 1): ~$60
  - Mackie HM-4 or similar
  - Distributes audio to multiple headphones
  - Not needed with ATEM Television Studio HD8 ISO

---

## Video Equipment

### Production Monitor
**Feelworld ATEM156 15.6" 4K HDMI Monitor**
- 15.6" IPS Panel with 4K support
- Multiple HDMI inputs for confidence monitoring
- Perfect for monitoring program output
- Waveform, vectorscope, and histogram tools
- Price: $599.95 (B&H Photo)
- Essential for quality control during recording

### Camera Setup

#### Wide Shot Camera (Wall-Mounted)
**Camera Options:**
- Sony ZV-E10 with 10-18mm lens
- Canon M50 Mark II with wide angle lens
- Must have clean HDMI output

**Mounting:**
- Elgato Wall Mount
- SmallRig Articulating Arm
- Position for full room coverage

#### Close-Up Cameras (2 units)
**Camera Options:**
- Match the wide shot camera model for consistency
- 35mm or 50mm lenses for flattering close-ups
- Clean HDMI output required

**Support:**
- Manfrotto 502AH Video Heads
- Sturdy tripods for smooth adjustments
- Quick-release plates for easy repositioning

### Camera Power & Accessories
- **AC Power Adapters** (3x): ~$90
  - Dummy batteries for continuous power
  - Essential for all-day recording
  - ~$30 per camera
- **HDMI Cables** (3x 25ft): ~$75
  - High-quality cables for 20x20ft room
  - ~$25 each for reliable 4K cables
- **Memory Cards** (6x): ~$180
  - 64GB SD cards for backup recording
  - 2 per camera for rotation
  - ~$30 each

### Live Switching & Recording

#### ATEM Mini Pro ISO (Basic Option)
**Key Features:**
- Records all 4 HDMI inputs as separate files
- Records the live-switched "Program" output
- Frame-accurate synchronization
- Built-in streaming encoder
- Control via hardware or iPad app
- **LIMITATION:** No built-in Audio Follow Video (AFV)

**How ISO Recording Works:**
1. Connect each camera via HDMI (up to 4 inputs)
2. Connect USB-C SSD for recording (Samsung T5/T7 recommended)
3. Press record to capture:
   - Individual camera files (1080p60 H.264)
   - Program file (your live switch decisions)
   - DaVinci Resolve project file
   - Embedded audio from all sources

**File Output Structure:**
```
Recording_001/
├── Video ISO Files/
│   ├── Camera1.mp4
│   ├── Camera2.mp4
│   ├── Camera3.mp4
│   └── Camera4.mp4 (if used)
├── Program.mp4
├── Project.drp
└── Audio files
```

**Storage Requirements:**
- ~8-10GB per camera per hour
- 3 cameras + program ≈ 35-40GB per hour
- Minimum 1TB SSD recommended

---

## Lighting & Studio Infrastructure

### Professional Lighting Setup
- **Soft LED Overhead Lighting System:** ~$6,000
  - Professional-grade soft LED panels
  - Ceiling-mounted with diffusers
  - Even, flattering light for all positions
  - Dimmable and color temperature adjustable

### Support Equipment
- **C-Stands:** Impact Master Century C-Stand Kit (3x): $510
  - Professional-grade support for lights/modifiers
  - $170 each (B&H Photo)
  - 10.75' height with 40" arm and grip heads
  - [B&H Link](https://www.bhphotovideo.com/c/product/372016-REG/Impact_CT40MKIT_Master_Century_C_Stand.html)

### Power Infrastructure
- **Extension Cords** (25ft, 4x): ~$120
  - Heavy-duty for studio equipment
  - ~$30 each for quality cords
- **Power Strips/Surge Protectors** (3x): ~$150
  - Studio-grade with multiple outlets
  - ~$50 each with surge protection
- **Power Distribution:** ~$100
  - Cable management and power splitters
  - Organized power routing for 20x20ft space

---

## Audio-Video Integration: The AFV Challenge

### Understanding Audio Follow Video (AFV)
**The Problem:** In a multi-person podcast, when you switch to a close-up of Person B, you want:
- Microphone B to be prominent in the mix
- Other microphones to automatically lower (duck)
- Smooth, professional transitions
- No manual audio mixing during recording

**Without AFV:** Audio and video are separate systems, requiring manual sync and mixing in post-production.

### Option 1: ATEM Mini Pro ISO + Intelligent Control
**Setup:** Use the basic ATEM with added automation

**Hardware:**
- ATEM Mini Pro ISO: $895
- Zoom PodTrak P8: $300
- Computer running Companion software
- Total added cost: ~$1,195

**How it Works:**
1. **Physical Connections:**
   ```
   Mics → PodTrak P8 → Main Mix → ATEM Audio Input
                    ↓
                 SD Card (Multitrack backup)
   ```

2. **Automation via Companion:**
   - Install Bitfocus Companion (free)
   - Create macros linking camera switches to audio changes
   - When switching to Camera B:
     - Companion sends MIDI to PodTrak
     - Mic B level increases
     - Other mics duck by preset amount

3. **Workflow:**
   - Operator uses ATEM buttons to switch cameras
   - Companion automatically adjusts audio mix
   - Both changes are recorded

**Pros:**
- Keeps equipment costs lower
- Maintains separate audio recording
- Can be customized extensively

**Cons:**
- Requires initial setup and programming
- Another software layer to manage
- Less reliable than hardware AFV

### Option 2: ATEM Television Studio HD8 ISO (Professional)
**Setup:** Upgrade to broadcast-grade switcher with built-in AFV

**Hardware:**
- ATEM Television Studio HD8 ISO: $3,395 (Sweetwater)
- Built-in Fairlight audio mixer
- No separate audio interface needed for basic setup
- Total cost: $3,395 (+ mics and cables)

**How it Works:**
1. **Direct Integration:**
   ```
   Mics → XLR inputs on ATEM Television Studio
              ↓
        Built-in Fairlight Mixer
              ↓
        AFV Processing (automatic)
              ↓
   Embedded in each ISO recording
   ```

2. **AFV Configuration:**
   - Assign each microphone to its corresponding camera:
     - Mic A (XLR 1) → Camera 1
     - Mic B (XLR 2) → Camera 2
     - Mic C (XLR 3) → Camera 3
     - All mics balanced → Camera 4 (wide shot)
   
   - Set AFV parameters:
     - ON level: 0dB (when camera is live)
     - OFF level: -10dB to -15dB (when camera not live)
     - Transition time: 0.5-1.0 seconds

3. **Result:**
   - Switch to Camera B → Mic B automatically at full level
   - Other mics automatically duck
   - Each ISO file has the appropriate audio mix
   - Program file has the live-switched audio

**Advanced Features:**
- 8 HDMI inputs (room for growth)
- 4 XLR inputs with phantom power
- Multiple audio follows options:
  - AFV (Audio Follow Video)
  - Audio-over-Time transitions
  - Split audio/video transitions
- Streaming encoder built-in
- Records all channels separately PLUS the mix

**File Output with AFV:**
```
Recording_001/
├── Video ISO Files/
│   ├── Camera1.mp4 (Mic A prominent when Camera 1 was live)
│   ├── Camera2.mp4 (Mic B prominent when Camera 2 was live)
│   ├── Camera3.mp4 (Mic C prominent when Camera 3 was live)
│   └── Camera4.mp4 (Balanced mix for wide shots)
├── Program.mp4 (Live switch with live audio mix)
├── Audio ISO Files/
│   ├── Mic1.wav
│   ├── Mic2.wav
│   ├── Mic3.wav
│   └── Mic4.wav
└── Project files
```

**Pros:**
- True broadcast-quality AFV
- Rock-solid reliability
- All-in-one solution
- Each camera file has correct audio embedded
- Still maintains separate audio tracks

**Cons:**
- Higher initial investment
- Larger physical footprint
- May be overkill for simple podcasts

### Which Option to Choose?

**Choose Option 1 (ATEM Mini Pro ISO + Automation) if:**
- Budget is a primary concern
- You enjoy tinkering with software
- You want maximum flexibility
- You're okay with occasional manual intervention

**Choose Option 2 (ATEM Television Studio HD8 ISO) if:**
- You need bulletproof reliability
- Daily production efficiency is critical
- You want true broadcast standards
- Budget allows for the investment
- You plan to scale up production

---

## Software & Automation

### Editing Software

#### Adobe Premiere Pro
- Create project templates with:
  - Pre-built multicam sequences
  - Audio processing presets
  - MOGRT templates for lower thirds
  - Export presets for multiple platforms

#### After Effects
- Template projects for:
  - Animated intros/outros
  - Dynamic title cards (CSV-driven)
  - Social media templates
  - Stylized subtitles

### Automation Tools

#### AutoPod (Essential)
- Automatically edits multicam podcasts
- Intelligently switches between speakers
- Huge time saver for daily production
- Works perfectly with ATEM ISO files

#### Additional Tools
- **Descript:** Transcription and rough cuts
- **Gling AI:** Remove silences and filler words
- **Simon Says:** Professional transcription for subtitles

---

## Complete Signal Flow

### Option 1: Basic Setup (ATEM Mini Pro ISO)

#### Audio Path
1. SM7B Microphones → XLR cables → PodTrak P8
2. PodTrak P8 → Main Mix Out → ATEM Audio Input
3. PodTrak P8 → SD card (multitrack recording for post)
4. Optional: Companion software controls audio levels via MIDI

#### Video Path
1. Cameras → HDMI cables → ATEM Mini Pro ISO
2. ATEM → USB-C SSD (all ISO recordings + program)
3. ATEM → HDMI out to confidence monitor
4. All video files share same audio mix (no AFV)

#### Post-Production Requirements
- Manual audio sync required
- Use multitrack from PodTrak for individual control
- More time needed for audio mixing

### Option 2: Professional Setup (ATEM Television Studio HD8 ISO)

#### Integrated Audio/Video Path
1. SM7B Microphones → XLR → ATEM Television Studio HD8
2. Cameras → HDMI → ATEM Television Studio HD8
3. Internal Fairlight mixer processes with AFV
4. Recording outputs:
   - Each ISO file has AFV-processed audio
   - Separate audio ISO files preserved
   - Program file with live mix

#### Post-Production Benefits
- Each camera file already has appropriate audio mix
- Can use as-is for quick turnaround
- Individual audio tracks still available for fine-tuning
- AutoPod works seamlessly with pre-mixed audio

### Post-Production Workflow (Both Options)
1. Import all ISO files into Premiere Pro template
2. Create multicam sequence (or use AutoPod)
3. For Option 1: Sync with multitrack audio from PodTrak
4. For Option 2: Audio already embedded correctly
5. Apply MOGRTs for graphics
6. Export master and social cuts

---

## Daily Operation Workflow

### Pre-Production Checklist
- [ ] Update CSV file with guest names/episode info
- [ ] Check all cable connections
- [ ] Format recording media (SSD and SD cards)
- [ ] Test all microphone levels
- [ ] Verify camera framing
- [ ] Load intro/outro music on PodTrak

### During Recording
- [ ] Start recording on PodTrak P8
- [ ] Start recording on ATEM Mini Pro ISO
- [ ] Monitor audio levels throughout
- [ ] Mark good takes/segments
- [ ] Note any technical issues for post

### Post-Production Pipeline
1. **File Transfer (5 min)**
   - Copy files from SSD to edit station
   - Copy audio from SD card
   - Create project folder from template

2. **Rough Edit (15-30 min with AutoPod)**
   - Import to Premiere template
   - Run AutoPod for initial edit
   - Sync high-quality audio

3. **Fine Edit (30-45 min)**
   - Review AutoPod decisions
   - Add graphics via MOGRTs
   - Color correction if needed
   - Audio sweetening

4. **Export (15-20 min)**
   - Master file (4K or 1080p)
   - YouTube version
   - Podcast platforms (audio only)
   - Social clips (vertical)

---

## Budget Breakdown

### Option 1: Basic Professional Setup (~$16,455)
- Shure SM7B (4x): $1,800
- Zoom PodTrak P8: $300 (B&H Photo)
- ATEM Mini Pro ISO: $895
- Cameras (3x Sony ZV-E10): $2,100
- Lenses: $900
- Tripods/Mounts: $600
- Feelworld ATEM156 Monitor: $600 (B&H Photo)
- Elgato Wave Mic Arm LP (4x): $400 (B&H Photo)
- XLR Cables (4x Kopul 25'): $100
- Pop Filters (4x): $100
- Headphones (Sony MDR-7506): $100
- Headphone Amplifier: $60
- AC Power Adapters (3x): $90
- HDMI Cables (3x 25ft): $75
- Memory Cards (6x): $180
- Extension Cords (4x 25ft): $120
- Power Strips (3x): $150
- Power Distribution: $100
- Soft LED Overhead Lighting: $6,000
- C-Stands (3x Impact): $510 (B&H Photo)
- HDMI Cables & Other Accessories: $200
- SSD Storage (Samsung T7 1TB): $100
- AutoPod License: $29/month
- **Note:** Requires manual audio/video sync in post

### Option 2: AFV Professional Setup (~$18,595)
- Shure SM7B (4x): $1,800
- ATEM Television Studio HD8 ISO: $3,395 (Sweetwater)
- Cameras (3x Sony ZV-E10): $2,100
- Lenses: $900
- Tripods/Mounts: $600
- Feelworld ATEM156 Monitor: $600 (B&H Photo)
- Elgato Wave Mic Arm LP (4x): $400 (B&H Photo)
- XLR Cables (4x Kopul 25'): $100
- Pop Filters (4x): $100
- Headphones (Sony MDR-7506): $100
- AC Power Adapters (3x): $90
- HDMI Cables (3x 25ft): $75
- Memory Cards (6x): $180
- Extension Cords (4x 25ft): $120
- Power Strips (3x): $150
- Power Distribution: $100
- Soft LED Overhead Lighting: $6,000
- C-Stands (3x Impact): $510 (B&H Photo)
- HDMI Cables & Other Accessories: $200
- SSD Storage (Samsung T7 1TB): $100
- Cloudlifters (4x): $600 (needed without separate preamp)
- AutoPod License: $29/month
- **Benefit:** Automatic audio following video, saves 15+ min/episode
- **Note:** No headphone amplifier needed (built into ATEM)

### Ongoing Costs (Both Options)
- AutoPod: $29/month
- Adobe Creative Cloud: $55/month
- SSD storage as needed
- Companion software: Free (Option 1 only)

---

## Tips for Efficiency

1. **Template Everything**
   - Premiere project templates
   - After Effects MOGRT templates
   - Folder structure templates
   - Export preset templates

2. **Consistent Naming**
   - YYYY-MM-DD_PodcastName_GuestName
   - Keep file names short but descriptive
   - Use same naming across all assets

3. **Backup Strategy**
   - Record to SSD and computer simultaneously
   - Audio backup on SD card
   - Cloud backup of final exports

4. **Quality Control**
   - Quick review of AutoPod edits
   - Check audio levels consistency
   - Verify graphics/titles accuracy
   - Test exports on target platforms

---

## Next Steps

1. **Finalize Camera Selection**
   - Test different models if possible
   - Ensure clean HDMI output
   - Check low-light performance

2. **Room Preparation**
   - Acoustic treatment
   - Lighting setup
   - Cable management
   - Dedicated edit station

3. **Test Workflow**
   - Do practice recordings
   - Time each step
   - Identify bottlenecks
   - Refine templates

---

## Recommendation Summary

### For Most Podcasters: Start with Option 1
- Begin with ATEM Mini Pro ISO + PodTrak P8 + Companion automation
- Test the workflow and identify pain points
- Upgrade to Option 2 if AFV becomes critical
- Lower initial investment with room to grow

### For Professional/Daily Production: Go with Option 2
- ATEM Television Studio HD8 ISO from the start
- Time saved in post-production pays for itself
- True broadcast quality from day one
- Scalable for future growth

### The AFV Difference
**Without AFV (Option 1):**
- Switch to Camera B → Same audio mix continues
- Fix audio levels in post-production
- Extra 10-15 minutes per episode

**With AFV (Option 2):**
- Switch to Camera B → Mic B automatically prominent
- Other mics automatically duck
- Ready to publish with minimal post work

For a daily podcast, those extra 15 minutes add up to 5+ hours per month of additional editing time.

---

*Document created: January 2025*
*Last updated: January 2025*