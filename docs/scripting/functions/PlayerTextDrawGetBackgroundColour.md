---
title: PlayerTextDrawGetBackgroundColour
description: Gets the background colour of a player-textdraw
tags: ["player", "textdraw", "playertextdraw"]
---

<VersionWarn name='feature (player-textdraws)' version='omp v1.1.0.2612' />

## Description

Gets the background colour of a player-textdraw

| Name     | Description                                             |
| -------- | ------------------------------------------------------- |
| playerid | The ID of the player |
| PlayerText:textid | The ID of the player textdraw to get the background colour of |

## Returns

Returns the background colour of the player-textdraw.

## Examples

```c
new PlayerText:pTextdraw[MAX_PLAYERS];

public OnPlayerConnect(playerid)
{
    pTextdraw[playerid] = CreatePlayerTextDraw(playerid, x, y, "...");
    PlayerTextDrawSetOutline(playerid, pTextdraw[playerid], 1);
    PlayerTextDrawBackgroundColour(playerid, pTextdraw[playerid], 0x00FF00FF);
    PlayerTextDrawShow(playerid, pTextdraw[playerid]);

    new backgroundColour = PlayerTextDrawGetBackgroundColour(playerid, pTextdraw[playerid]);
    // the `backgroundColour` will be 0x00FF00FF
    return 1;
}
```

## Related Functions

- [CreatePlayerTextDraw](CreatePlayerTextDraw): Create a player-textdraw.
- [PlayerTextDrawDestroy](PlayerTextDrawDestroy): Destroy a player-textdraw.
- [PlayerTextDrawBoxColour](PlayerTextDrawBoxColour): Set the colour of a player-textdraw's box.
- [PlayerTextDrawBackgroundColour](PlayerTextDrawBackgroundColour): Set the background colour of a player-textdraw.
- [PlayerTextDrawAlignment](PlayerTextDrawAlignment): Set the alignment of a player-textdraw.
- [PlayerTextDrawFont](PlayerTextDrawFont): Set the font of a player-textdraw.
- [PlayerTextDrawLetterSize](PlayerTextDrawLetterSize): Set the letter size of the text in a player-textdraw.
- [PlayerTextDrawTextSize](PlayerTextDrawTextSize): Set the size of a player-textdraw box (or clickable area for PlayerTextDrawSetSelectable).
- [PlayerTextDrawSetOutline](PlayerTextDrawSetOutline): Toggle the outline on a player-textdraw.
- [PlayerTextDrawSetShadow](PlayerTextDrawSetShadow): Set the shadow on a player-textdraw.
- [PlayerTextDrawSetProportional](PlayerTextDrawSetProportional): Scale the text spacing in a player-textdraw to a proportional ratio.
- [PlayerTextDrawUseBox](PlayerTextDrawUseBox): Toggle the box on a player-textdraw.
- [PlayerTextDrawSetString](PlayerTextDrawSetString): Set the text of a player-textdraw.
- [PlayerTextDrawShow](PlayerTextDrawShow): Show a player-textdraw.
- [PlayerTextDrawHide](PlayerTextDrawHide): Hide a player-textdraw.
