# Atlas MUN Workflow — Master SOP (v1.0)

**Authors:** [Brandon Estevez](https://www.linkedin.com/in/YOUR_LINKEDIN) · [Bernard Roach](https://www.linkedin.com/in/BERNIE_LINKEDIN)  
**Repository:** [Atlas MUN Workflows](https://github.com/brandonestevez95/Atlas-MUN-Workflow)  
**License:** [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/)  

---

## 0. Purpose & Scope

Atlas is a standardized **GIS + StoryMaps workflow** that integrates spatial intelligence into Model United Nations (MUN) conferences. It establishes a **replicable, scalable pipeline** for producing committee maps using **ArcGIS Online (Map Viewer)**, configuring them as **Instant Apps (Sidebar)**, and embedding them in a centralized **StoryMaps Collection**.

This document outlines the *core Atlas workflow* — the public-facing procedure used to ensure professional-quality GIS integration at MUN events such as CAPSMUN. Internal acceleration materials (custom datasets, scripts, and timing playbooks) are proprietary and excluded.

---

## 1. Core Principles

- **Standardization:** Every map follows the same naming, tagging, and design structure.  
- **Replicability:** Any trained GIS or Secretariat team can reproduce the workflow.  
- **Scalability:** Supports 1–20+ committees with consistent performance.  
- **Usability:** Delegates can intuitively explore maps without GIS training.  
- **Attribution:** Data sources (Esri, Living Atlas, 4-H) are transparently credited.  
- **Accessibility:** Built-in translation (Spanish minimum) and readable symbology.

---

## 2. Naming & Tagging Conventions

### 2.1 File Naming
**Format:**

ConferenceName-CommitteeAcronym-MapYear

**Example:**

CAPSMUN-SC-Map2025

### 2.2 Tag Structure
Each ArcGIS item (map, app, or StoryMap) must include:
- `ConferenceName` → e.g., `CAPSMUN`
- `AuthorLastNameYear` → e.g., `Estevez2025`
- `CommitteeAcronym` → e.g., `SC`

**Optional Tags:** `TopicA`, `TopicB`, keywords (`climate`, `migration`), `InstantApp`, `StoryMaps`.

> **Purpose:** Consistent naming allows for easy search, maintenance, and annual scaling.

---

## 3. Committee Setup & Topic Intake

1. **Gather Committee Topics** — Obtain Topic A and Topic B from each delegate guide.  
   Example:  
   - Topic A: “Cybersecurity in Critical Infrastructure”  
   - Topic B: “Nuclear Nonproliferation”  

2. **One Master Map per Committee** — Both topics are represented as thematic groups within one map.

3. **Country Filtering** —  
   Begin with *Living Atlas – World Countries*. Apply filters for participating nations only.  
   Example Filter:  

COUNTRY IN (‘Argentina’,‘Australia’,‘Brazil’,‘France’,‘India’,‘United States’)

---

## 4. Data Layer Workflow

### 4.1 Discovery Phase
Cast a wide net to identify relevant data.

- **AI Search Prompts:**  
Example queries for ChatGPT or Esri Assistant:  
- “Find ArcGIS Living Atlas layers on global food insecurity (post-2015).”  
- “Search AGOL for global carbon emission datasets with public access.”  

- **Manual Search:**  
Explore ArcGIS Living Atlas and AGOL manually for under-tagged or regional datasets.

**Log findings** in a `Layer_Index.csv`:

committee,topic,layer_name,provider,url,license,geometry,notes,keep/discard

### 4.2 Curation Phase
Refine the dataset collection.

- Select **5–10 layers per topic** for clarity.  
- Prioritize **credible sources**: UN, World Bank, WHO, Esri, NOAA, FAO.  
- Remove overlapping or redundant layers.  
- Test visibility and symbology at multiple zoom levels.

### 4.3 Styling & Symbology
- Use sequential or diverging color ramps with 4–6 classes.  
- Keep legends concise and intuitive.  
- Apply neutral, professional colors — avoid red/green-only ramps.  
- Use **Light Gray Canvas** or **Modern Indigo** basemap for contrast.  

**Pop-ups:**  
Include meaningful info (country, metric, year, data source). Remove technical fields (e.g., OBJECTID).

---

## 5. Instant App (Sidebar) Configuration

### 5.1 App Creation
1. In Map Viewer:  
   **Create App → Instant Apps → Sidebar Template.**

2. **Required Settings**
   - **Title:** `Committee – Topic Explorer`  
     Example: `Security Council – Topic Explorer`
   - **Theme:** Indigo  
   - **Widgets:** Enable **Legend** and **Layer List**  
   - **Translation:** Enable; include **Spanish** and additional relevant languages.  
   - **Footer:** Add “Maps built using Esri ArcGIS Online and Living Atlas.”

3. **Optional Enhancements**
   - Add bookmarks for key regions.  
   - Configure initial extent to show all member nations.  
   - Disable excess widgets for speed.

4. **Performance Testing**
   - Target load time ≤ 3–5 seconds on average school Wi-Fi.  
   - Verify on mobile and low-bandwidth networks.

---

## 6. StoryMap Assembly (Per Committee)

Each committee receives a dedicated **StoryMap**, which integrates both topics and the Instant App.

### 6.1 Structure Template
1. **Title Section**  
   - Committee name and acronym (e.g., *Security Council (SC)*)  
   - One-sentence description.  

2. **Background**  
   - Insert official background text from delegate guide.

3. **Topic A**  
   - Header: `Topic A: [Full Title]`  
   - Embed the Instant App (max width).  

4. **Topic B**  
   - Repeat Topic A format.

5. **Additional Resources**  
   - Conference website  
   - Delegate guide (PDF)  
   - External references (UN, WHO, FAO)

6. **Credits**  
   - Acknowledge authors, platforms, and data providers.

### 6.2 StoryMaps Collection
1. Create a **Collection** to centralize all committee StoryMaps.  
   **Name format:**  

ConferenceName-Atlas-Collection-MapYear

Example: `CAPSMUN-Atlas-Collection-2025`  

2. Share this single Collection link via:
- Conference website  
- Delegate guide QR codes  
- Opening ceremony slides  

---

## 7. Quality Assurance Checklist

### Structure
- [ ] Correct naming convention (`CAPSMUN-SC-Map2025`)  
- [ ] Proper tags applied  
- [ ] Filtered World Countries layer verified  

### Map Design
- [ ] ≤10 relevant layers per topic  
- [ ] Symbology readable and consistent  
- [ ] Legends and pop-ups clean  
- [ ] Basemap properly styled  

### Instant App
- [ ] Sidebar template  
- [ ] Indigo theme  
- [ ] Legend + Layer List enabled  
- [ ] Spanish translation functional  

### StoryMap
- [ ] Background imported from delegate guide  
- [ ] Both topics included  
- [ ] Instant App embedded at full width  
- [ ] Additional resources linked  
- [ ] Credits formatted and complete  

### Final Collection
- [ ] All committees included  
- [ ] Public sharing permissions verified  
- [ ] Load speed and mobile layout confirmed  

---

## 8. Attribution & Credits

**Short Footer (for Apps & StoryMaps)**  

Built with Esri ArcGIS Online and Living Atlas.
Atlas Workflow by Brandon Estevez & Bernard Roach (CAPSMUN).

**Full Credits (for StoryMap "Credits" section)**  

Authors: Brandon Estevez, Bernard Roach
Workflow: Atlas MUN (https://github.com/brandonestevez95/Atlas-MUN-Workflow)

Platforms & Data:
	•	Esri ArcGIS Online — https://www.esri.com
	•	ArcGIS Living Atlas of the World — https://livingatlas.arcgis.com
	•	National 4-H Geospatial Leadership Team — LINK_PLACEHOLDER
	•	Additional datasets credited within layer pop-ups.

License: [Creative Commons Attribution 4.0 International (CC BY 4.0)](https://creativecommons.org/licenses/by/4.0/)

---

## 9. Data Governance

- Maintain **raw datasets privately** in the conference organization’s Esri account.  
- Share only **curated, cleaned maps** through Instant Apps or StoryMaps.  
- Use a **Layer Index spreadsheet** to document:
  - Source URLs  
  - Attribution  
  - Licensing notes  
  - Final status (keep/discard)

**Data Sensitivity:** Exclude PII, secure infrastructure, or non-public datasets.

---

## 10. Accessibility & Localization

- Enable translation tools (Spanish minimum).  
- Use high-contrast color schemes.  
- Replace jargon with plain terms in pop-ups and legends.  
- Test accessibility on mobile and with keyboard navigation.  

---

## 11. Timeline (Recommended Cadence)

| Phase | Days Before Conference | Key Deliverables |
|-------|------------------------|------------------|
| Topic intake & layer search | T–21 to T–14 | Layer Index draft |
| Map assembly & curation | T–13 to T–10 | Core committee maps |
| Instant App setup | T–9 to T–7 | Sidebar apps functional |
| StoryMap assembly | T–6 to T–4 | Committee StoryMaps completed |
| QA & review | T–3 to T–2 | Translations, permissions checked |
| Publish & share | T–1 | Collection live, links distributed |

---

## 12. Version Control

- Commit messages follow:  

committee: change summary

Example:  

SC: Updated pop-ups and replaced emissions dataset

- Keep `CHANGELOG.md` with version notes.  
- Archive old conference versions under year-tagged folders.

---

## 13. Risk & Mitigation

| Issue | Mitigation |
|--------|-------------|
| Slow map performance | Reduce layer count, simplify geometry |
| Broken data links | Replace from Layer Index backups |
| Duplicate delegations | Validate committee country lists pre-publish |
| Translation errors | Manual review before final QA |

---

## 14. Behind-the-Scenes StoryMap (Upcoming)

A public StoryMap documenting Atlas’s creation, CAPSMUN’s GIS process, and delegate impact is in development.

https://storymaps.arcgis.com/stories/e6b6538e81ad47e2b6d2d7d9f24b19cf

---

## 15. Appendix

### A) Layer Index (Template)

committee,topic,layer_name,provider,url,license,geometry,year,unit,popup_fields,style_notes,keep/discard

### B) StoryMap Structure Example

Security Council (SC)

Brief description…

Background

[Text from delegate guide]

Topic A: Nuclear Nonproliferation

[Embedded Instant App]

Topic B: Cybersecurity in Critical Infrastructure

[Embedded Instant App]

Additional Resources
	•	Conference Site: LINK
	•	Delegate Guide (PDF): LINK
	•	UN/WHO References: LINKs


16. Attribution & License

Built with:
	•	Esri ArcGIS Online — https://www.esri.com
	•	ArcGIS Living Atlas of the World — https://livingatlas.arcgis.com
	•	National 4-H Geospatial Leadership Team — LINK_PLACEHOLDER

© 2025 Brandon Estevez & Bernard Roach.
Licensed under Creative Commons Attribution 4.0 International (CC BY 4.0).

---

Would you like me to add GitHub-optimized Markdown styling (badges, table of contents links, section anchors, etc.) for a final version that looks publication-ready inside your repo viewer?
