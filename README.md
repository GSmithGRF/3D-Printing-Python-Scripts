# 3D Printing Utilities

This repository hosts a collection of Python scripts designed to assist 3D printing enthusiasts in preparing, analyzing, and optimizing models for slicers like OrcaSlicer. The tools focus on automating common tasks, providing actionable guidance, and improving print success rates by evaluating model orientation, overhangs, and bed adhesion before printing. Each script is self-contained and can be run directly from the command line or from an IDE such as IntelliJ.

---

## Features

* **STL Analysis:** Load and parse both ASCII and binary STL files.
* **Orientation Optimization:** Suggest ideal print orientations using heuristic scoring based on overhangs, footprint, and print height. Includes grid-based, random, and PCA-aligned candidates.
* **Quick Instructions:** Generate human-readable, step-by-step guides for model placement, rotation, support settings, and bed adhesion in OrcaSlicer.
* **IntelliJ-Friendly Workflow:** Automatically locate STL files on your computer or removable drives when run without command-line arguments.
* **Flexible Configuration:** Customize build volume, clearance, overhang thresholds, and alternative orientation outputs.

---

## Installation

1. Clone the repository:

```bash
git clone https://github.com/yourusername/3d-printing-utilities.git
cd 3d-printing-utilities
```

2. Ensure Python 3.9+ and NumPy are installed:

```bash
pip install numpy
```

---

## Usage

### Command-Line Interface

```bash
python stl_orcaslicer_advisor.py path/to/model.stl --pca --overhang 45
```

* **`--pca`**: Include PCA-based orientation candidate.
* **`--overhang`**: Set the overhang threshold in degrees.
* Additional options: build volume, clearance, random rotation samples, and number of alternative orientations.

### IntelliJ Quick-Run

1. Set the `STL_NAME` variable at the bottom of the script.
2. Leave run arguments empty.
3. Run the script; it will locate the STL automatically and provide instructions.

---

## Example Output

The script outputs a structured, sectioned guide including:

* File information and model size
* Recommended orientation with rotation angles or PCA alignment
* Instructions for centering, dropping to bed, and confirming fit
* Support and adhesion guidance
* Basic print quality settings and final checks
* Alternative orientation suggestions

---

## Contributing

Contributions are welcome! You can submit feature requests, bug reports, or pull requests for:

* Additional orientation heuristics
* Integration with other slicers
* Advanced support analysis
* Enhanced visualization of suggested orientations

---

## License

This project is released under the MIT License.

---

This README provides users with a clear understanding of the purpose of the scripts, installation instructions, usage patterns, and guidance for contributions.

If you want, I can also draft a **visual workflow diagram** showing how the STL analysis and orientation scoring works, which could be included in the README to make it more approachable for new users.
