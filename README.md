# X-47m HUD
X-47m Custom HUD and flight controls 

OBSOLETE--CODE MADE OBSOLETE BY GAME CHANGES..SHIP WILL NOT BE RETAINED POST-WIPE

This site is for the distribution of the LUA code for the X-47m. The X-47m is a compactable pocket rocket for Dual Universe and is currently exclusively available to members of ChimerA. The cockpit and programming board DRM will be removed upon request to allow uprades or the use of a different HUD. It has been tested with ArchHud v1.4.11 running in 'cockpit' mode in place of the built-in custom HUD. See the ArchHud GitHub site for installation instructions. The code on this page will be the latest version of the custom fligth HUD and can be used to updgrade the ship code or replace it if you changed out the original HUD.  You can contact me on Discord at: KVeen#3678 if you have any questions. The flight controls here are intended specifically for the X-47m but could be adapted for any pocket rocket using a cockpit controller with a databank and programming board.

The X-47m is a highly maneuvarable compactable xs construct with a very low sustainment speed and a reasonable layer of voxel 'armor' to limit damage in collisions. It sacrifices some speed (may still exceeds 1400 for higher tier pilots, 1200 or mid-tier pilots) for extremely good handling at any speed and very good handling at very low speed (as in when you are landing in a high lag area). It has sufficient voxel to prevent most damage to key components during minor impacts and is survivable in impacts that would destroy many lighter pocket rockets AND has extremely overpowered airbrakes for its size. It is recommended to have the construct boosted and a fully boosted X-47m is flyable by any level of pilot with good performance. However, the hovers will be marginal for lower tier pilots on an unboosted (handling talents) X-47m. X-47m's can be boosted for free and DRM removed from the cockpit and programming board upon request. Contact KVeen#3678 for availability. 

Installation Instructions:
1) The X-47m has a programming board installed direclty behind the cockpit (see picture x47m02). Install the programming board code by viewing the 'programming board.json' file in 'raw' selecting all code and pasting into the programming board in game.
2) Do the same with the cockpit unit using the 'cockpit.json' code.

**Ship Instructions**

A current limitation with DU is that custom HUD's cannot be direclty used with cockpit controllers. However, by using an external programming board, normal flight HUDs designed for cockpit ships can be utilized in both first and third person view.

  1) The X-47m has a programming board installed directly behind the upper portion of the cockpit partially obscured in voxel (see x47m02 picture). 
  2) Prior to entering the cockpit, manually activate the programming board to start the HUD
  3) Enter the cockpit, the cockpit connects already to the HUD and displays flight information in first or third person view.
  4) Enjoy your flight!
  5) The programming board will automatically exit once you leave the cockpit so you will have to re-activate it manually before re-entering the cockpit.

NOTE: This limitation was removed with a recent update. The current cockpit LUA code will now generate the flight HUD without activating the programming board. Once updated, the PB is no longer neccessary

**Custom HUD features**

  1) Pressing 'G' when landed will auto-takeoff to maximum hover height for the pilot. Pressing G while in a hover will auto-land. A red indicator with current/max hover height will appear on the HUD whenever hoverheight is not 0. Using ctrl-space and ctrl-c will increment or decrement hover height setting
  2) The pitch and roll will automaticaly level to zero when you are below your set speed. The speeds for this are located in the LUA parameters and can be reset individually. By default pitch will auto level below 50kph, and roll will auto level below 200kph but these can be adjusted. Simply set them to zero to disable this feature. The pitch and roll bars on the HUD will turn blue and display 'Auto' when auto-leveling is engaged
  3) Alt-4 will toggle auto-stabilization and lock both pitch and roll to zero at any speed. The pilot may still maneuver the craft, but both pitch and roll will return to zero when controls are released. The pitch and roll bars turn red and display 'locked' when stabilization is toggled on.
  4) Alt-3 will engage roll stabilization (locked) and auto pitch to maintain a set altitude. The initial set altitude will be the altitude the constrcut is at when Alt-3 is pressed. The set altitude can be incremented or decremented with Alt-6 and Alt-7 once engaged and the craft will attempt to maintian that altitude. The maximum auto-pitch correction can be configured in the LUA parameters
  5) Alt-5 locks the brake. The X-47m has sufficient braking power to brake land on any planet with no damage to the craft if the hovers are engaged (ensure the red hover height indicator is present at the bottom of center HUD line). Pressing the brake key (ctrl by default) will engage the brake but not lock it.
  6) Alt-8 toggles between 3 cruise modes, normal mode is standard flight using the throttle, low speed cruise for slow flight, and max cruise for maximum speed flight. Both low speed and max speed cruise are configurable in LUA parameters. Cruise can be manually adjusted once set and cruise/travel modes can be toggled using the bound key on your keyboard as well.
  7) LUA parameters have adjustments for the placement of the fuel widget and both font and line width. While font and line will auto-scale for most displays, you can change the sizes to your preference as well as the transparency factor for the HUD in the LUA parameters.
