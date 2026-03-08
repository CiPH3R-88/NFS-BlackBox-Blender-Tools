# NFS BlackBox Blender Tools

A Blender toolkit designed for the **Need for Speed BlackBox modding
pipeline**.

This addon provides tools that simplify two common workflows used when
preparing vehicles for BlackBox engine games:

-   Vinyl UV Mapping
-   Bulk Part Renaming

Supported games include:

-   Need for Speed Underground
-   Need for Speed Underground 2
-   Need for Speed Most Wanted
-   Need for Speed Carbon
-   Need for Speed ProStreet
-   Need for Speed Undercover
-   Need for Speed World

------------------------------------------------------------------------

# Features

## 1. Vinyl UV Mapping Tool

The **Vinyl Unwrapper** automates the classic BlackBox vinyl mapping
workflow.

It allows artists to quickly project UVs from orthographic views and
place them into the correct vinyl template zones used by NFS games.

### Main Capabilities

-   Automatic UV projection from view
-   Supports five vinyl zones:
    -   LEFT
    -   RIGHT
    -   TOP
    -   FRONT
    -   REAR
-   Works with:
    -   Separate objects
    -   Joined meshes with material regions
-   UV zone overlay inside the UV Editor
-   Editable UV zone bounds
-   Optional template grid limits for UG / MW layouts
-   UV scaling option
-   UV preset system
-   Fully automated legacy unwrap sequence

### Automatic UV Mapping

The addon can run the complete mapping sequence automatically:

LEFT → TOP → RIGHT → FRONT → REAR

This reproduces the classic workflow used when mapping vinyl templates
for BlackBox engine games.

### UV Zone Overlay

The tool can display colored UV zones inside the **UV Editor**, allowing
artists to visually place each section of the car inside the correct
template area.

### UV Presets

Users can save and load custom UV layouts.

Presets store:

-   UV zone bounds
-   scaling settings

Preset files are stored as **JSON files**.

------------------------------------------------------------------------

# 2. Bulk Part Renaming Tool

The **NFS BlackBox Part Naming** tool automates renaming vehicle parts
according to the naming rules used in BlackBox engine games.

It applies correct naming logic for:

-   BASE parts
-   KIT00 parts
-   STYLE variants (or custom prefix variants)
-   Special BODY kit numbering

The tool renames both:

-   Object Name
-   Object Data (Mesh) Name

This ensures **export-safe naming and prevents .001 duplication
issues**.

------------------------------------------------------------------------

## Bulk Rename Features

-   Automatic uppercase enforcement
-   Live preview before applying
-   Special KIT00_BODY_A numbering rule
-   Default STYLE## prefix generation
-   Optional custom prefix support (example: NFS##, CARNAME##)
-   Strict naming validation
-   Selected object count display
-   Undo support
-   Automatically clears First Object Name after applying
-   Renames object and mesh data together

------------------------------------------------------------------------

## Supported Naming Formats

BASE_A\
KIT00_SPOILER_A\
KIT00_BODY_A

Example output:

KIT00_SPOILER_A\
STYLE01_SPOILER_A\
STYLE02_SPOILER_A\
STYLE03_SPOILER_A

Special rule for BODY kits:

KIT00_BODY_A\
KIT01_BODY_A\
KIT02_BODY_A\
KIT03_BODY_A

------------------------------------------------------------------------

# Installation

Installation is extremely simple.

## Drag & Drop Installation (Recommended)

1.  Open Blender\
2.  Drag the addon ZIP file directly into the **3D Viewport**\
3.  Blender will automatically install and enable the addon

------------------------------------------------------------------------

## Install via Preferences

1.  Open **Edit → Preferences**\
2.  Go to **Add-ons**\
3.  Click **Install**\
4.  Select the addon ZIP file\
5.  Enable the addon

------------------------------------------------------------------------

# Location in Blender

After installation the tools appear in the **3D View Sidebar**.

Press:

N

Open the tab:

NFS BB TOOLS

You will find:

-   NFS BB Vinyl Unwrapper
-   NFS BB Bulk Part Naming

------------------------------------------------------------------------
Note: The car model must always face the +X axis. Ensure all car parts are properly assembled and the object origin is set to the 3D Cursor.

# Vinyl Mapping Workflow

Typical workflow:

### 1. Create Vinyl Materials

Press:

Create Vinyl Materials

This generates the required materials:

LEFT\
RIGHT\
TOP\
FRONT\
REAR

------------------------------------------------------------------------

### 2. Assign Materials

Assign each material to the correct faces of the vehicle mesh.

Example:

LEFT → left side panels\
RIGHT → right side panels\
TOP → roof / hood\
FRONT → front bumper\
REAR → rear bumper

------------------------------------------------------------------------

### 3. Run Auto UV Mapping

Press:

Auto UV Mapping

The addon will automatically:

1.  Switch views\
2.  Project UVs\
3.  Move UV islands into correct vinyl zones

------------------------------------------------------------------------

# Bulk Rename Workflow

1.  Place all parts inside a collection.

2.  Select the parts:

Click the first object then:

Shift + Click the last object

3.  Press **N** to open the Sidebar.

4.  Go to:

NFS BB Bulk Rename

5.  Enter the exact name of the first object.

The name must start with:

BASE\
or\
KIT00\_

6.  Optional settings:

-   Enable **Preview Names** to see results before applying
-   Enable **Custom Prefix** to replace STYLE

7.  Click **Apply Rename**.

After a successful rename the **First Object Name field automatically
clears**.

------------------------------------------------------------------------

# Important Rules

-   At least **2 objects must be selected**
-   The **first selected object must match the input name**
-   The input must start with:

BASE\
or\
KIT00\_

-   Custom prefix **cannot be empty** when enabled

------------------------------------------------------------------------

# Supported Layout Types

UG1 / UG2 / MW / CB / PS / UC / WORLD

Each tab loads the correct default UV zone configuration.

------------------------------------------------------------------------

# Requirements

Blender 3.0 or newer

Tested with Blender 3.x and Blender 4.x

------------------------------------------------------------------------

# Author

Cipher

------------------------------------------------------------------------

# License

This project is released under the **MIT License**.
