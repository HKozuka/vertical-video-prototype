# Vertical Video Cropping Prototype

AI-powered conversion of horizontal movie scenes to vertical format for mobile viewing.

## Overview

Built a working prototype that uses face detection to intelligently crop 16:9 movies to 9:16 vertical format, optimized for mobile screens where users hold phones vertically.

**Key stat:** Vertical videos have 90% higher completion rates on mobile than horizontal videos (Snapchat, 2023)

## Results

- **Face detection rate:** 89.3% (1,164 of 1,304 frames)
- **Subject retention:** 97.8% (actor stayed in frame)
- **Processing speed:** ~30 FPS on CPU
- **Output quality:** 1080x1920 vertical format

## Technical Approach

**Model:** OpenCV Haar Cascade (Viola-Jones algorithm)
- Pre-trained face detection, no training data required
- 38-stage cascade with ~2,500 decision trees
- Industry standard for 20+ years (cameras, smartphones)
- Optimal balance: fast (CPU-only) + accurate enough for MVP


## Key Learning

Face detection works reliably for dialogue scenes. For production, recommend hybrid approach: automated ML for simple scenes + editorial review for complex shots. Validate user demand first, then refine algorithm.


- **`vertical_video_prototype.ipynb`** - Full implementation with code, analysis, and results

---
