
# NFS BlackBox Blender Tools

A set of Blender tools designed for the **Need for Speed BlackBox modding pipeline**.

These tools simplify two common tasks used when preparing vehicles for BlackBox engine games:

- Vinyl UV Mapping
- Bulk Part Renaming

Supported games include:

- Need for Speed Underground
- Need for Speed Underground 2
- Need for Speed Most Wanted
- Need for Speed Carbon
- Need for Speed ProStreet
- Need for Speed Undercover
- Need for Speed World

---

# Features

## 1. Vinyl UV Mapping Tool

The **Vinyl Unwrapper** automates the classic BlackBox vinyl mapping workflow.

It allows artists to quickly project UVs from orthographic views and place them inside the correct vinyl template zones used by NFS games.

### Main capabilities

- Automatic UV projection from view
- Supports five vinyl zones:
  - LEFT
  - RIGHT
  - TOP
  - FRONT
  - REAR
- Works with:
  - Separate objects
  - Joined meshes with material regions
- UV zone overlay inside the UV editor
- Editable zone bounds
- Optional template grid limits for UG/MW
- UV scaling option
- UV preset system
- Fully automated legacy unwrap sequence

### Automatic UV Mapping

The addon can run the complete mapping sequence automatically:

LEFT → TOP → RIGHT → FRONT → REAR

This reproduces the classic workflow used when mapping vinyl templates for BlackBox engine games.

### UV Zone Overlay

The tool can display colored UV zones inside the UV Editor to visualize where each part of the car should be mapped.

### UV Presets

Users can save and load custom UV layouts.

Presets store:

- UV zone bounds
- scaling settings

Preset files are saved as JSON files.

---

## 2. Bulk Part Renaming Tool

The **Bulk Rename** tool renames selected objects using naming conventions required by the BlackBox engine.

Supported naming formats include:

BASE_A
KIT00_SPOILER_A
KIT00_BODY_A

### Features

- Automatic sequential naming
- Optional custom prefix
- Live rename preview
- Renames both object and mesh data names

Example result:

KIT00_SPOILER_A
STYLE01_SPOILER_A
STYLE02_SPOILER_A
STYLE03_SPOILER_A

Special handling exists for BODY kits:

KIT00_BODY_A
KIT01_BODY_A
KIT02_BODY_A
KIT03_BODY_A

This ensures compatibility with NFS modding pipelines.

---

# Installation

Installation is extremely simple.

## Drag & Drop Installation (Recommended)

1. Open Blender
2. Drag the addon ZIP file directly into the **3D Viewport**
3. Blender will automatically install and enable the addon

---

## Install via Preferences

1. Open **Edit → Preferences**
2. Go to **Add-ons**
3. Click **Install**
4. Select the addon ZIP file
5. Enable the addon

---

# Location in Blender

After installation the tools appear in the **3D View Sidebar**.

Press:

N

Open the tab:

NFS BB TOOLS

You will find:

- NFS BB Vinyl Unwrapper
- NFS BB Bulk Part Naming

---

# Vinyl Mapping Workflow

Typical workflow:

### 1. Create Vinyl Materials

Press:

Create Vinyl Materials

This generates the required materials:

LEFT
RIGHT
TOP
FRONT
REAR

### 2. Assign Materials

Assign each material to the appropriate faces of the vehicle mesh.

Example:

LEFT → left side panels  
RIGHT → right side panels  
TOP → roof / hood  
FRONT → front bumper  
REAR → rear bumper  

### 3. Run Auto UV Mapping

Press:

Auto UV Mapping

The addon will automatically:

1. switch views
2. project UVs
3. move UVs into correct vinyl zones

---

# Supported Layout Types

Different NFS games use different vinyl layouts.

Legacy layout:

UG
MW

Modern layout:

CB
PS
UC
WORLD

Each tab loads the correct default zone configuration.

---

# Advanced Controls

Users can enable **UV Zone Controls** to manually edit zone boundaries.

Editable properties include:

Left  
Right  
Top  
Bottom  

for every vinyl zone.

---

# Requirements

Blender version:

Blender 3.0 or newer

Tested with:

Blender 3.x  
Blender 4.x

---

# Author

Cipher

---

# License

This project is released under the MIT License.
