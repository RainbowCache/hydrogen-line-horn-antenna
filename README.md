# hydrogen-line-horn-antenna

I'm making a hydrogen line horn antenna. Work in progress.

## Overview

This project contains design files and simulation tools for a horn antenna tuned to detect the 21 cm hydrogen line at 1.42 GHz, used in radio astronomy.

## Getting Started

I ended up creating an Ubuntu virtual machine and building / installing openEMS 
into /opt/openEMS. The openEMS install process also includes creating
a /opt/openEMS/venv directory which is the virtual environment I use for this python 
project. I had to install ipykernel in the virtual environment as well:

```bash
pip install scipy
pip install ipykernel
```

Back in Visual Studio Code, in the project directory, I just ran the following to create 
a symbolic link to the system's OpenEMS virtual environment directory:

```bash
ln -s /opt/openEMS/venv .venv
```

In Visual Studio, I created a python environment as usual under .venv. It detects that 
the directory is there and uses the openEMS virtual environment instead.

### Prerequisites

1. **Python 3.8+** with pip
2. **OpenEMS** - Open Electromagnetic Field Solver
   - Installation instructions: https://docs.openems.de/install.html
   - OpenEMS-Project repository: https://github.com/thliebig/openEMS-Project

### Installation

1. Clone this repository:
   ```bash
   git clone https://github.com/RainbowCache/hydrogen-line-horn-antenna.git
   cd hydrogen-line-horn-antenna
   ```

2. Install Python dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Launch Jupyter notebook:
   ```bash
   jupyter notebook horn_antenna_design.ipynb
   ```

## Jupyter Notebook

The `horn_antenna_design.ipynb` notebook provides:
- Horn antenna design parameters for 1.42 GHz
- OpenEMS simulation setup
- Geometry visualization
- Theoretical performance calculations
- Step-by-step guide for electromagnetic simulation

### Features

- **Design Parameters**: Pre-configured for the hydrogen line frequency (1420.405 MHz)
- **Geometry Visualization**: 2D plots of horn antenna profile
- **OpenEMS Integration**: Ready-to-use setup for electromagnetic simulation
- **Performance Estimates**: Theoretical gain, beamwidth, and directivity calculations

## Usage

Open the Jupyter notebook and run the cells sequentially. The notebook will:
1. Verify that required packages are installed
2. Set up design parameters for 1.42 GHz
3. Visualize the horn antenna geometry
4. Configure OpenEMS simulation (if installed)
5. Provide theoretical performance estimates

## Project Structure

```
hydrogen-line-horn-antenna/
├── README.md                    # This file
├── requirements.txt             # Python dependencies
└── horn_antenna_design.ipynb   # Main design notebook
```

## Resources

- [OpenEMS Documentation](https://docs.openems.de/)
- [Society of Amateur Radio Astronomers](https://www.radio-astronomy.org/)
- [Hydrogen Line Information](https://en.wikipedia.org/wiki/Hydrogen_line)

## License

See LICENSE file for details.
