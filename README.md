# AI Bento Plating Robot 3D — Six Compartments

## Overview

MuJoCo-based 3D robotic bento plating system.

Features:
- Six-compartment bento box (2 × 3)
- Normal-size and oversized food items
- CNN food classification
- RGB-D food size estimation
- Image-based food center localization
- Three-finger robotic claw
- Baseline vs AI comparison
- Japanese-narrated 120-second video

## Main files

- `scene_3d.py` — MuJoCo scene and robot
- `vision_model.py` — CNN and RGB-D vision
- `run_project.py` — Training and evaluation
- `make_video.py` — Video and narration
- `make_report.py` — PDF report

## Reproduction

Install dependencies using `requirements.txt`, then run:

```bash
python run_project.py --out results_bento6_vision --train-n 500 --val-n 125 --epochs 10 --scenes 4 --seed 31031
```


## Evaluation results

- Scenes: 4
- Baseline success rate: 33.3%
- CNN without size judgment: 63.9%
- Proposed AI success rate: 86.1%
- Oracle reference: 100.0%
- Oversize rejection recall: 100.0%

Results are from the simulation described in `results/summary.json`.


## Limitations

The robot uses a simplified kinematic grasp constraint.
Image localization uses known supply-cell regions.
The system has been evaluated in simulation, not on a real robot.

## Demo

Add the public YouTube video URL here.
