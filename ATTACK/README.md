# ATT&CK - STIX Content 
The STIX content found here is the unabridged conversion of the MITRE ATT&CK catalog in its entirety. All of the converted STIX Objects can be found individually in all the subdirectories enumerated here (i.e. organized by STIX object type) OR compiled in a single json file (mitre-attack.json). The STIX 2.0 content is in the json format.

## ATT&CK -> STIX 2.0 Mapping (High-Level)
* ATT&CK Technique -> STIX Attack-Pattern
* ATT&CK Tactic -> STIX Attack-Pattern.Kill-Chain-Phase, STIX Tool.Kill-Chain-Phase, STIX Malware.Kill-Chain-Phase
* ATT&CK Group -> STIX Intrusion-Set
* ATT&CK Software -> STIX Malware (OR) STIX Tool
* ATT&CK Mitigation -> STIX Course-of-Action

## ATT&CK -> STIX 2.0 Mapping (Detailed)

**Bold** signifies data pulled from ATT&CK model objects

**(Custom)** signifies STIX object properties that are not apart of the standard STIX 2.0 data model but were added for further fidelity in the mapping from ATT&CK.

### ATT&CK Technique -> STIX Attack-Pattern

Attack-Pattern.type = *"attack-pattern"*  
Attack-Pattern.id = *"attack-pattern-uuid"*  
Attack-Pattern.created = [date created]  
Attack-Pattern.modified = [date modified]  
Attack-Pattern.name = **Name of ATT&CK software**  
Attack-Pattern.labels = (Hand selected)  
Attack-Pattern.description = **Taken from ATT&CK page entry - also includes ATT&CK fields for effective permissions, data sources, requires network, supports remote, and detection**  
Attack-Pattern.external_references = **References from ATT&CK**  
Attack-Pattern.kill_chain_phases = **ATT&CK Tactic**  
Attack-Pattern.x_mitre_contributors **(Custom)** = **ATT&CK Technique.Contributors**  
Attack-Pattern.x_mitre_data_sources **(Custom)** = **ATT&CK Technique.Data Sources**  
Attack-Pattern.x-mitre_platforms **(Custom)** = **ATT&CK Technique.Platforms**  

### ATT&CK Tactic -> STIX Attack-Pattern.Kill-Chain-Phase, STIX Tool.Kill-Chain-Phase, STIX Malware.Kill-Chain-Phase
Attack-Pattern.kill_chain_phases = **ATT&CK Tactic**

Malware.kill_chain_phases = **ATT&CK Tactic**

Tool.kill_chain_phases = **ATT&CK Tactic**

### ATT&CK Group -> STIX Intrusion-Set

Intrusion-Set.type = *"intrusion-set"*  
Intrusion-Set.id = *"intrusion-set-uuid"*  
Intrusion-Set.created = [date created]  
Intrusion-Set.modified = [date modified]  
Intrusion-Set.name = **Name of ATT&CK Group**  
Intrusion-Set.aliases = **List of ATT&CK Group.aliases**  
Intrusion-Set.description = **Taken from ATT&CK page entry**  
Intrusion-Set.external_references = **References from ATT&CK**  

### ATT&CK Software -> STIX Malware (OR) STIX Tool

Malware.type = *"malware"*  
Malware.id = *"malware-uuid"*  
Malware.created = [date created]  
Malware.modified = [date modified]  
Malware.name = **Name of ATT&CK software**  
Malware.labels = (hand selected)  
Malware.description = **Taken from ATT&CK page entry**  
Malware.external_references = **References from ATT&CK**  
Malware.kill_chain_phases = **Taken from ATT&CK page entry: backtracked from technique to tactic**  
Malware.x_mitre-aliases **(custom)** = **Fill in**  

Tool.type = *"tool"*  
Tool.id = *"tool-uuid"*  
Tool.created = [date created]  
Tool.modified = [date modified]  
Tool.name = **Name of ATT&CK software**  
Tool.labels = (hand selected)  
Tool.description = **Taken from ATT&CK page entry**  
Tool.external_references = **References from ATT&CK**  
Tool.kill_chain_phases = **Taken from ATT&CK page entry: backtracked from technique to tactic** 
Tool.x_mitre_aliases **(custom)** = ** Fill In**

### ATT&CK Mitigation -> STIX Course-of-Action

Course-of-Action.type = *"course-of-action"*  
Course-of-Action.id = *"course-of-action-uuid"*  
Course-of-Action.created = [date created]  
Course-of-Action.modified = [date modified]  
Course-of-Action.name = **Name of ATT&CK software**  
Course-of-Action.description = **Taken from ATT&CK page entry**  
Course-of-Action.external_references = **References from ATT&CK**  

## Life Cycle
As the MITRE ATT&CK catalog - to include Tactics, Techniques, Groups, Software, and Mitigations - is further developed and expanded, so to will this repository of translated STIX content. Any modification to the ATT&CK catalog triggers an immediate process to assess and update the existing STIX content found here. 

Explicit concern is paid to the maintenance of the STIX Object versions. All converted ATT&CK content follows the STIX versioning policy (read the docs: https://oasis-open.github.io/cti-documentation/). 