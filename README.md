# 🌋 XML and DTD Exam Project – Activity 11

This project involves creating an **XML document** together with its corresponding **DTD**, representing information about the **volcanic eruption in La Palma (Canary Islands)**.  
The main goal is to validate the correct structure and definition of elements, attributes, and relationships within a hierarchical data set.

## 🗂️ Project Structure
📁 PruebaExamenXML/
├── Activity11.dtd
├── Activity11.xml
└── README.md
---

## 👥 Collaborators

| Name | Role |
|------|------|
| 🧑‍💻 Joana Ramírez (@ixf2) | Main author of the XML and DTD |
| 👨‍💻 Víctor Vergara (@sdvictorvergara) | DTD validation and XML review |

---

## 📘 Content Description

### 🧩 XML – `Activity11.xml`

The XML file provides detailed information about:

- 🌋 **Volcanoes** and their activity dates (`start_date`, `final_date`)  
- 🏝️ **Affected islands**, with names and impacted areas  
- 🏘️ **Municipalities** and **evacuated zones**  
- 🧑‍🚒 **Human and material resources** used  
- 👷 **Tasks** carried out during the emergency  

📄 **Example:**

**XML:**
```xml
<CanaryIsland>
    <volcanos start_date="19-09-2001" final_date="12-12-2001">
        <islands>
            <island name_island="La Palma">
                <affectead_area>
                    <zones>
                        <zone>Todoque</zone>
                        <municipalities>
                            <municipality name_municipality="Los Llanos de Aridane" sos="123123123">
                                <civil_service>23</civil_service>
                            </municipality>
                        </municipalities>
                    </zones>
                </affectead_area>
                <resource>
                    <materials>
                        <material und="3">Helicopter</material>
                    </materials>
                    <humans>
                        <human name="Juan" surname="Ramírez Delgado" dni="1212121212S">
                            <task date_task="3 horas">Ayudar en la evacuación de los habitantes de Todoque</task>
                        </human>
                    </humans>
                </resource>
            </island>
        </islands>
    </volcanos>
</CanaryIsland>
```

**DTD:**
```dtd
<!ELEMENT CanaryIsland (volcanos)>
<!ELEMENT volcanos (volcano*)>
<!ELEMENT volcano (affected_area*, resource)>
<!ATTLIST volcano 
    name_island CDATA #REQUIRED
    start_date CDATA #REQUIRED
    final_date CDATA #REQUIRED>
<!ELEMENT affected_area (zones, municipalities)>
<!ELEMENT zones (zone*)>
<!ELEMENT zone (#PCDATA)>
<!ELEMENT municipalities (municipality*)>
<!ELEMENT municipality (emergencyPhones, civil_service?)>
<!ATTLIST municipality name_municipality CDATA #REQUIRED>
<!ELEMENT emergencyPhones (emergencyPhone*)>
<!ELEMENT emergencyPhone (#PCDATA)>
<!ELEMENT civil_service (#PCDATA)>
<!ELEMENT resource (material, humans)>
<!ELEMENT material (#PCDATA)>
<!ATTLIST material und CDATA #REQUIRED>
<!ELEMENT humans (human*)>
<!ELEMENT human (task+)>
<!ATTLIST human 
    name_human CDATA #REQUIRED
    surname_human CDATA #REQUIRED
    dni CDATA #REQUIRED>
<!ELEMENT task (#PCDATA)>
<!ATTLIST task 
    date_task CDATA #REQUIRED
    hour CDATA #REQUIRED>
```


## Acknowlegment

Special thanks to:

- **Professor Tiburcio** who taught us
- **@Jes1997** We take reference to learn how to correctly do the readme and the license https://github.com/Jes1997
- We also take reference from: https://github.com/othneildrew/Best-README-Template and https://github.com/PurpleBooth/a-good-readme-template