---
sidebar_position: 2
#
# This file is autogenerated. DO NOT MODIFY DIRECTLY
#
---

import ScriptEventPreview from '@site/src/components/ScriptEventPreview';

# Scene

## Escena: Cambiar escena
Transition to a new scene with player at a specified position and direction. A connection line will be drawn between the source of the event and the destination scene with an icon appearing at the destination position. It's possible to drag this icon around and between scenes to modify the event.
<ScriptEventPreview title={"Escena: Cambiar escena"} fields={[{"key":"sceneId","label":"Escena","description":"The scene to transition to.","type":"scene","defaultValue":"LAST_SCENE"},{"type":"group","fields":[{"key":"x","label":"X","description":"The initial player horizontal position in the new scene.","type":"number","min":0,"max":255,"defaultValue":0,"width":"50%"},{"key":"y","label":"Y","description":"The initial player vertical position in the new scene.","type":"number","min":0,"max":255,"defaultValue":0,"width":"50%"}]},{"key":"direction","label":"Dirección","description":"The initial player direction.","type":"direction","width":"50%","defaultValue":""},{"key":"fadeSpeed","label":"Velocidad para desvanecer","description":"The speed of the fade animation.","type":"fadeSpeed","defaultValue":"2","width":"50%"}]} />

- **Escena**: The scene to transition to.  
- **X**: The initial player horizontal position in the new scene.  
- **Y**: The initial player vertical position in the new scene.  
- **Dirección**: The initial player direction.  
- **Velocidad para desvanecer**: The speed of the fade animation.  

## Escena: Vaciar escena de pila
Remove all scenes from the scene stack without leaving the current scene.
<ScriptEventPreview title={"Escena: Vaciar escena de pila"} fields={[{"label":"Limpia la pila de los estados de escena guardados."}]} />


## Escena: Restaurar primera desde pila
Transition to the very first scene stored on the stack, for instance if you had multiple levels of menu scenes you could use this to imediately return to the game scene. This event will cause the scene stack to become empty.
<ScriptEventPreview title={"Escena: Restaurar primera desde pila"} fields={[{"label":"Saca todos los estados de escena de la pila."},{"type":"break"},{"key":"fadeSpeed","label":"Velocidad para desvanecer","description":"The speed of the fade animation.","type":"fadeSpeed","defaultValue":"2","width":"50%"}]} />

- **Velocidad para desvanecer**: The speed of the fade animation.  

## Escena: Restaurar previa desde pila
Transition to the last stored scene from the scene stack using the specified fade speed. The previous scene will then be removed from the stack so the next time this event is used it will transition to the scene before that.
<ScriptEventPreview title={"Escena: Restaurar previa desde pila"} fields={[{"label":"Saca el estado de escena del tope de la pila."},{"type":"break"},{"key":"fadeSpeed","label":"Velocidad para desvanecer","description":"The speed of the fade animation.","type":"fadeSpeed","defaultValue":"2","width":"50%"}]} />

- **Velocidad para desvanecer**: The speed of the fade animation.  

## Escena: Guardar actual en pila
Store the current scene and player state on to the scene stack, this allows you to return to this exact location later using the Scene Restore events. A common use of this event would be to include in a script just before a Change Scene event to open a menu scene, in the menu scene you could wait for the player to press a close button and then use the Restore Previous From Stack event to return to where the player opened the menu.
<ScriptEventPreview title={"Escena: Guardar actual en pila"} fields={[{"label":"Empuja el estado de la escena a la pila."}]} />

