# Door-Opener
Autmatic Door Opener

Install:
- copy the files from epoch.mission into your mission file (if init.sqf already exist, paste the code into this file)
- Add the following lines to the and of this file: "epoch.mission\epoch_config\Configs\CfgActionMenu\CfgActionMenu_self.hpp"
class Ignatz_DoorOpener
{
	condition = "if (dyna_AtHome && dyna_IsDriver) then {['opencheck'] call Ignatz_Client_DoorOpener} else {false};";
	action = "['open'] call Ignatz_Client_DoorOpener;";
	icon = "addons\pics\Actions\Gate_Open.paa";
	tooltip = "Open Gate";
};
class Ignatz_DoorCloser
{
	condition = "if (dyna_AtHome && dyna_IsDriver) then {['closecheck'] call Ignatz_Client_DoorOpener} else {false};";
	action = "['close'] call Ignatz_Client_DoorOpener;";
	icon = "addons\pics\Actions\Gate_Close.paa";
	tooltip = "Close Gate";
};


Only for EPOCH 1.0:
- Add this: https://github.com/EpochModTeam/Epoch/commit/2fe4b0ff969ea468cd5600fb86becee215eca5a0
