# accidents.csv
|Spaltenname|Beschreibung|Bemerkung|
|-|-|-|
|STATE|Enthält den Code des US-Bundesstaates, in dem der Unfall stattgefunden hat.||
|STATENAME|Gibt den vollständigen Namen des US-Bundesstaates aus.|-|
|ST_CASE|Dieses Element identifiziert die eindeutige Fallnummer, die vom Dateneingabesystem vergeben wurde.|Bitte füllen Sie die FARS-Formulare mit der vom RBIS vergebenen Fallnummer aus.|
|PEDS|Dieses Element erfasst die Anzahl der Personen-Formulare, die für diesen Fall relevant sind – speziell für Personen, die nicht als Kraftfahrzeuginsassen erfasst werden (z. B. Fußgänger, Radfahrer etc.).|Zählung gemäß Feld „Anzahl Personen, die sich nicht in Kraftfahrzeugen befinden“. Motorfahrzeuginsassen (z.B. Autofahrer) werden ausgeschlossen. Erfasst werden beispielsweise: Personen in nicht-motorisierten Transportmitteln (z.B. in einer Pferdekutsche, Code 04), Fußgänger/Radfahrer (z.B. ein Fußgänger, Code 05–07), Nutzer persönlicher Fortbewegungsmittel (z.B. Skateboardfahrer, Code 11–13) sowie verletzte Personen in Gebäuden (z.B. in einem Geschäft, Code 10).|
|VE_TOTAL|Dieses Element erfasst alle Kraftfahrzeuge, die in Kontakt kamen und vom Beamten im Polizeiunfallbericht als an dem Unfall beteiligte Einheit gemeldet wurden.|Eingeschlossen sind Fahrzeuge, die sich im Transport befinden, Fahrzeuge, die nicht im Transport sind (z. B. geparkte, abseits der Fahrbahn angehaltene oder im Einsatz befindliche Kraftfahrzeuge), sowie Fahrzeuge, die sich außerhalb der Fahrbahngrenzen befinden.|
|PERSONS|Erfasst die Anzahl der Kraftfahrzeuginsassen, wie sie in den zugehörigen Personenformularen angegeben sind. Dieser Wert wird während der Fallstrukturierung abgeleitet.|Dieses Element wird beim Strukturieren des Falls abgeleitet. Siehe Abschnitt 203 „How to Structure a Case“ für weitere Hinweise.|
|COUNTY|Dieses Element bezieht sich auf den Ort des unstabilisierten Ereignisses hinsichtlich Landkreis/Stadt.|County und City werden als ein Feld erfasst und müssen zusammen übermittelt werden. Ist nur der County bekannt, kann City mit 9999 (Unbekannt) codiert werden. Codieren Sie City als 0000 (Nicht zutreffend), wenn der Unfall außerhalb der Stadtgrenzen erfolgt; als 9997 (Andere), wenn die Stadt nicht zu den GSA-Codes gehört; oder als 9999 (Unbekannt), wenn der Unfallort unbekannt ist. Codieren Sie County als 997 (Andere), wenn dieser nicht zu den GSA-Codes gehört, bzw. als 999 (Unbekannt), wenn der Ort unbekannt ist. Generell sollten 000/0000 (Nicht zutreffend) verwendet werden, wenn kein GSA-Code existiert, und 997/9997 (Andere), wenn ein GSA-Code existiert, aber nicht in der Masterliste von NHTSA erscheint – beide Fälle sind an NHTSA zu melden. Verwenden Sie 998/9898 (Nicht gemeldet), wenn keine Information vorliegt (z.B. wenn das entsprechende Feld fehlt oder leer ist und keine weiteren Angaben vorhanden sind). Falls das Crash-Report-Handbuch eines Bundeslandes vorsieht, nicht zutreffende Felder leer zu lassen, gilt ein leeres Feld NICHT als „Nicht gemeldet“ – in solchen Fällen prüfen Sie, ob „Unbekannt“ passender ist.|
|MONTH|Dieses Element identifiziert das Datum, an dem der Unfall stattgefunden hat.|Wenn der Polizeibericht angibt, dass der Unfall (in der Regel Fahrerflucht) zwischen einer p.m.- und a.m.-Zeit (z. B. 20:00 und 06:00 Uhr) am Vortag oder Folgetag stattfand, codieren Sie den Unfall als am Folgetag. Wird ein Zeitraum (z. B. zwischen Sonntag und Freitag) angegeben, verwenden Sie das letzte Datum (z. B. Freitag). FARS SPEZIALINSTRUKTION: Falls das Unfall-Datum im Polizeibericht als unbekannt gemeldet wird, nutzen Sie zur Festlegung des Datums das Sterbedatum aus der Sterbeurkunde. CRSS SPEZIALINSTRUKTION: Das Datum wird aus dem CRSS-Stichprobenprogramm übernommen. Ist das Datum unbekannt, verwenden Sie das Melde-Datum. Ist die Unfallzeit unbekannt, tragen Sie 9999 ein. Kann der Monat nicht aus dem Polizeibericht ermittelt werden, verwenden Sie den Monat des "Ending Contact Date" aus der Inventaraufzeichnung. Stimmen die Unfall-Daten im Polizeibericht und auf dem Dateneingabebildschirm nicht überein und ist der Polizeibericht korrekt, wird das Datum korrigiert.|
|DAY|Dieses Element identifiziert das Datum, an dem der Unfall stattgefunden hat.|Falls im Polizeibericht angegeben wird, dass der Unfall (in der Regel Fahrerflucht) zwischen einer p.m.- und a.m.-Zeit (z. B. 20:00 und 06:00 Uhr) am Vortag oder Folgetag erfolgte, codieren Sie den Unfall als am Folgetag stattgefunden. Wird ein Zeitraum (z. B. zwischen Sonntag und Freitag) angegeben, verwenden Sie das letzte Datum des Zeitraums (z. B. Freitag). FARS SPEZIALINSTRUKTION: Falls das Unfall-Datum im Polizeibericht als unbekannt gemeldet wird, ziehen Sie zur Festlegung des Datums das Sterbedatum aus der Sterbeurkunde heran. CRSS SPEZIALINSTRUKTION: Das Unfall-Datum wird aus dem CRSS-Stichprobenprogramm übernommen. Ist das Datum unbekannt, verwenden Sie das Melde-Datum; ist die Unfallzeit unbekannt, tragen Sie 9999 ein. Kann der Monat nicht aus dem Polizeibericht ermittelt werden, verwenden Sie den Monat des "Ending Contact Date" aus der Inventaraufzeichnung. Stimmen die Unfall-Daten im Polizeibericht und auf dem Dateneingabebildschirm nicht überein und wird der Polizeibericht als korrekt befunden, wird das Datum entsprechend korrigiert.|
|YEAR|Dieses Element identifiziert das Datum, an dem der Unfall stattgefunden hat.|Falls im Polizeibericht angegeben wird, dass der Unfall (zumeist Fahrerflucht) zwischen einer p.m.- und einer a.m.-Zeit (z.B. 20:00 Uhr und 06:00 Uhr) am Vortag oder Folgetag erfolgte, codieren Sie den Unfall als am Folgetag stattgefunden. Wird ein Zeitraum (z.B. von Sonntag bis Freitag) angegeben, verwenden Sie das letzte Datum (z.B. Freitag). FARS SPEZIALINSTRUKTION: Ist das Unfall-Datum im Polizeibericht als unbekannt gemeldet, ziehen Sie zur Festlegung des Datums das Sterbedatum aus der Sterbeurkunde heran. CRSS SPEZIALINSTRUKTION: Das Datum wird aus dem CRSS-Stichprobenprogramm übernommen. Ist das Datum unbekannt, verwenden Sie das Melde-Datum; ist die Unfallzeit unbekannt, tragen Sie 9999 ein. Kann der Monat nicht aus dem Polizeibericht ermittelt werden, verwenden Sie den Monat des „Ending Contact Date“ aus der Inventaraufzeichnung. Stimmen die Unfall-Daten im Polizeibericht und auf dem Dateneingabebildschirm nicht überein und gilt der Polizeibericht als korrekt, wird das Datum entsprechend korrigiert.|
|HOUR|Dieses Element identifiziert die Uhrzeit, zu der der Unfall stattgefunden hat.|Tragen Sie die Uhrzeit ein, wie sie im Polizeibericht angegeben ist – diese Angabe ist in jedem Fall vorzuziehen. Falls die Unfallzeit nicht gemeldet, unbekannt oder als fehlerhaft bekannt ist, nutzen Sie alle verfügbaren Fallinformationen, um die UNFALLZEIT zu bestimmen. Kann die Stunde nicht ermittelt werden, geben Sie 9999 (Unbekannt) ein.|
|MINUTE|Dieses Element identifiziert die Minute, zu der der Unfall stattgefunden hat.|Tragen Sie die Unfallzeit so ein, wie sie im Polizeibericht angegeben ist – dies ist in allen Fällen die bevorzugte Angabe. Falls die Unfallzeit nicht gemeldet, unbekannt oder fehlerhaft ist, nutzen Sie alle verfügbaren Fallinformationen, um die Unfallzeit zu bestimmen. Kann die Minute nicht ermittelt werden, geben Sie 9999 (Unbekannt) ein.|
|TWAY_ID|Dieses Element erfasst die Bezeichnung (den Namen) der Fahrbahn, auf der der Unfall stattfand.||
|TWAY_ID2|	Dieses Element erfasst die Bezeichnung (den Namen) der Fahrbahn, auf der der Unfall stattfand.||
|ROUTE|	Dieses Element identifiziert die Beschilderung der Fahrtroute, auf der der Unfall stattfand. Codieren Sie den Wert, der das von der FHWA genehmigte Landnutzungs- und Funktionssystem repräsentiert. Es muss die FHWA-Klassifikation verwendet werden, die vom staatlichen Straßenverkehrsamt bereitgestellt wird. Keine andere Klassifikationsquelle ist zulässig. Bei Problemen wenden Sie sich an das Planungsbüro des zuständigen Verkehrsministeriums.|Vor der Codierung sicherstellen, welcher Fahrbahnabschnitt gemeint ist. Dieses Element bezieht sich auf den Fahrbahnabschnitt in der obersten Zeile der Fahrbahnidentifikation. Bei Unklarheiten konsultieren Sie das Bemerkungsfeld der Fahrbahnidentifikation für die Hierarchie zur Auswahl des richtigen Fahrbahnabschnitts.|
|RUR_URB|Dieses Element erfasst die Klassifikation des Fahrbahnabschnitts, auf dem der Unfall stattfand, basierend auf den von der Federal Highway Administration (FHWA) genehmigten, angepassten Volkszählungsgrenzen für kleine städtische Gebiete und Ballungsräume.|Vor der Codierung dieses Elements stellen Sie sicher, welche Fahrbahn codiert werden soll. Dieses Element wird in Bezug auf die in den Feldern NATIONAL HIGHWAY SYSTEM, OWNERSHIP, ROUTE SIGNING und in der obersten Zeile der TRAFFICWAY IDENTIFIER ausgewählte Fahrbahn codiert. Eine Ausnahme bildet ein Kreuzungsunfall in einer Autobahnauffahrt. Siehe die Bemerkungen in TRAFFICWAY IDENTIFIER für die Hierarchie zur Auswahl der entsprechenden Fahrbahn. Codieren Sie den Wert, der das von der FHWA genehmigte Landnutzungs- und Funktionssystem repräsentiert. Die FHWA-Klassifikation, die vom staatlichen Straßenverkehrsamt bereitgestellt wird, muss verwendet werden. Keine andere Klassifikationsquelle ist zulässig. Bei Problemen wenden Sie sich bitte an das Planungsbüro des zuständigen Verkehrsministeriums.|
|FUNC_SYS|Dieses Element identifiziert die funktionale Klassifikation des Fahrbahnabschnitts, auf dem der Unfall stattfand.|Vor der Codierung dieses Elements stellen Sie sicher, welche Fahrbahn codiert werden soll. Dieses Element wird in Bezug auf die in den Feldern NATIONAL HIGHWAY SYSTEM, OWNERSHIP, ROUTE SIGNING und in der obersten Zeile der TRAFFICWAY IDENTIFIER ausgewählte Fahrbahn codiert. Eine Ausnahme bildet ein Kreuzungsunfall in einer Autobahnauffahrt. Siehe die Bemerkungen in TRAFFICWAY IDENTIFIER für die Hierarchie zur Auswahl der entsprechenden Fahrbahn. Codieren Sie den Wert, der das von der FHWA genehmigte Landnutzungs- und Funktionssystem repräsentiert. Die FHWA-Klassifikation, die vom staatlichen Straßenverkehrsamt bereitgestellt wird, muss verwendet werden. Keine andere Klassifikationsquelle ist zulässig. Bei Problemen wenden Sie sich bitte an das Planungsbüro des zuständigen Verkehrsministeriums.|
|RD_OWNER|Dieses Element identifiziert die Organisation, die das rechtliche Eigentum an dem Fahrbahnabschnitt besitzt, auf dem der Unfall stattfand.|Vor der Codierung dieses Elements stellen Sie sicher, welche Fahrbahn codiert werden soll. Dieses Element wird in Bezug auf die in den Feldern NATIONAL HIGHWAY SYSTEM, LAND USE AND FUNCTIONAL SYSTEM, ROUTE SIGNING und in der obersten Zeile der TRAFFICWAY IDENTIFIER ausgewählte Fahrbahn codiert. Eine Ausnahme bildet ein Kreuzungsunfall in einer Autobahnauffahrt. Bitte entnehmen Sie die Hierarchie zur Auswahl der entsprechenden Fahrbahn den Bemerkungen in TRAFFICWAY IDENTIFIER.|
|NHS|Dieses Element identifiziert, ob der Unfall auf einer Fahrbahn stattfand, die Teil des National Highway System ist.|Das National Highway System umfasst das Interstate System und besteht aus den Hauptverkehrsstraßen sowie einigen Verbindungsrouten des Strategic Highway Network, die funktional unterhalb der Hauptverkehrsstraßen klassifiziert werden. Es muss die von der FHWA bereitgestellte Klassifikation (vom staatlichen Straßenverkehrsamt) verwendet werden. Keine andere Klassifikationsquelle ist zulässig. Bei Problemen wenden Sie sich an den zuständigen Regional State Assignee.|
|SP_JUR|Dieses Element identifiziert, ob der Unfallort auf der Fahrbahn als Sonderzuständigkeitsbereich gilt – auch wenn er von staatlichen, kreislichen oder lokalen Polizeikräften überwacht wird (z. B. Staatsstraßen in Indianerreservaten).|Die Straße muss unter die Regelung einer Sonderzuständigkeit fallen, auch wenn sie von staatlichen, kreislichen oder lokalen Polizeikräften überwacht wird. Es besteht ein Unterschied zwischen Nationalpark und Nationalwald: Nur Gebiete, die als Nationalpark ausgewiesen sind, sollten mit 1 (National Park Service) codiert werden; Staatsparks sind mit 8 (Andere) zu codieren, und Nationalwälder mit 0 (Keine Sonderzuständigkeit). Staatsstraßen in Indianerreservaten müssen als 3 (Indian Reservation) codiert werden.|
|MILEPT|Dieses Element identifiziert den Meilenpunkt, der dem Unfallort am nächsten liegt.|Siehe Bemerkungen im Abschnitt LAND USE AND FUNCTIONAL SYSTEM zur Auswahl der zu codierenden Fahrbahn. Codieren Sie den Meilenpunkt des entsprechenden TRAFFICWAY IDENTIFIER. Bei Unfällen auf Ein- oder Ausfahrten verwenden Sie den Meilenpunkt der jeweiligen Auffahrt. Beim Übergang zwischen zwei Fahrbahnen gleicher funktionaler Klasse wählen Sie den Meilenpunkt der ausfahrenden Fahrbahn. Angaben erfolgen laut dem staatlichen Straßenverkehrsamt: Der tatsächliche Meilenpunkt ist auf 0,1 Meile genau mit Dezimalstelle anzugeben und, falls weniger als fünf Ziffern vorhanden sind, rechtsbündig aufzufüllen (z. B. 10 muss als „0010.0“ codiert werden).|
|LATITUDE|Dieses Element identifiziert den Unfallort anhand von Global Position-Koordinaten (Breite).|Global Position bezieht sich auf den geografischen Ort des Unfalls, ausgedrückt in Grad, Minuten und Sekunden der Breite (Latitude) und Länge (Longitude): Breite: dd mm ss.ss (Grad/Minuten/Sekunden) Länge: ddd mm ss.ss (Grad/Minuten/Sekunden) In einigen Fällen können Längenangaben als negative Zahlen erscheinen; das Minuszeichen ist zu ignorieren. Codieren Sie vollständige, gültige Werte für Breite und Länge, sofern vorhanden. Gültige Minuten und Sekunden müssen codiert werden, wenn ein gültiger Gradwert vorliegt (z. B. ist "38 99 99.99" ungültig).|
|LONGITUD|Dieses Element identifiziert den Unfallort anhand von Global Position-Koordinaten (Länge).|Global Position bezieht sich auf den geografischen Ort des Unfalls, ausgedrückt in Grad, Minuten und Sekunden der Breite (Latitude) und Länge (Longitude): Breite: dd mm ss.ss (Grad/Minuten/Sekunden) Länge: ddd mm ss.ss (Grad/Minuten/Sekunden) In einigen Fällen können Längenangaben als negative Zahlen erscheinen; das Minuszeichen ist zu ignorieren. Codieren Sie vollständige, gültige Werte für Breite und Länge, sofern vorhanden. Gültige Minuten und Sekunden müssen codiert werden, wenn ein gültiger Gradwert vorliegt (z. B. ist "38 99 99.99" ungültig).|
|HARM_EV|Dieses Element identifiziert das erste verletzungs- oder schadenverursachende Ereignis des Unfalls.||
|MAN_COLL|Dieses Element erfasst die Ausrichtung von zwei im Transport befindlichen Kraftfahrzeugen, die am ERSTEN SCHADENSVERURSACHENDEN EREIGNIS eines Auffahrunfalls beteiligt sind. Falls das ERSTE SCHADENSVERURSACHENDE EREIGNIS keine Kollision zwischen zwei im Transport befindlichen Kraftfahrzeugen darstellt, wird dies entsprechend klassifiziert.||
|RELJCT1|Die Codierung dieses Datenelements erfolgt in zwei Unterfeldern und basiert auf der Lage des ERSTEN SCHADENSVERURSACHENDEN EREIGNISSES des Unfalls. Es gibt an, ob der Unfallort in einem Interchange-Bereich liegt und ob er sich in der Nähe typischer Komponenten von Kreuzungs- oder Interchange-Bereichen befindet.||
|RELJCT2|Die Codierung dieses Datenelements erfolgt in zwei Unterfeldern und basiert auf der Lage des ERSTEN SCHADENSVERURSACHENDEN EREIGNISSES des Unfalls. Es gibt an, ob der Unfallort in einem Interchange-Bereich liegt und ob er sich in der Nähe typischer Komponenten von Kreuzungs- oder Interchange-Bereichen befindet.||
|TYP_INT|Dieses Element identifiziert und ermöglicht die Unterscheidung verschiedener Kreuzungstypen.|Der ausgewählte Wert sollte auf der Lage des ERSTEN SCHADENSVERURSACHENDEN EREIGNISSES basieren und gilt ausschließlich für Kreuzungs- bzw. kreuzungsbezogene Unfälle. Ist bekannt, dass ein kreisförmiger Kreuzungstyp beteiligt war, jedoch unklar, ob es sich um einen 05 (Verkehrskreis) oder einen 06 (Roundabout) handelt, so ist standardmäßig 05 (Verkehrskreis) zu wählen. Unter „Kreuzung“ versteht man einen Bereich, der 1) einen Übergang oder eine Verbindung von zwei oder mehr Straßen (nicht als Einfahrten klassifiziert) umfasst und 2) von den Verlängerungen der seitlichen Bordsteinkanten oder, falls nicht vorhanden, von den seitlichen Begrenzungslinien der Straßen eingeschlossen wird. Liegt der Abstand zwischen zwei solchen Bereichen entlang der Straße unter 33 Fuß, werden beide Bereiche sowie die sie verbindende Straße als eine einzige Kreuzung betrachtet. (Siehe ANSI D.16 - 2.5.10)|
|REL_ROAD|Dieses Element identifiziert den Unfallort in Bezug auf seine Position innerhalb oder außerhalb der Fahrbahn, basierend auf dem ERSTEN SCHADENSVERURSACHENDEN EREIGNIS.||
|WRK_ZONE|Dieses Datenelement erfasst, dass es sich um einen "Work Zone Crash" handelt, wie in ANSI D16.1, 8. Auflage, definiert. Falls der Unfall als Work Zone Crash qualifiziert, wird der Typ der Arbeitstätigkeit erfasst.|Falls der Unfall ein Work Zone Crash ist, muss der Work-Zone-Typ im Fallmaterial eindeutig erkennbar sein; andernfalls ist 4 (Work Zone, Typ unbekannt) zu verwenden. Die Verwendung dieser Codes impliziert nicht, dass der Unfall durch Bau-, Wartungs- oder Versorgungsarbeiten verursacht wurde.|
|LGT_COND|Dieses Element erfasst die Art bzw. das Niveau der Beleuchtung, die zum Zeitpunkt des Unfalls laut Fallmaterial vorhanden war.||
|WEATHER|Dieses Element erfasst die vorherrschenden atmosphärischen Bedingungen, die zum Zeitpunkt des Unfalls laut Polizeibericht bestanden.|Falls im Fallmaterial eine Kombination der genannten Zustände (z. B. Clear/Cloudy, Clear or Cloudy, Sleet/Hail/Freezing Rain, Snow/Sleet/Hail) angegeben wird und nicht eindeutig ermittelt werden kann, welche Bedingung vorherrschte, codieren Sie 98 (Nicht gemeldet). Temperatur gilt nicht als atmosphärische Bedingung. Regen, Schneeregen oder Schnee dürfen nicht automatisch als „Cloudy“ interpretiert werden – „Cloudy“ muss explizit im Fallmaterial genannt sein.|
|SCH_BUS|Dieses Datenelement gibt an, ob ein Schulbus oder ein als Schulbus eingesetztes Kraftfahrzeug mit dem Unfall in Verbindung steht.||
|RAIL|Dieses Element gibt an, ob der Unfall an oder in der Nähe eines Bahnübergangs stattfand.||
|NOT_HOUR|Dieses Element gibt die Uhrzeit an, zu der die erste EMS-Einheit, die am Einsatzort eintraf, benachrichtigt wurde.||
|NOT_MIN|Dieses Element erfasst die Minute, in der die erste EMS-Einheit, die am Einsatzort eintraf, benachrichtigt wurde.||
|ARR_HOUR|Dieses Element gibt die Uhrzeit an, zu der die erste EMS-Einheit am Unfallort eintraf.||
|ARR_MIN|Dieses Element erfasst die Minute, in der die erste EMS-Einheit am Unfallort eintraf.||
|HOSP_HR|Dieses Element gibt die Uhrzeit an, zu der der Rettungsdienst am Behandlungsort (Krankenhaus, Klinik, Traumazentrum etc.) eintraf, wohin das am schwersten verletzte Unfallopfer transportiert wurde.||
|HOSP_MN|Dieses Element erfasst die Minute, in der der Rettungsdienst am Behandlungsort (Krankenhaus, Klinik, Traumazentrum etc.) eintraf, wohin das am schwersten verletzte Unfallopfer transportiert wurde.||
# cevent.csv
| Spaltenname  | Beschreibung | Bemerkung |
|:-:|:-:|-|
|STATE|||
| STATENAME    |              |           |
| ST_CASE      |              |           |
| EVENTNUM     |              | Dies ist eine computergenerierte Nummer, die mit „001“ beginnt. Die Ereignisnummer(n) zeigt die chronologische Abfolge der qualifizierten schädlichen und nicht-schädlichen Ereignisse des Unfalls. Qualifizierte Ereignisse sind solche, die ein im Transport befindliches Kraftfahrzeug oder ein durch ein im Transport befindliches Kraftfahrzeug in Bewegung gesetztes Objekt betreffen. Im RBIS entspricht dies der Zeilenposition und wird nicht als Spalte in der Eingabetabelle angezeigt. |
| VNUMBER1     |              | Geben Sie die Nummer des im Transport befindlichen Kraftfahrzeugs ein, das mit dem Ereignis in der Spalte „SEQUENCE OF EVENTS“ der Crash Events Table verknüpft ist. Fahrzeugen wird die Fahrzeugnummer aus dem polizeilichen Unfallbericht zugewiesen, es sei denn, im Fall wird keine Fahrzeugnummer aus dem polizeilichen Unfallbericht verwendet (z. B. bei einem Fahrzeug ohne Kontakt). Siehe den Kodierleitfaden: Crash Events Table, Vehicle Placement für hilfreiche Informationen. |
| AOI1         |              | Kennzeichnet den Kontaktpunkt (falls zutreffend) für das in „Vehicle Number (This Vehicle)“ codierte Fahrzeug, das mit diesem Ereignis verknüpft ist. Handelt es sich um einen Zusammenstoß, codieren Sie den Wert, der den Aufprallbereich identifiziert oder anzeigt, dass dieses Fahrzeug ein Objekt in Bewegung gesetzt hat. Bei einem schädlichen Ereignis ohne Zusammenstoß verwenden Sie das Attribut 00 (Kein Zusammenstoß). Bei einem nicht-schädlichen Ereignis wird kein Wert für „AREAS OF IMPACT (This Vehicle)“ eingegeben. Dieses Feld verwendet dieselben Werte und Bemerkungen wie das Datenfeld auf Fahrzeugebene AREAS OF IMPACT—Initial Contact Point. Das Datenfeld wird aus der Crash Events Table abgeleitet und ist immer der erste aufgezeichnete AREA OF IMPACT-Wert für jedes Fahrzeug in der Tabelle. Siehe den Kodierleitfaden: Fahrzeugkomponenten und Aufprallbereiche für hilfreiche Informationen. |
| AOI1NAME     |              |           |
| SOE          |              | Dieses Datenelement wird aus der Crash Events Table abgeleitet. Die Erfassung der Unfallereignisse endet beim letzten schädlichen Ereignis des gesamten Unfalls. Daher wird ein nicht-schädliches Ereignis (z. B. das Überqueren der Mittellinie), das nach dem letzten schädlichen Ereignis auftritt, nicht berücksichtigt. Korrekturen der Reihenfolge der SEQUENCE OF EVENTS müssen durch eine Überarbeitung der Crash Events Table vorgenommen werden. Dieses Feld verwendet dieselben Werte und Bemerkungen wie das Datenfeld auf Fahrzeugebene SEQUENCE OF EVENTS. |
| SOENAME      |              |           |
| VNUMBER2     |              | Identifiziert die Fahrzeugnummer des Fahrzeugs, mit dem das in „Vehicle Number (This Vehicle)“ erfasste im Transport befindliche Kraftfahrzeug in Kontakt kam. Dieses Feld ist nur anwendbar, wenn es sich um einen Zusammenstoß zwischen zwei Kraftfahrzeugen handelt (d. h. SEQUENCE OF EVENTS-Codes 12, 54, 55, 14 oder 45). Falls es sich nicht um einen Zusammenstoß zwischen zwei Kraftfahrzeugen handelt, bleibt Vehicle Number (Other Vehicle) leer. Siehe den Kodierleitfaden: Crash Events Table, Vehicle Placement für hilfreiche Informationen. |
| VNUMBER2NAME |              |           |
| AOI2         |              | Kennzeichnet den Kontaktpunkt für das in „Vehicle Number (Other Vehicle)“ codierte Fahrzeug, das mit diesem Ereignis verknüpft ist. Falls es sich nicht um einen Zusammenstoß zwischen zwei Kraftfahrzeugen handelt, ist AOI (Other Vehicle) nicht anwendbar und bleibt leer. Dieses Feld verwendet dieselben Werte wie das Datenfeld auf Fahrzeugebene AREAS OF IMPACT—Initial Contact Point. Das Datenfeld wird aus der Crash Events Table abgeleitet und ist immer der erste aufgezeichnete AREA OF IMPACT-Wert für jedes Fahrzeug in der Tabelle. Siehe den Kodierleitfaden: Fahrzeugkomponenten und Aufprallbereiche für hilfreiche Informationen. |
| AOI2NAME     |              |           |

# crashrf.csv
| Spaltenname  | Beschreibung | Bemerkung |
|:-:|:-:|-|
| STATE        |              |           |
| STATENAME        |              |           |
| ST_CASE        |              |           |
|CRASHRF|This element identifies factors related to the crash expressed in the case material.|Code information provided in the case material.|
|CRASHRFNAME|              |           |

# damage.csv
| Spaltenname  | Beschreibung | Bemerkung |
|:-:|:-:|-|
|STATE|              |           |
|STATENAME|              |           |
|ST_CASE|              |           |
|VEH_NO|              |           |
|DAMAGE|This subfield identifies the area on this vehicle that produced the first instance of injury to non-motorists or occupants of this vehicle, or that resulted in the first instance of damage to other property or to this vehicle. This subfield identifies all the areas on this vehicle that were damaged in the crash as reflected in the case material by the officer.| If AREAS OF IMPACT- INITIAL CONTACT POINT / DAMAGED AREAS are provided on the crash report in this exact format, use the values from the report unless there are clear errors (e.g., officer switches vehicles by mistake). If these elements are not provided on the crash report in this exact format, then similar report fields, narrative, or diagram information may be used to code these elements. These subfields do not refer to direction of force of the impact. They identify the area(s) on the vehicle associated with the initial contact (Subfield 1) and all damage to the vehicle identified in the case material (Subfield 2).|
|DAMAGENAME|||

# distract.csv
| Spaltenname  | Beschreibung | Bemerkung |
|:-:|:-:|-|
|STATE|              |           |
|STATENAME|              |           |
|ST_CASE|              |           |
|VEH_NO|              |           |
|DRDISTRACT|This element identifies the attribute(s) that best describes this driver’s attention to driving
prior to the driver’s realization of an impending critical event or just prior to impact if realization of an
impending critical event does not occur. This element reports on the presence of any distractions that
may or may not have contributed to the crash. Distraction from the primary task of driving occurs when
drivers divert their attention from the driving task to some other activity. Also, driving while
daydreaming or lost in thought is identified as distracted driving by NHTSA. Physical
conditions/impairments (fatigue, alcohol, medical condition, etc.) or psychological states (anger,
emotional, depressed, etc.) are not identified as distractions by NHTSA.|DRIVER DISTRACTED BY is a “Select All That Apply” element. If the element values 00 (Not Distracted),
16 (No Driver Present), 17 (Distraction/ Inattention), 18 (Distraction/Careless), 19
(Careless/Inattentive), 92 (Distraction (Distracted), Details Unknown), 93 (Inattention (Inattentive),
Details Unknown), 96 (Not Reported), or 99 (Reported as Unknown if Distracted) are selected, then
only that one element value may be used.|
|DRDISTRACTNAME|||
# drimpair.csv
| Spaltenname  | Beschreibung | Bemerkung |
|:-:|:-:|-|
|STATE|              |           |
|STATENAME|              |           |
|ST_CASE|              |           |
|VEH_NO|              |           |
|DRIMPAIR|This element identifies physical impairments to this driver or non-motorist that may have
contributed to the cause of the crash as identified by law enforcement.|Select all that apply. These impairments can appear anywhere in the case material (in the
narrative section, in the violations section, in a column entitled “Contributing Factors,” or “Driver
Action,” etc.). See clarification on the use of information provided by witnesses in section 103. Data
Sources.|
|DRIMPAIRNAME|              |           |
# driverrf.csv
| Spaltenname  | Beschreibung | Bemerkung |
|:-:|:-:|-|
|STATE|              |           |
|STATENAME|              |           |
|ST_CASE|              |           |
|VEH_NO|              |           |
|DRIVERRF|This element identifies factors related to this driver expressed in the case material.|Code information provided in the case material. This is a nominal list only and does NOT imply
a hierarchy.|
|DRIVERRFNAME|              |           |
# drugs.csv
| Spaltenname  | Beschreibung | Bemerkung |
|:-:|:-:|-|
|STATE|              |           |
|STATENAME|              |           |
|ST_CASE|              |           |
|VEH_NO|              |           |
|PER_NO|              |           |
|DRUGSPEC|Definition for Drug Test Status: This element identifies if a chemical test for the presence of drugs was
given to this person.
Definition for Drug Specimen: This element identifies the bodily tissue or fluid used to perform a
chemical test for the presence of drugs in this person.
Definition for Drug Test Result: This element records the result of a chemical test for the presence of
drugs in this person.|This element’s values and remarks are identical to the Person (MV Occupant) Level element
DRUG TOXICOLOGY RESULTS. Please see DRUG TOXICOLOGY RESULTS for remarks.
See Alphabetical Drug Index and Drugs by Category under element DRUG TOXICOLOGY RESULTS. Also
reference “Examples for Interpreting Drug Tests” under element DRUG TOXICOLOGY RESULTS.|
|DRUGSPECNAME|              |           |
|DRUGRES|Definition for Drug Test Status: This element identifies if a chemical test for the presence of drugs was
given to this person.
Definition for Drug Specimen: This element identifies the bodily tissue or fluid used to perform a
chemical test for the presence of drugs in this person.
Definition for Drug Test Result: This element records the result of a chemical test for the presence of
drugs in this person.|This element’s values and remarks are identical to the Person (MV Occupant) Level element
DRUG TOXICOLOGY RESULTS. Please see DRUG TOXICOLOGY RESULTS for remarks.
See Alphabetical Drug Index and Drugs by Category under element DRUG TOXICOLOGY RESULTS. Also
reference “Examples for Interpreting Drug Tests” under element DRUG TOXICOLOGY RESULTS.|
|DRUGRESNAME|              |           |
# factor.csv

# maneuever.csv

# maneuever.csv

# MIACC.CSV

# MIDRVACC.CSV

# MIPER.CSV

# nmcrash.csv

# nmdistract.csv

# nmimpair.csv

# nmprior.csv

# parkwork.csv

# pbtype.csv

# person.csv

# personrf.csv

# pvehiclesf.csv

# race.csv

# safetyeq.csv

# vehicle.csv

# vehiclesf.csv

# vevent.csv

# violatn.csv

# vision.csv

# vpicdecode.csv

# vpictrailerdecode.csv

# vsoe.csv

# weather.csv