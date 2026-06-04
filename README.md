# Colby Formula Electric Database

Central repository for Colby College's Formula Electric team documentation, design notes, and subsystem data.

## Overview

This repository helps the team keep engineering information organized and easy to find across seasons. It is structured by subsystem so members can quickly access relevant resources for design, testing, and build decisions.

Current focus areas:
- Electrical systems
- Structural systems

## Repository Structure

```text
CFE-Database/
|- Electrical/
|- Structural/
`- README.md
```

## Purpose

Use this repository to:
- Track subsystem-level technical references and design rationale
- Store standards, procedures, and calculation templates
- Store project files and documentation in a predictable structure
- Document testing results and lessons learned
- Maintain continuity between graduating and incoming team members

## Getting Started

1. Clone the repository.
2. Create or open files in the appropriate subsystem folder.
3. Use clear file names with dates when relevant.
4. Commit changes with a concise, descriptive message.

## Naming and Organization Conventions

### Folder Organization

- Top-level folders are team subsystems: `Electrical` and `Structural`.
- Each subsystem contains subsection folders (for example: `Chassis`, `Suspension`, `Battery Management`).
- Each subsection folder should include:
	- Technical files for that subsection
	- A local `README.md` with an entry for each file with: Author, Date and File details

### Folder Naming

- Use Title Case for folders.
- Use spaces only when needed.
- Examples: `Chassis`, `Suspension`, `Battery Management`

### File Naming

- Use lowercase and underscores for file names.
- Recommended format:

```text
subsection_author_yyyy_mm_dd.ext
```

- Example:

```text
battery_management_kevin_gustafson_2026_03_12.csv
```

- Every folder-level documentation file should be named exactly:

```text
README.md
```

### Commit Message Convention

- Format:

```text
Subsystem/Subsection: short action summary
```

- Examples:

```text
Electrical/Battery Management: add BMS fault log template
Structural/Chassis: update weld inspection checklist
```

## Contribution Guidelines

When committing a file to a subsection, be sure to add the relevant metadata to the subsections README, as detailed in Folder Organization

- Keep files subsystem-specific when possible.
- Add short context at the top of technical notes:
	- Author
	- Date
	- Version
	- Status (Draft, Review, Approved)
- Avoid deleting historical data unless it is duplicated or incorrect.

## Data Quality Standards

- Include units in all calculations and tables.
- Cite assumptions and references for major decisions.
- For test data, include setup details and pass/fail criteria.
- For design updates, briefly state what changed and why.

## Academic and Team Use

This repository is intended for educational and team engineering use at Colby College. Follow campus safety and lab policies when documenting manufacturing, battery, and high-voltage procedures.

## Credits

- Colby College Formula Electric Team members and leadership
- Faculty advisors and lab staff supporting team operations
- Student contributors maintaining subsystem documentation and data quality

## Contact

For access, structure changes, or onboarding questions, contact the current Colby Formula Electric team leadership at cfe@colby.edu.
