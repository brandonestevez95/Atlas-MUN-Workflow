# 🌐 Model UN GIS Mapping Workflow — Full SOP

Version 1.0 | Maintained by Brandon Estevez | Last updated October 2025

This workflow standardizes how GIS is integrated into Model United Nations conferences. It provides a repeatable, scalable pipeline for producing committee-specific interactive maps and StoryMaps that enhance delegate research, debate, and resolution drafting. It is designed for use with ArcGIS Online (AGOL), StoryMaps, and Instant Apps.

---

## 1. 📛 Standardized Naming & Tagging Conventions

A clean naming structure is the backbone of this system. Every map, app, and StoryMap must follow the same convention so future team members can quickly find, update, or replicate your work.

### 1.1 Map Naming Convention

Format:



Example:



- **ConferenceName**: e.g., CAPSMUN, NHSMUN, RALMUN
- **CommitteeAcronym**: e.g., SC, GA, HRC, ECOSOC
- **MapYear**: the calendar year of the conference

### 1.2 Required Tags

Each map and app must include the following tags:
- **Conference Name**: e.g., CAPSMUN
- **AuthorLastNameYear**: e.g., Estevez2025
- **Committee Acronym**: e.g., SC

Optional but encouraged tags:
- **Topic keywords**: e.g., migration, climate, energy
- **Map type**: choropleth, points, dashboard
- **Conference year**: 2025

Why this matters:
- Makes future conferences plug-and-play.
- Enables bulk cleanup and searching in AGOL.
- Prevents lost or duplicated work between committees.

---

## 2. 🧠 Layer Discovery and Map Assembly

This is the most time-intensive phase. The goal is to cast a wide net, then narrow strategically.

### 2.1 Topic Analysis

For each committee topic (e.g., GA Topic A, SC Topic B):
1. **AI-Assisted Search**: Use ChatGPT to query ArcGIS Living Atlas and AGOL for relevant datasets. Include global and thematic keywords, such as refugee