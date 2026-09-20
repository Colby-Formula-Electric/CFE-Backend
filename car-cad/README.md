# Colby Formula Student Electric — Car CAD

Central repository for the team's vehicle CAD, assemblies, manufacturing files, and released design revisions.

This repository serves as the **source of vehicle CAD**. All members should follow the organization and version-control conventions below to keep the car's design history maintainable across team generations.

---

## Repository Structure

```text
car-cad/
│
├── 26-27/
│   ├── 00_Master_Assembly/
│   ├── 01_Chassis/
│   ├── 02_Suspension/
│   ├── 03_Steering/
│   ├── 04_Brakes/
│   ├── 05_Powertrain/
│   ├── 06_Accumulator/
│   ├── 07_Electronics/
│   ├── 08_Aero/
│   ├── 09_Bodywork/
│   └── 10_Manufacturing/
│
├── new-year-template/
│   ├── 00_Master_Assembly/
│   ├── 01_Chassis/
│   ├── 02_Suspension/
│   ├── 03_Steering/
│   ├── 04_Brakes/
│   ├── 05_Powertrain/
│   ├── 06_Accumulator/
│   ├── 07_Electronics/
│   ├── 08_Aero/
│   ├── 09_Bodywork/
│   └── 10_Manufacturing/
|
├── shared/
│   ├── fasteners/
│   ├── bearings/
│   ├── purchased_Components/
│   └── hardware/
│
├── released/
|
└── README.md
```

### Year-by-year Directories

| Directory            | Contents                                                 |
| -------------------- | -------------------------------------------------------- |
| `00_Master_Assembly` | Complete vehicle assemblies and top-level CAD            |
| `01_Chassis`         | Frame, mounts, brackets, structural components           |
| `02_Suspension`      | Uprights, control arms, rockers, dampers, etc.           |
| `03_Steering`        | Steering rack, column, steering wheel, linkages          |
| `04_Brakes`          | Pedal box, calipers, rotors, brake mounts                |
| `05_Powertrain`      | Motors, motor mounts, drivetrain components              |
| `06_Accumulator`     | Accumulator enclosure, mounting, cooling, HV components  |
| `07_Electronics`     | Electronics enclosures, mounts, sensors, wiring hardware |
| `08_Aero`            | Wings, endplates, mounts, aerodynamic structures         |
| `09_Bodywork`        | Body panels, covers, driver interface components         |
| `10_Manufacturing`   | Manufacturing-specific files, drawings, jigs, fixtures   |

---

## Branching

The `main` branch represents the **current stable vehicle design**.

For changes, create a feature branch:

```text
feature/front-upright-revision
feature/rear-wing-mount
feature/accumulator-enclosure
```

Do not make experimental or incomplete changes directly on `main`

The `main` should only be edited or changed by team leads

## Commit Messages

Commit messages should clearly describe the engineering change.

### Good

```text
Suspension: revise front upright mounting geometry
Chassis: add motor mount reinforcement
Aero: update front wing endplate
Accumulator: revise enclosure mounting tabs
Manufacturing: add CNC drawing for rear upright
```

### Avoid

```text
update
changes
stuff
fixed
new cad
asdf
```

Please sign each commit with your name, keep messages concise but encompass all changes or additions you have made, more is better than less.

---

## Released Designs

The `Released/` directory contains CAD that has been formally released for a specific purpose.

Examples:

```text
Released/
├── 2027-design-freeze/
└── 2027-competition-configuration/
```

Released files should **not be modified**.

If a released component needs to change, create a new revision rather than modifying the old released version in place.

---

## CAD Revision Philosophy

CAD should be treated as an engineering record, not simply a collection of files.

When making a substantial design change:

1. Create a branch.
2. Make the CAD changes.
3. Verify assembly references.
4. Check for interference/errors.
5. Update associated drawings.
6. Update the BOM if necessary.
7. Have the relevant subsystem member review the change.
8. Have a team lead merge into `main`.

---

## Purchased Components

Purchased components should be stored in:

```text
Shared/Purchased_Components/
```

Where possible, retain the manufacturer's original CAD file without modifying it.

Use descriptive names:

```text
SKF_6005_2RS.SLDPRT
Brembo_Caliper_ModelX.STEP
Motor_Model_ABC.STEP
```

If a purchased component is modified for integration, save the modified version separately and clearly identify it as such.


---

## Folder Naming

Folder names should be all lowercase, with spaces replaced with `-`:

```text
26-27
04-brakes
new-year-template
```

## File Naming

Use descriptive, consistent names. Replace spaces with `_` and capitalize. **Do not delete prior file versions** - instead add `_v#` to your file name (see below for examples)

### Preferred

```text
Front_Upright_v8.SLDPRT
Front_Control_Arm_Upper.SLDPRT
Motor_Mount_Left_v2.SLDPRT
Accumulator_Enclosure_v7.SLDASM
Rear_Wing_Mainplane.SLDPRT
```

### Avoid

```text
Part1.SLDPRT
NewPart.SLDPRT
Final.SLDPRT
Final_Final.SLDPRT
New_Upright_2_REAL_FINAL.SLDPRT
```

Avoid using names such as `FINAL`, `NEW`, or `LATEST` to indicate revisions. Git history and releases should handle versioning.

---

## Do Not Commit

Do not commit:

* Temporary exports
* Personal notes
* Duplicate CAD files
* Screenshots unless specifically required
* Local software cache files
* Autosave/recovery files
* Unnecessary rendered images
* Credentials or API keys
* Personal files

Use `.gitignore` for software-specific temporary files.

---

## Design Philosophy

The purpose of this repository is not simply to store CAD.

It should preserve the team's **engineering history**.

A future team member should be able to answer:

* What did the car look like?
* Why was a component changed?
* Who reviewed the change?
* Which version was manufactured?
* Which CAD revision corresponds to a physical part?
* What was the competition configuration?
* What designs were eventually abandoned?

When in doubt, favor **traceability and clarity** over convenience.

---

## Competition Configuration

Before competition, create a clearly identified snapshot of the vehicle's final configuration.

Example:

```text
Released/
└── 2027_Competition_Configuration/
    ├── Master_Assembly/
    ├── Manufacturing/
    ├── Drawings/
    └── BOM/
```

This represents the CAD configuration corresponding to the physical vehicle submitted for competition.

---

## For New Team Members

Before modifying vehicle CAD:

1. Read this README.
2. Learn the team's CAD software workflow.
3. Identify the subsystem you are working on.
4. Pull the latest version of the repository.
5. Make changes on a feature branch.
6. Do not overwrite another member's work.
7. Ask the subsystem lead if you are unsure about a design decision.
8. Keep assemblies and references intact.
9. Document significant engineering changes.
10. Make your commits understandable to someone who was not involved in the work.

**Build the car. Preserve the knowledge.**
