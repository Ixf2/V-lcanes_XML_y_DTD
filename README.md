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

