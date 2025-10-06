# V-lcanes_XML_y_DTD# 🌋 Prueba de Examen XML – Actividad 11

Este proyecto consiste en la creación de un documento **XML** junto con su correspondiente **DTD**, representando información sobre **la erupción volcánica en La Palma (Islas Canarias)**.  
El objetivo principal es validar la correcta estructuración y definición de elementos, atributos y relaciones dentro de un conjunto de datos jerárquico.

---

## 🗂️ Estructura del proyecto

📁 PruebaExamenXML/
├── Activity11.dtd
├── Activity11.xml
└── README.md

## 👥 Colaboradores

| Nombre | Rol |
|---------|-----|
| 🧑‍💻 Joana Ramírez | (@ixf2) Autora principal del XML y DTD |
| 👨‍💻 Víctor Vergara | (@sdvictorvergara) Validación del DTD y revisión del XML |

## 📘 Descripción del contenido

### 🧩 XML – `Activity11.xml`

El archivo XML describe información detallada sobre:
- 🌋 **Volcanes** y sus fechas de actividad (`start_date`, `final_date`)
- 🏝️ **Islas afectadas**, con nombre y áreas impactadas
- 🏘️ **Municipios** y zonas evacuadas
- 🧑‍🚒 **Recursos humanos y materiales** utilizados
- 👷 **Tareas** realizadas durante la emergencia

📄 **Ejemplo:**
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

