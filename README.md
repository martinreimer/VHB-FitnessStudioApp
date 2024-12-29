# Mitglieder- und Kursverwaltung für Fitnessstudios

## Projektbeschreibung

### Projektziele

Die App soll die Verwaltungsarbeit eines Premium-Fitnessstudio-Betreibers erleichtern. Premium-Fitnessstudios bieten ihren Mitgliedern wöchentlich verschiedene Kurse an, die seit der Corona-Pandemie hohen Verwaltungsaufwand erfordern. Denn während vor der Pandemie die Kursräume auch überfüllt sein durften und alle Mitglieder ohne vorherige Anmeldung an Kursen teilnehmen konnten, ist die Kursteilnahme jetzt auf eine bestimmte Teilnehmeranzahl zur Einhaltung von Abstandsregeln begrenzt und eine Anmeldung zum Kurs wurde wegen der Nachvollziehbarkeit von Infektionsketten zur Pflicht. Die App ermöglicht es den Betreibern, ihren Wochen-Kursplan zu verwalten und weitere nützliche Infos zu ihrem Studio wie Trainerinfos oder die Anfahrtsbeschreibung bereitzustellen. Für Mitglieder des Studios bietet die App eine einfache und übersichtliche Möglichkeit, Infos zum Studio einzusehen und sich zu Kursen an- oder abzumelden.

#### Wesentliche Funktionen der App
##### Registrierung/Login
Die Benutzer melden sich mit der Rolle Admin/Trainer oder der Rolle Mitglied an der App an

![image](https://user-images.githubusercontent.com/99557936/159299311-adbd84a9-c161-4005-9c64-7285065e8472.png)
##### Hauptmenü
Je nach Rolle des angemeldeten Benutzers werden die entsprechenden Menüpunkte angezeigt

![image](https://user-images.githubusercontent.com/99557936/159300670-6d5ebef4-74b8-47ae-b3f1-16521007e1ed.png)


##### Pflege des Wochen-Kursplans
Die Übersicht der Kurse wird auf einem Tabbed Screen mit Wochentagen angezeigt. Pro Wochentag wird der Zeitplan dargestellt:

![image](https://user-images.githubusercontent.com/99557936/159299513-a0de9b32-4523-475e-8380-2aff85da6159.png)

Die Detailansicht der Kurse dient zur Einsicht von Kursdaten und zum Pflegen eines Kurses:

![image](https://user-images.githubusercontent.com/99557936/159299583-011d8a60-6b90-4452-a4bb-4d20c57665f3.png)
##### Buchen/Stornieren von Kursen
Die Übersicht der anstehenden Kurse mit farblich hervorgehobenen gebuchten Kursen ist auf einer Kalender-Ansicht zu finden:

![image](https://user-images.githubusercontent.com/99557936/159300020-52a1c7e0-271b-41eb-99af-ec36cc2ae234.png)

In der Detailansicht eines Kalender-Events kann ein Kurs gebucht oder eine Buchung storniert werden:

![image](https://user-images.githubusercontent.com/99557936/159301009-8e6de63b-cfef-4628-9895-b27b61b8bfc8.png)
##### Pflege von Studio-Kontaktinformationen
![image](https://user-images.githubusercontent.com/99557936/159300162-e06ed071-fda1-4c3d-a5fd-0afefff5c7a9.png)
##### Einsicht von Studio-Kontaktinformationen
![image](https://user-images.githubusercontent.com/99557936/159501508-1181ca45-63d4-4e0a-910b-c03ad9155a55.png)
##### Pflege und Einsicht von Trainern
Auf einer Übersichtsseite werden alle Trainer in Listenform dargestellt.

![image](https://user-images.githubusercontent.com/99557936/159300236-0ee32a04-af6a-4238-a461-2ecccfc76bec.png)

Auf der Detailansicht sind die Lizenzen, Aus- und Fortbildungen der Trainer zu finden:

![image](https://user-images.githubusercontent.com/99557936/159300284-45068b5f-7e53-4230-bf45-2ef6068b9282.png)
##### Pflege und Einsicht von Mitgliedern

Auf einer Übersichtsseite werden alle Mitglieder in Listenform dargestellt.

![image](https://user-images.githubusercontent.com/99557936/159300332-65b8e571-57c3-41f6-99ac-0ad2b4535bca.png)

Auf der Detailansicht können Kontaktdaten eingesehen und bearbeitet werden.

![image](https://user-images.githubusercontent.com/99557936/159300395-8d7b9a86-c2bb-4eae-be2e-cc9d21f08ee4.png)
  
#### Hinweise zur Inbetriebnahme der App
##### Datenbank
Die App beihaltet eine lokale Room-Datenbank. Zur Inbetriebnahme der App müsste eine zentrale Datenbank angebunden werden, auf die jeder angemeldete Benutzer zugreift, um den aktuellen Stand vom Kurswochenplan, von Buchungen, Mitgliedern, Trainern und deren Profilbildern zu erhalten. Es wurde außerdem auf die Validierungsfunktion einer Buchung verzichtet, d.h. zur Inbetriebnahme müsste geprüft werden, ob noch Kursplätze verfügbar sind oder der Kurs bereits ausgebucht ist. In vielen Studios gibt es außerdem die Möglichkeit, sich bei ausgebuchten Kursen auf die Warteliste setzen zu lassen. Das könnte über einen weiteren Buchungsstatus erweitert werden.
##### Registrierung
Die App beinhaltet keinerlei Verifikation der Email-Adresse oder eines gültigen Mitglieds- oder Trainer-Accounts. Zur Inbetriebnahme müsste die App um einen Bestätigungslink per Email und um die Genehmigung einer neuen Registrierung durch den Studiobetreiber oder berechtigte Benutzer erweitert werden.
###### Ausblick
Weitere Funktionen, die für einen Live-Betrieb der App wünschenswert wären, sind:
- Die Möglichkeit, dass Trainer nicht nur die Anzahl der Buchungen für einen Kurs, sondern auch die angemeldeten Benutzer einsehen können.
- Funktionen für eine bessere Vermarktung des Studios, z.B. über Bereiche zum Hochladen von Bildern und Videos oder bevorstehende Veranstaltungen.
- Einsicht von Preis- und Leistungsinformationen des Studios.

#### Kompilierbarkeit
Um einen kompilierbaren Clone der App zu erhalten, sind folgende Eigenschaften zu beachten:
- API-Level: minSdk 26, targetSdk 31
- Android Studio Default JDK Version: 11.0.11
- Android Studio Version: Android Studio Bumblebee | 2021.1.1 Patch 2
- Damit die Google-Map-Komponente verwendet werden kann, ist der API-KEY im local.properties-File folgendermaßen zu ergänzen:
  ```
  MAPS_API_KEY=AIzaSyBRKAuXtcb5S3yeIeQrM3pkUacBD9vuLik
  ```
#### Ausführbare Datei
Die APK-Datei zur App ist [hier](fitnessstudio.apk) zu finden.

### Projektvorgehen
Das Projekt wurde vollständig in einem eigenen Github-Repository entwickelt. Die wesentlichen Commits wurden zur Veranschaulichung in dieses Class-Room-Repository projiziert.
Im initialen Projekt-Kick-Off-Meeting wurden die Vorgehensweise für unser Projekt sowie die wesentlichen Funktionen, die die App erhalten soll, gemeinsam definert und in einer Meilenstein-/Terminplanung über Github-Project verwaltet:

  ![image](https://user-images.githubusercontent.com/99557936/159285114-187d698a-402e-4bf9-bf98-93b9c23bb2e4.png)
  
![mockups_img](https://user-images.githubusercontent.com/99968798/159904490-25d2e893-4b8d-446d-9458-f9ce8bdb34a0.png)
![classdiagramm](https://user-images.githubusercontent.com/99968798/159904575-87a0e763-9197-4409-8441-cd5276e7e8b1.png)

Nach der Erstellung von Mockups- und Klassendiagrammen wurde in einer weiteren gemeinsamen Besprechung die Aufgabenaufteilung festgelegt.
Für die Entwicklung der App wurde ein Kanban-Board benutzt, auf dem die einzelnen Funktionen der App in Tasks aufteilt wurden.

![image](https://user-images.githubusercontent.com/99557936/159286128-6ff360ac-246d-4fe5-9aca-c43732416746.png)

In weiteren wöchentlichen MS-Teams-Meetings wurden Fortschritt, Probleme und weiteres Vorgehen besprochen.  

### Funktionen
#### Übersicht der Aufwandspunkte nach Anforderungskatalog 
|Feature-Beschreibung                         |Kategorie              |Aufwand      |beschrieben in Funktion(en)                          |
|---------------------------------------------|-----------------------|-------------|-----------------------------------------------------|
|Daten verschlüsselt speichern                |Sicherheit             |1            |[Registrierung](#funktion-registrierung)             |
|Wiederverwendbare Layoutbausteine: Fragments |User Interface         |1            |[Kurse buchen](#funktion-kurse-buchen)              |
|Shared Preferences persistieren              |Persistenz             |1            |[Studio-Kontaktinformationen pflegen](#funktion-studio-kontaktinformationen-pflegen)       |
|Intents mit Payload                          |Kommunikation (intern) | 1           |[Registrierung](#funktion-registrierung), [Kursplan pflegen](#funktion-kursplan-pflegen)       |
|Tabbing (Swipe to change screen)             |User Interface         |1            |[Kursplan pflegen](#funktion-kursplan-pflegen)       |
|Nebenläufige Aktionen                        |Software-Engineering   |2            |alle Datenbankoperationen, [Studio-Kontaktinformationen einsehen](#funktion-studio-kontaktinformationen-pflegen)|
|Notification                                 |User Interface         |1            |[Kurse buchen](#funktion-kurse-buchen)               |
|Datenbank auf dem Gerät                      |Persistenz             |2            |[Registrierung](#funktion-registrierung),[Kursplan pflegen](#funktion-kursplan-pflegen),[Trainer pflegen](#funktion-trainer-pflegen),[Mitglieder verwalten](#funktion-mitglieder-verwalten)|
|Eigener Adapter                              |Software-Engineering   |2            |[Mitglieder verwalten](#funktion-mitglieder-verwalten),[Trainer pflegen](#funktion-trainer-pflegen),[Kursplan pflegen](#funktion-kursplan-pflegen)       |
|Service für längere Hintergrundaufgaben      |Software-Engineering   |2            |[Kurse buchen](#funktion-kurse-buchen)                              |
|Map-Komponente dynamisch/interaktiv          |User Interface         |3            |[Studio-Kontaktinformationen einsehen](#funktion-studio-kontaktinformationen-pflegen)|
|Fingerabdruck-Login für App                  |Sensoren               |3            |[Anmeldung](#funktion-anmeldung)                     |

#### Funktion: Anmeldung
Grundsätzlich bestehen zwei Möglichkeiten des Logins über die [LoginActivity]( app/src/main/java/app/fitnessstudio/login/LoginActivity.java). Zum einen der normale Weg über Eingabe von E-Mail-Adresse und Passwort als Identifier und zum anderen der Weg über den Fingerabdruck Login:

##### Normale Eingabe 
Die hier angezeigten Eingabefelder sind mit einem TextChangeListener ausgestattet, ohne den der inaktiv geschaltete „Einloggen“-Button nicht zu benutzen ist. Nach ausfüllen der benötigten Felder kann eine Anfrage über den jetzt aktiven Button gestellt werden. Um unnötige Datenbankabfragen zu verhindern, durchlaufen die Benutzereingaben eine Vorabüberprüfung auf die passende Form (Mail-Adressen Format). Da die Userpasswörter in verschlüsselter Form in der Datenbank hinterlegt sich, ist ein weiterer Punkt im Ablauf des Prozesses das Hashen des Passwortes mit Hilfe der tohash() Funktion des [HashHelper](app/src/main/java/app/fitnessstudio/HashHelper.java).
Wurde der User in der Datenbank gefunden, wird seine ID und Rolle in den SharedPreferences gespeichert und je nach gefundener Rolle die passende Activity gestartet. Das hat den Grund das späteren Datenbankoperationen die ID des Nutzers benutzen können, ohne diese diese per Intent Extra weiterreichen zu müssen. Ist die Userrolle als „member“ hinterlegt wird per Intent die [MemberMainActivity](app/src/main/java/app/fitnessstudio/MemberMainActivity.java) gestartet. Entspricht die Rolle „admin“, gelangt der User in die mit mehr Rechten und Menüpunkten ausgestattet [AdminMainActivity](app/src/main/java/app/fitnessstudio/AdminMainActivity.java). Hat der User falsche Logindaten verwendet wird ihm dies über einen Toast mitgeteilt.

##### Fingerabdruck Login
Um den Fingerabdruck Login benutzen zu können muss diese Option zunächst im Einstellungen Menüpunkt in der [SettingsActivity](app/src/main/java/app/fitnessstudio/settings/SettingsActivity.java) aktiviert werden und in den SharedPreferences hinterlegt. Beim nächsten Aufrufen der Login Activity wird diese Information von dort abgefragt. Ein BiometricManager prüft, ob die entsprechende Hardware im Device des Benutzers vorhanden ist und zeigt den Button im Interface an. Hat der Benutzer die Benutzung aktiviert und verfügt über die entsprechende Hardware, wird der Button angezeigt. Die BiometricPrompt Klasse verwaltet alle Funktionen des Fingerabdrucksensors. Es zeigt den selbst mit Text ausstattbaren Authentifizierungsdialog und gleicht den gescannten Fingerabdruck mit dem im System Hinterlegten ab. Wie beim normalen Login wird anschließend die Rolle und ID aus den SharedPreferences ausgelesen und entsprechende Activities über einen Intent gestartet. 

![Element 16](https://user-images.githubusercontent.com/99582898/160103692-5cda471c-1d84-4e4b-ac1a-b8a69aad6294.png)


#### Funktion: Registrierung 
##### Erster Registrierungsschritt
Der Registrierungsprozess besteht aus drei Activities, in denen vom User Angaben zu seiner Person verlangt werden. 

In der [FirstStepRegisterActivity](app/src/main/java/app/fitnessstudio/login/FirstStepRegisterActivity.java) muss jedes Eingabefeld ausgefüllt werden, um sicherzustellen das möglichst vollständige Datensätze der Benutzer in die Datenbank eingefügt werden können. Dies wird durch einen TextChangeListener realisiert, der nach jeder Eingabe das komplette Formular auf Vollständigkeit prüft und in diesem Fall den „Fortfahren“ Button aktiv schaltet. Wird dieser Button betätigt startet die Eingabevalidierung und Felder wie die E-Mail-Adresse werden mittels einer Pattermatcher Funktion aus der Libary auf eine ihre Grundform überprüft. Aus Sicherheitsgründen wird die Passworteingabe mittels des inputType=„TextPassword“ verdeckt angezeigt, kann jedoch bei Bedarf über das Augensymbol an der linken Seite sichtbar gemacht werden. Ebenfalls der Sicherheit wegen muss der User sein Passwort wiederholen und kann nur mit einer mindestlänge von 5 Zeichen fortfahren. Die Eingabe des Geburtsdatums erfolgt durch den übliche DatePickerDialog. 

![Element 12](https://user-images.githubusercontent.com/99582898/160093510-743abbd2-b192-4191-aecf-05c509910951.png)

##### Zweiter Registrierungsschritt
Die Funktionen in der [SecondStepRegisterActivity](app/src/main/java/app/fitnessstudio/login/SecondStepRegisterActivity.java) gleichen im Wesentlichen denen des Ersten. Ein kleines Dropdown Menü, das durch einen AutoCompleteTextView in Verbindung mit einem ArrayAdapter implementiert wurde, lässt den User sich eine Rolle zuweisen. Im Hintergrund wurden die Userdaten durch einen mit Extra beladenen Intent weitergegeben, zwischengespeichert und in gleicher Weise an die letzte Registrierungsaktivity weitergegeben.

![Element 15](https://user-images.githubusercontent.com/99582898/160093658-94e55ab9-42eb-47f3-8ae2-6009cac775d2.png)

##### Dritter Registrierungsschritt
Hier in der [ThirdStepRegisterActivity](app/src/main/java/app/fitnessstudio/login/ThirdStepRegisterActivity.java) werden aus Usabiliygründen alle, durch die Intents weitergegebenen, Informationen des Users erneut angezeigt, um sie vom User auf ihre Korrektheit zu prüfen. Ist der User einverstanden, kann er die Registrierung durch den Button abschließen. Hier bei wird mit Hilfe, der von unserem DatabaseHelper bereitgestellten Funktionen die User, entsprechend ihrer ausgewählten Rolle, als Member bzw Admin erstellt, in die Datenbank geschrieben und die entsprechende Hauptmenüaktivity per Intent gestartet. 

![Element 13](https://user-images.githubusercontent.com/99582898/160093725-25774d0f-8065-4195-85da-86f819f213c3.png)


##### Verschlüsseltes Speichern
Um die Passwörter nicht als Klartext in die Datenbank schreiben zu müssen, wird vor der Übergabe des Passwortstrings dieser mittels [HashHelper](app/src/main/java/app/fitnessstudio/HashHelper.java)-Klasse verschlüsselt. Diese produziert mit dem Secure Hash Algorithmus (SHA-512) aus einer Zeichenkette einen 64-Byte-Hashwert.


#### Rolle Trainer/Admin
##### Funktion: Kursplan pflegen
Für die Verwaltung des Wochen-Kursplans wurde eine Tabbed Activity erstellt.
Die [CourseActivity](app/src/main/java/app/fitnessstudio/coursemanagement/course/CourseActivity.java) benutzt den View [activity_course.xml](app/src/main/res/layout/activity_course.xml) und kümmert sich mithilfe des [SectionsPagerAdapters](app/src/main/java/app/fitnessstudio/coursemanagement/course/SectionsPagerAdapter.java) um die Anzeige der Tabreiter. Die Tab-Überschriften werden über einen Array im [Ressource String File](app/src/main/res/values/strings.xml) mit den Wochentagen Montag bis Sonntag befüllt. 
Pro Tabreiter wird ein Zeitplan angezeigt, welcher im [DayViewFragment](app/src/main/java/app/fitnessstudio/coursemanagement/course/DayViewFragment.java) mithilfe der öffentlichen Github-Library Android-Week-View (com.github.quivr:android-week-view:2.3.3) realisiert wurde. 

![image](https://user-images.githubusercontent.com/99557936/159491089-3fa4dabe-3de6-4d5f-84f1-06d9aae7953a.png)

Zum Hinzufügen eines neuen Kurses kann der Plus-Button betätigt werden, der zur Activity [CourseAddActivity](app/src/main/java/app/fitnessstudio/coursemanagement/course/CourseAddActivity.java) führt. Die Detailansicht des Kurses wurde im wiederverwendbaren Layoutbaustein [activity_course_details_view.xml](app/src/main/res/layout/activity_course_details_view.xml) definiert. Alternativ zum Plus-Button kann ein Long-Click auf einen leeren Bereich im Zeitplan gemacht werden, welcher die Uhrzeit in der Detailansicht mit dem angeklickten Zeitpunkt vorbefüllt. 
In der Kurs-Detailansicht können nun alle relevanten Felder befüllt werden. Dazu gehören der Kursname, Beschreibung, Start-Uhrzeit, Dauer, Trainer, Location und die maximale Teilnehmerzahl. Alle Felder sind Pflichtfelder und werden beim Speichern des Kurses validiert. Zur Auswahl des Start-Zeitpunkts kann über Long-Click in das Feld ein Zeitwähler geöffnet werden. Die Trainer können über einen Spinner, der als View und Dropdown-View [list_array_adapter.xml](app/src/main/res/layout/list_array_adapter.xml) anzeigt, der über den eigenen Adapter [CoachArrayAdapter](app/src/main/java/app/fitnessstudio/coach/CoachArrayAdapter.java) realisiert ist, ausgewählt werden. Außerdem kann ein Gültigkeitsdatum des Kurses festgelegt werden. Bei Long-Click wird ein Datumswähler-Dialog angezeigt. So kann der Stundenplan im Voraus zum Beispiel für das nächste Quartal gepflegt werden, ohne dass die aktuellen Kurse verändert werden müssen(bis auf das gültig-bis Datum). Zum Speichern des Kurses ist im Action-Menü ein Speichern-Button verfügbar. Beim Speichern wird der Kurs über den nebenläufigen Task [AddCourseTask](app/src/main/java/app/fitnessstudio/database/tasks/course/AddCourseTask.java) in der Datenbank persistiert.

![image](https://user-images.githubusercontent.com/99557936/159490799-ee0597bd-264b-45fd-894b-52e81ebdcbf6.png)

Wird in der Kurs-Plan-Ansicht ein bestehender Kurs angeklickt so wird ein Intent mit den Kursinformationen als Payload zur Activity [CourseEditActivity](app/src/main/java/app/fitnessstudio/coursemanagement/course/CourseEditActivity.java) gestartet. Die Activity benutzt denselben Layoutbaustein [activity_course_details_view.xml](app/src/main/res/layout/activity_course_details_view.xml) zur Detailansicht der Kurse. Im Action-Menü werden Buttons zum Speichern und zum Löschen des Kurses angezeigt. Beim Löschen wird der Kurs über den nebenläufigen Task [DeleteCourseTask](app/src/main/java/app/fitnessstudio/database/tasks/course/DeleteCourseTask.java) aus der Datenbank entfernt, zum Speichern wird der nebenläufigen Task [UpdateCourseTask](app/src/main/java/app/fitnessstudio/database/tasks/course/UpdateCourseTask.java) verwendet.
Ansonsten arbeitet die Activity mithilfe der [CourseHelper](app/src/main/java/app/fitnessstudio/coursemanagement/course/CourseHelper.java)-Klasse mit denselben Funktionen wie die [CourseAddActivity](app/src/main/java/app/fitnessstudio/coursemanagement/course/CourseAddActivity.java).

##### Funktion: Studio-Kontaktinformationen pflegen
Die Informationen über den Betrieb eines Fitnessstudios bleiben nicht für immer gleich, bespielsweise können sich die Öffnungszeiten häufig ändern. Diese Informationen müssen für den Administrator veränderbar sein, ohne dass die ganze App geupdated werden muss. Daher haben wir die [ContactInfoManagerActivity](app/src/main/java/app/fitnessstudio/contact_info/ContactInfoManagerActivity.java) (XML: [activity_manage_contact_info.xml](app/src/main/res/layout/activity_manage_contact_info.xml)) entwickelt. Der Administrator kann darauf über den "Kontakt Manager"-Button im Menü zugreifen. Der Admin kann dort den Namen des Studios, die Addresse, die E-Mail, die Nummer und die Öffnungszeiten einstellen. Diese Werte werden zunächst validiert und nach erfolgreicher Validierung im Preference Manager im <key, value> Format abgespeichert. Falls keine Werte vom Admin eingestellt werden, werden Default Werte verwendet, welche im [Ressource String File](app/src/main/res/values/strings.xml) gespeichert sind.

##### Funktion: Trainer pflegen
Die Trainerliste wird über die Activity [CoachListActivity](app/src/main/java/app/fitnessstudio/coach/CoachListActivity.java), den zugehörigen eigenen Adapter [CoachArrayAdapter](app/src/main/java/app/fitnessstudio/coach/CoachArrayAdapter.java) und den XML-View [list_array_adapter.xml](app/src/main/res/layout/list_array_adapter.xml) realisiert.

![image](https://user-images.githubusercontent.com/99557936/159496655-14b0ee72-bea8-458d-83c9-80fa5e634f20.png)

Über einen Klick auf ein List-Item gelangt der Benutzer in die Trainer-Detailansicht [CoachDetailsActivity](app/src/main/java/app/fitnessstudio/coach/CoachDetailsActivity.java) mit zugehörigem XML-View [activity_coach_details_view.xml](app/src/main/res/layout/activity_coach_details_view.xml).
Zur selben Activity wir den Benutzer über den Plus-Button geleitet.
In der Detailansicht des Trainers kann der Benutzer den Namen und die Beschreibung wie Lizenzen oder Ausbildungsstand des Trainers pflegen. Über den Kamera-Button kann ein Profilbild hinterlegt werden.

![image](https://user-images.githubusercontent.com/99557936/159498580-a1b40830-203e-40ed-aa0e-3a75bc6415a8.png)

- Mit der Option "Foto machen" wird die Kamera-App gestartet und der Benutzer kann ein neues Foto schießen. Dazu wurde ein File-Provider im 
[Manifest](app/src/main/AndroidManifest.xml) definiert und der Bilder-Pfad im [XML-Resource-File](app/src/main/res/xml/provider_paths.xml) hinterlegt. Die URI zum Profilbild-Pfad wird in der Trainer-Datenbanktabelle abgespeichert.
- Mit der Option "Foto aus Galerie wählen" kann der Benutzer ein Foto aus der Galerie hochladen. Die URI wird ebenso in der Trainer-Datenbanktabelle abgespeichert, womit das Profilbild beim nächsten Start der App und auch in der Listenansicht der Trainer wieder in ein Bitmap umgewandelt wird.
##### Funktion: Mitglieder verwalten
Mitglieder werden in der Datenbank angelegt, indem sich die Mitglieder selber registrieren. Der Administrator benötigt die Möglichkeit die registrierten Mitglieder zu verwalten. Zum Beispiel soll er die Möglichkeit haben Mitglieder aus der Datenbank entfernen zu können, die nicht für das Studio bezahlen oder die Hausverbot haben. Außerdem sollte er zum Beispiel die Adresse eines Mitglieds ändern können, falls sich diese ändern sollte. Um diese Funktionalität anbieten zu können wurden folgende Klassen mit XML-Darstellung erstellt: 
  - die [MembersListActivity](app/src/main/java/app/fitnessstudio/member/MembersListActivity.java) (XML: [activity_members_list.xml](app/src/main/res/layout/activity_members_list.xml)) um alle Mitglieder für den Admin aufzulisten. Alle Mitglieder werden als ListArray aus einer Datenbankabfrage geholt und mit Hilfe des MembersArrayAdapter dargestellt.
  - der [MembersArrayAdapter](app/src/main/java/app/fitnessstudio/member/MembersArrayAdapter.java) (XML: [list_array_adapter.xml](app/src/main/res/layout/list_array_adapter.xml)) um vorzugeben, wie jedes Mitglied in der Auflistung als View dargestellt werden soll.
  - die [MemberDetailsView](app/src/main/java/app/fitnessstudio/member/MemberDetailsView.java) (XML: [activity_member_details_view.xml](app/src/main/res/layout/activity_member_details_view.xml)) um ein Mitglied in Einzelansicht darzustellen. Hier können einzelne Daten eines Mitglieds vom Admin nach Validierung dieser verändert werden und das Mitglied kann von hier aus auch entfernt werden.

#### Rolle Mitglied
##### Funktion: Kursplan anzeigen
Ist ein Benutzer mit der Rolle Mitglied angemeldet, werden dieselben Activities und XML-Views wie in [Funktion: Kursplan pflegen](#funktion-kursplan-pflegen) im Read-Only-Modus verwendet:

![image](https://user-images.githubusercontent.com/99557936/159491924-f6b4a5be-a716-4b98-b5fa-e2030b03b70e.png)
![image](https://user-images.githubusercontent.com/99557936/159868090-e86ef00a-b07e-4c5e-be3c-dd88243eca28.png)
##### Funktion: Kurse buchen
Die Activity [BookingActivity](app/src/main/java/app/fitnessstudio/coursemanagement/booking/BookingActivity.java) zeigt den XML-View [activity_booking.xml](app/src/main/res/layout/activity_booking.xml), welcher die Android-Week-View beinhaltet. Diese zeigt eine Kalendersicht im Wochenformat und beinhaltet alle anstehenden Kurse eine Woche im Voraus als Events des Android-Week-Views. 

![image](https://user-images.githubusercontent.com/99557936/159492827-e556df62-26de-4be9-af94-31a205f1ee3e.png)

Beim Klick auf ein Event wird die Kurs-Detailansicht über das Fragment [BookingFragment](app/src/main/java/app/fitnessstudio/coursemanagement/booking/BookingFragment.java) mit dem wiederverwendbaren Layoutbaustein [activity_course_details_view](app/src/main/res/layout/activity_course_details_view.xml) geöffnet und das Mitglied kann sich über den Action-Button zum Kurs anmelden. Daraufhin wird der Kurs in der Kalenderansicht farblich hervorgehoben. 
Vor Abspeichern des Kurses wird ein zufälliger numerischer requestCode erzeugt, mit dem in der [BookingActivity](app/src/main/java/app/fitnessstudio/coursemanagement/booking/BookingActivity.java) ein Alarm eine Stunde vor Kursbeginn gesetzt wird. Der Alarm bekommt als Parameter einen PendingIntent, der einen Broadcast auslöst. Bei Empfang des Broadcasts eine Stunde vor Kursbeginn startet der [BookingReminderReceiver](app/src/main/java/app/fitnessstudio/coursemanagement/booking/BookingReminderReceiver.java) den Service [BookingReminderService](app/src/main/java/app/fitnessstudio/coursemanagement/booking/BookingReminderService.java), welcher eine Notification auslöst. 

![image](https://user-images.githubusercontent.com/99557936/159495757-ae963248-6d25-4d8e-a1d7-346fe84ffd15.png)

Der Kurs wird anschließend in der Datenbank mit der UserId und der requestId des Alarm-Services abgespeichert.
Mit Klick auf die Notification kann der Benutzer in die Kurs-Buchen-Ansicht wechseln.
Zum Abmelden von einem Kurs kann das Mitglied in einen gebuchten Kurs klicken und dort den Action-Button seine Buchung stornieren.
Die Buchung erhält den Status storniert in der Datenbank und über die requestId wird der laufende Alarm abgebrochen, so dass der Benutzer keine Notification eine Stunde vor Kursbeginn mehr für einen Kurs erhält, für den er nicht mehr eingebucht ist. 

##### Funktion: Trainereinsicht
Es werden dieselben Activities und XML-Views wie in [Funktion: Trainer pflegen](#funktion-trainer-pflegen) im Read-Only-Modus verwendet:

![image](https://user-images.githubusercontent.com/99557936/159500102-76f6e15c-7004-4ad1-9b0a-cfd94eb831b5.png)
![image](https://user-images.githubusercontent.com/99557936/159500129-b29d1ff2-4e9a-4940-bb42-90faebeeedfe.png)

##### Funktion: Mitgliedereinsicht
Das Mitglied erhält über das [Mitglieder Menü](app/src/main/java/app/fitnessstudio/MemberMainActivity.java) (XML: [activity_member_main.xml](app/src/main/res/layout/activity_member_main.xml)) eine kleine Ansicht über dessen Eigenschaften. Es wird zum einen der Vorname angezeigt und das Datum an dem sich das Mitglied registriert hat. Sollte das Mitglied seine Daten verändern oder sein Konto löschen wollen, müsste er sich an den Admin wenden.
##### Funktion: Studio-Kontaktinformationen einsehen
Über die [ContactInfoActivity](app/src/main/java/app/fitnessstudio/contact_info/ContactInfoActivity.java) (XML: [activity_contact_info.xml](app/src/main/res/layout/activity_contact_info.xml)) erhalten die Mitglieder Informationen über die Kontaktinformationen des Studios. Diese Informationen werden aus dem Preference Manager geladen. Sollte der Admin keine aktuellen Kontaktinformationen bereitstellen, werden Default Werte aus dem [Ressource String File](app/src/main/res/values/strings.xml) geladen.
Neben den aufgelisteten Informationen wurde auch eine Maps-Komponente in die Ansicht integriert. Diese Maps-Komponente zeigt die Adresse des Studios in einer Karte an. Die Karte beinhaltet einen Marker an der Studio-Adresse, welche über einen Background-Thread mit dem [GeocoderTask](app/src/main/java/app/fitnessstudio/maps/GeocoderTask.java) aufgelöst wird. Bei Klick auf die Infobox mit der Adresse wird Google Maps geöffnet und ein Routenplaner zum Studio gestartet. Klickt der Benutzer auf einen anderen Bereich in der Karte wird die Karte in einer neuen Full-Screen-Activity mit denselben Funktionen geöffnet (Activity [MapsActivity](app/src/main/java/app/fitnessstudio/maps/MapsActivity.java) mit XML-View [activity_maps.xml](app/src/main/res/layout/activity_maps.xml)). Diese Funktion soll es dem Mitglied ermöglichen schneller das Fitnessstudio zu finden.

### Demo

Wegen des Uploadlimits von 25 MB ist unser Präsentationsvideo hier zu finden: https://www.dropbox.com/s/6xjtch4rc33w5v7/AbgabevideoFitnessApp.mp4?dl=0

## Team

### Vorstellung

#### Lucas Schmieder
- Email-Adresse: lus8199@thi.de
- Github-Nutzername: LSchmieder
#### Martin Reimer
- Email-Adresse: Martin.Reimer@stud.uni-regensburg.de
- Github-Nutzername: martinur
#### Julia Strahberger
- Email-Adresse: julia.strahberger@stud.th-deg.de
- Github-Nutzername: Julia-Strahberger 

### Zuständigkeiten

#### Lucas Schmieder
- Mockups
- Splash Screen 
- Anmeldung/Registrierung
- Hauptmenüs
- Launcher-Icon
- App-Video
#### Martin Reimer
- Use Case Diagramm
- Klassendiagramm
- Fingerabdruck-Sensor
- Mitglieder-Verwaltung
- Kontaktverwaltung
- Shared Preferences
- Verschlüsselung von Passwörtern
#### Julia Strahberger
- Projektorganisation
- Kursverwaltung
- Kursbuchung
- Trainerverwaltung
- Profilbild-Upload
- Notification
- Google Map-Komponente

## Guidelines zur Nutzung dieses Repositorys

### Allgemeine Hinweise und Vorgaben

* Das Repository besteht im initialen Stand aus einem einzelnen Master-Branch. Versuchen Sie bei der Arbeit am Projekt darauf zu achten, dass sich in diesem Branch stets die aktuell lauffähige und fehlerfreie Version Ihrer Anwendung befindet. Nutzten Sie für die eigentliche Entwicklung ggf. weitere Branches.
* Gehen Sie sorgfältig bei der Erstellung von Issues und *Commit Messages* vor: Die Qualität dieser Artefakte fließt nicht in die Bewertung ein, trotzdem sollten Sie versuchen, Ihr Vorgehen anhand nachvollziehbarer Versionseinträge und klarere Aufgabenbeschreibung gut zu dokumentieren.
* Halten Sie diese Readme-Datei(en) stets aktuell.
* Diese sollte auch wichtige Informationen für die Nutzung beinhalten (Handbuch).
* Spätestens zur Projektabgabe legen Sie eine Release-Version des finalen Stands Ihrer Anwendung an und hängen an diese eine installierbare (Debug-) APK-Datei an.
* Achten Sie insbesondere darauf anzugeben, welches API-Level / NDK-Version ihrem Projekt zugrunde liegt und auf die 'Kompilierbarkeit' ihres finalen Codes.
