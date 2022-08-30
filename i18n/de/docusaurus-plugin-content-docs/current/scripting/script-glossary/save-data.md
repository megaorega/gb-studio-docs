---
sidebar_position: 2
#
# This file is autogenerated. DO NOT MODIFY DIRECTLY
#
---

import ScriptEventPreview from '@site/src/components/ScriptEventPreview';

# Speichere Daten

## Spieldaten: Laden
Load the saved game data from the selected slot.
<ScriptEventPreview title={"Spieldaten: Laden"} fields={[{"label":"Spieldaten aus dem Speicher laden."},{"key":"saveSlot","label":"Speichere Slot","description":"The save slot to use.","type":"togglebuttons","options":[[0,"Slot 1","Speichere Slot 1"],[1,"Slot 2","Speichere Slot 2"],[2,"Slot 3","Speichere Slot 3"]],"allowNone":false,"defaultValue":0}]} />

- **Speichere Slot**: The save slot to use.  

## Spieldaten: Löschen
Remove any previously saved game data in the selected slot.
<ScriptEventPreview title={"Spieldaten: Löschen"} fields={[{"label":"Löscht alle gespeicherten Spieldaten aus dem Speicher."},{"key":"saveSlot","label":"Speichere Slot","description":"The save slot to use.","type":"togglebuttons","options":[[0,"Slot 1","Speichere Slot 1"],[1,"Slot 2","Speichere Slot 2"],[2,"Slot 3","Speichere Slot 3"]],"allowNone":false,"defaultValue":0}]} />

- **Speichere Slot**: The save slot to use.  

## Spieldaten: Speichern
Save the current game data into the selected slot.
<ScriptEventPreview title={"Spieldaten: Speichern"} fields={[{"label":"Speichert die aktuellen Spieldaten im Speicher. Benötigt Modultyp mit BATTERIE."},{"key":"saveSlot","label":"Speichere Slot","description":"The save slot to use.","type":"togglebuttons","options":[[0,"Slot 1","Speichere Slot 1"],[1,"Slot 2","Speichere Slot 2"],[2,"Slot 3","Speichere Slot 3"]],"allowNone":false,"defaultValue":0},{"key":"__scriptTabs","type":"tabs","defaultValue":"save","values":{"save":"Beim Speichern"}},{"key":"true","label":"Beim Speichern","description":"A script to run after the save is completed. This won't be run on game load so you can use it show a 'Save Was Successful' message.","type":"events"}]} />

- **Speichere Slot**: The save slot to use.  
- **Beim Speichern**: A script to run after the save is completed. This won't be run on game load so you can use it show a 'Save Was Successful' message.  

## Falls Spieldaten Gespeichert
Conditionally run part of the script if save data is present within the specified save slot.
<ScriptEventPreview title={"Falls Spieldaten Gespeichert"} fields={[{"key":"saveSlot","label":"Speichere Slot","description":"The save slot to use.","type":"togglebuttons","options":[[0,"Slot 1","Speichere Slot 1"],[1,"Slot 2","Speichere Slot 2"],[2,"Slot 3","Speichere Slot 3"]],"allowNone":false,"defaultValue":0},{"label":"Ausführen, falls der Spieler ein Spiel gespeichert hat."},{"key":"true","label":"Wahr","description":"The script to run if the condition is true.","type":"events"},{"key":"__collapseElse","label":"Andernfalls","type":"collapsable","defaultValue":true,"conditions":[{"key":"__disableElse","ne":true}]},{"key":"false","label":"Falsch","description":"The script to run if the condition is false.","conditions":[{"key":"__collapseElse","ne":true},{"key":"__disableElse","ne":true}],"type":"events"}]} />

- **Speichere Slot**: The save slot to use.  
- **Wahr**: The script to run if the condition is true.  
- **Falsch**: The script to run if the condition is false.  

## Variable aus Spieldaten in Variable speichern
Read a variable's value from a specified save slot and store it in a variable.
<ScriptEventPreview title={"Variable aus Spieldaten in Variable speichern"} fields={[{"key":"variableDest","label":"Variable festlegen","description":"The variable to update.","type":"variable","defaultValue":"LAST_VARIABLE"},{"type":"group","fields":[{"key":"variableSource","label":"Zu Variable","description":"The variable to read the value of.","type":"variable","defaultValue":"LAST_VARIABLE"},{"key":"saveSlot","label":"Von Speicher Slot","description":"The save slot to use.","type":"togglebuttons","options":[[0,"Slot 1","Speichere Slot 1"],[1,"Slot 2","Speichere Slot 2"],[2,"Slot 3","Speichere Slot 3"]],"allowNone":false,"defaultValue":0}]}]} />

- **Variable festlegen**: The variable to update.  
- **Zu Variable**: The variable to read the value of.  
- **Von Speicher Slot**: The save slot to use.  
