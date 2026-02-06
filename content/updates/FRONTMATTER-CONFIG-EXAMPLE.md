---
# ===========================================
# Updates Frontmatter Configuration Example
# ===========================================

# Required Fields
# ==========================================
title: "Your Article Title" # Title displayed on cards and article pages
date: 2025-10-12 # Date format: YYYY-MM-DD or YYYY-MM-DDTHH:MM:SS-TZ
draft: true # True = drafts are not displayed, false = published versions are displayed

# Optional Field - Background Image
# ========================================
# If not set, the system will prioritize the following:
# 1. Use the first image in the article
# 2. If no image is available, a random image will be assigned from /images/updates-random/ (fixed for each article)

featured_image: "/images/your-image.jpg" # Custom background image path

# Optional Field - Summary Text
# =========================================
# If not set, the first 200 words will be automatically extracted from the article content.

summary: "Enter a custom summary here. This will be displayed on the list page card. You can write a more concise introduction than the automatic one. Displays up to 3 lines (2 lines on mobile devices)."

# Optional Field - Visual Style
# ========================================
overlay_color: "rgba(0, 0, 0, 0.5)" # Overlay color, default: rgba(0,0,0,0.4)
# Use a light overlay for dark images, a dark overlay for light images

text_color: "#ffffff" # Text color, default: white
# For light backgrounds, use "#333333"

button_text: "View Details" # Button text, default: "Read More"

button_style: "border-color: #943929; background: rgba(148, 57, 41, 0.2);"
# Custom button styles (CSS), can change color, background, etc.

# Preset combination suggestions
# ========================================
#
# Dark background image (recommended):
# overlay_color: "rgba(0, 0, 0, 0.4)"
# text_color: "#ffffff"
#
# Light background image:
# overlay_color: "rgba(255, 255, 255, 0.7)"
# text_color: "#333333"
# button_style: "border-color: #333; color: #333;"
#
# Accent button (red):
# button_style: "border-color: #943929; background: rgba(148, 57, 41, 0.2);"
#
# Accent button (blue):
# button_style: "border-color: #2563eb; background: rgba(37, 99, 235, 0.2);"

---

## This is the article body

Your article content starts here...

### Example title

If the article contains images and `featured_image` is not set, the first image will automatically be used as the background for the list page:

![Sample image](/images/your-image.jpg)

More...

## Complete example

### Minimal configuration (recommended)
```yaml
---
title: "My Update"
date: 2025-10-12
draft: false
---
```
The system automatically handles background images and snippets.

### Fully Customizable Configuration
```yaml
---
title: "Major Update: Rocket Launch Successful"
date: 2025-10-15
draft: false
featured_image: "/images/rocket-launch.jpg"
summary: "We successfully completed our first rocket test launch, reaching the target altitude of 10 kilometers. This marks the beginning of a new phase for the project."
overlay_color: "rgba(0, 0, 0, 0.5)"
text_color: "#ffffff"
button_text: "View Details"
button_style: "border-color: #943929; background: rgba(148, 57, 41, 0.2);"
---
```

## Technical Description

### Background Image Selection Logic
1. **Priority 1**: `featured_image` field
2. **Priority 2**: The first `<img>` image in the article Tags Images
3. **Priority 3**: Randomly assigned from `/images/updates-random/` (based on the article path hash, fixed)

### Random Image Pool
Currently 6 space images:
- GSFC_20171208_Archive_e000842~large.jpg (Earth)
- PIA26077~orig.jpg (Mars)
- S84-27031~large.jpg (Space Capsule)
- carina_nebula~orig.png (Nebula)
- iss064e041512~large.jpg (International Space Station)
- iss073e0659744~large.jpg (Earth at night)

### Style Restrictions
- **Title**: Automatically sized, mobile responsive
- **Abstract**: Maximum 3 lines on desktop, 2 lines on mobile, hidden if exceeding
- **Button**: Fixed style, color can be customized using `button_style`
- **Content area**: Maximum width 600px, left-aligned, 8% left margin