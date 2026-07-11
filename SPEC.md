# The Semantic Life Versioning (LifeVer) Standard v1.5.0
**Last Updated**: 2026-07-11
**Authors**: A Master Software Architect and a forward-thinking user.

See [CHANGELOG.md](./CHANGELOG.md) for the standard's own version history.
## Preamble
The Semantic Life Versioning (LifeVer) standard is a comprehensive framework for tracking personal accomplishments, significant events, and personal growth over time. It provides a structured, consistent, and reviewable format for logging the "changes" that constitute a life. Its purpose is to foster reflection, provide perspective, and create a meaningful, personal history of progress and resilience.
## 1. Versioning Scheme
LifeVer uses a three-part versioning number: `EPOCH.MILESTONE.STEP`.
-   **`EPOCH`**: Represents a fundamental era or chapter of your life. It increments only when a life event occurs that fundamentally alters your core identity, responsibilities, or daily reality (e.g., marriage, parenthood, career change, moving to a new country).  
-   **`MILESTONE`**: Represents the achievement of a significant goal or the completion of a major project. It is a noteworthy "feature release" for your life that adds new capabilities or experiences (e.g., running a marathon, completing a major certification, finishing a large home renovation).  
-   **`STEP`**: Represents a single, meaningful accomplishment or a collection of smaller accomplishments bundled into one "release." It is the incremental progress you make on a daily or weekly basis (e.g., reading a book, fixing an appliance, successfully completing a work sprint).

**The MILESTONE Test**: An accomplishment qualifies as a MILESTONE only when both are true: (1) it took sustained, deliberate effort spread across multiple weeks or months toward one named goal, and (2) it leaves something lasting behind — a credential, a finished project, a permanently changed environment, a new fact about you — not just the memory of having done it. If only one is true, log it as a STEP. This test applies to `Added`, `Improved`, `Fixed`, and `Removed` entries. For `Changed` entries — things that happened to you rather than through your own effort — judge the tier by severity and impact instead; see Section 6.

**Rule**: When a higher-level version number is incremented, all lower-level numbers reset to 0. For example, after `42.1.3` comes the milestone `42.2.0`. After the epoch change `42.12.5` comes `43.0.0`.
## 2. The Changelog File & Workflow
The official log is maintained in a single Markdown file named `changelog.md`. New entries are always added to the top of the file.
The key to the LifeVer workflow is the `[Unreleased]` section.
1.  **Capture**: A special `## [Unreleased]` heading always exists at the top of the file. As you accomplish tasks throughout your day or week, you add them as bullet points under this heading. This is a low-friction method for capturing progress as it happens.  
2.  **Review & Release**: At a cadence of your choosing (e.g., weekly), you perform a "Review & Release Ceremony." You review all items under `[Unreleased]`.  
3.  **Versioning**: Based on the review, you determine the next version number. You then replace the `## [Unreleased]` heading with the new version number and the current date (e.g., `## [42.1.4] - 2025-06-13`).  
4.  **Reset**: A new, empty `## [Unreleased]` section is created at the top of the file, ready for the next cycle.
## 3. Entry Structure
Each versioned entry must adhere to the following structure:
```markdown
## [EPOCH.MILESTONE.STEP] - YYYY-MM-DD
### Type
- **[Scope]**: A concise, past-tense description of the accomplishment or change.
- **[Scope]**: Another description.
### Another Type
- **[Scope]**: Description.
```
-   **Header (`##`)**: Contains the full version number in brackets, a hyphen, and the date of the "Review & Release" in `YYYY-MM-DD` format.  
-   **Type (`###`)**: One of the five official Change Types (see Section 4).  
-   **Item (`-`)**: A bulleted list item containing the Scope and Description.  
-   **Scope (`**[Scope]:**`)**: The life domain of the item, presented in bold with brackets and a colon.  
-   **Description**: A brief text describing the change.
## 4. Change Types
This is a stable list. These five types are the only valid types to be used for categorizing entries.
-   **`Added`**: For introducing something new to your life (a skill, habit, routine, item).  
-   **`Improved`**: For enhancing an existing skill, process, or area of your life through your own agency.  
-   **`Changed`**: For logging a factual change in state, especially one that is neutral, negative, or externally imposed (e.g., a diagnosis, a layoff, a relocation).  
-   **`Fixed`**: For solving a distinct problem, bug, or source of friction.  
-   **`Removed`**: For intentionally stopping a habit or removing a responsibility, item, or commitment.
## 5. Scopes
Scopes represent the various domains of your life. This is an extensible list, allowing you to tailor it to your life.
#### Initial Core Scopes:
-   `[Work]`: Your profession and career.  
-   `[Family]`: Relationships with family and children.  
-   `[Personal]`: Individual growth, hobbies, and learning.  
-   `[Health]`: Physical and mental well-being.  
-   `[Home]`: Management of your living space.  
-   `[Spiritual]`: Connection to faith, purpose, and meaning.  
-   `[Financial]`: Management of personal finances.
#### Extensibility:
You are encouraged to add new Scopes as needed. A good guideline is the **"Rule of Three"**: If you have three or more entries that feel like they belong to a new, distinct category, create a new Scope for them. If earlier entries would now fit better under the new Scope, you may retag them for consistency — see Section 6 for why this doesn't compromise the integrity of the log.
## 6. Guiding Principles
-   **Separation of Concerns**: The LifeVer Changelog is for logging the past. Planning for the future should be done in a separate "Issue Tracker" (i.e., any to-do list application or notebook).  
-   **Curation over Raw Data**: Log the *accomplishment*, not every single task. Summarize and curate your entries to reflect the meaningful outcome.  
-   **Honesty and Resilience**: Use the `Changed` type to log difficult events truthfully. Use the other types to log your resilient responses to those events. A `Changed` entry is not limited to STEP tier — its severity, not its type, determines whether it warrants a MILESTONE or even an EPOCH release. A layoff or a serious diagnosis can be exactly as version-significant as an achievement.
-   **Immutable History, Correctable Record**: The events of your past cannot be changed — once something has happened, it will always have happened. The changelog, however, is your *record* of that history, and a record can be imperfect. Correcting a past entry, such as retagging its Scope for consistency (see Section 5), does not rewrite what happened; it only makes the log more faithful to it.
-   **Private by Default, Curated by Choice**: The changelog is a private record, not a public one. If you want to share your progress — a status report for work, a summary for family — build it as a separate, curated derivative of specific entries. Never treat the raw log itself as the shareable artifact.
## 7. Full Example
#### 1. State of `changelog.md` before weekly review:
```markdown  
# My Life Changelog
## [Unreleased]
### Added  
- **[Personal]:** Finished reading "Dune" by Frank Herbert.  
- **[Home]:** Installed new smart thermostat.
### Fixed  
- **[Work]:** Resolved the recurring sync issue in the reporting module that was causing user complaints.
### Improved  
- **[Family]:** Taught my daughter how to properly structure a five-paragraph essay for her school project.
---  
## [42.1.3] - 2025-06-06  
... (previous entries) ...  
```
#### 2. After the "Review & Release Ceremony" on June 13, 2025:
```markdown
# My Life Changelog
## [Unreleased]
---  
## [42.1.4] - 2025-06-13
### Added  
- **[Personal]:** Finished reading "Dune" by Frank Herbert.  
- **[Home]:** Installed new smart thermostat.
### Fixed  
- **[Work]:** Resolved the recurring sync issue in the reporting module that was causing user complaints.
### Improved  
- **[Family]:** Taught my daughter how to properly structure a five-paragraph essay for her school project.
---  
## [42.1.3] - 2025-06-06  
... (previous entries) ...  
```
## Appendix A: Notes for AI & Automated Systems
This section provides technical details for parsing and interacting with changelog.md files that adhere to the LifeVer 1.4 standard.  
1. **File Encoding**: UTF-8 is recommended.  
2. **Entry Delimiters**: Each entry begins with a Markdown H2 header (`##`).  
3. **Header Parsing**: The versioned entry header can be reliably parsed with the following Regular Expression**: `^## \[((\d+)\.(\d+)\.(\d+))\] - ((\d{4})-(\d{2})-(\d{2}))$`  
4. **Unreleased Header**: The unreleased section header is static: `## [Unreleased]`  
5. **Type Delimiters**: Change Types within an entry are denoted by a Markdown H3 header (`###`). The valid string values are: `Added`, `Improved`, `Changed`, `Fixed`, `Removed`.  
6. **Item Parsing**: Each accomplishment is a list item beginning with `-` . The Scope can be extracted with the regex `^\- \*\*\[([^\]]+)\]:\*\*` which captures the text inside the brackets. The remaining text on the line is the description.  
7. **Data Model**: A parser should be able to transform an entry into a structured object, for example (in JSON):
```JSON  
{  
"version": "42.1.4",  
"release_date": "2025-06-13",  
"changes": [  
{  
"type": "Added",  
"scope": "Personal",  
"description": "Finished reading \"Dune\" by Frank Herbert."  
},  
{  
"type": "Added",  
"scope": "Home",  
"description": "Installed new smart thermostat."  
},  
{  
"type": "Fixed",  
"scope": "Work",  
"description": "Resolved the recurring sync issue in the reporting module that was causing user complaints."  
},  
{  
"type": "Improved",  
"scope": "Family",  
"description": "Taught my daughter how to properly structure a five-paragraph essay for her school project."  
}  
]  
}
```
