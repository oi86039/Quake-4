DOOM 2016 Gameplay Mod
	-Deliverables
		** Modify Player Movement (in progress)
		** Double Jump
		** Berserk Mode
		** Enemies Drop pickups on death
		** Glory Kill System
		** Weapon Attachment system
		
Main deliverables to be graded are marked with two asterisks (**)
		
9/22/18 - Modify Player Movement and Weapon Feel
	- pak022.pk4
		** player.def 
			** Jump height changed to 96 (was 48)
			** Normal speed changed to 250 (was 160)
			** Walk and Crouch speed changed to 140 (was 80)
			
			- Maximum health changed to 250 (was 100)
			- Default weapons set to All Weapons (was Blaster)
			- Starting ammo for all weapons set to < MaxAmmo/2 (was 0)

		- shotgun.def
			- Removed reloading; Clip size changed to 0 (was 8)
			- Recoil increased; Recoil Time set to 1100 (was 600)
		- machinegun.def
			- Damage set to 30 (was 18)
			- Zoomed damage set to 50/60 (was 20/24)
			- Zoom time set to 0.5 (was .1)
			- Fire rate changed to 0.15 (was .1)
			- Spread changed to 5 (was .2)
			- Removed reloading; Clip size changed to 0 (was 8)
			- Recoil increased; Recoil Time set to 250 (was 145)
			- Zoom time set to .3 (was .1)
			- Low ammor indicator triggers at 20 (was 10)
			- Bullet push increased to 57500 (was 7500)

			
	- pack001.pk4
		- blaster.def
			- Firerate changed to .30 (was .15)
			- Charge color set to 0 6 (was 0 .4)
			- Spread changed to 20 (was .2)
			- Recoil increased; Recoil Time set to 300 (was 100)
			- Charge Time set to 3.8 (was .8)
			- Uncharged Damage set to 
			- Charge Shot Velocity set to 4000 (was 2000)
			- Charge Splash Knockback set to 5000 (was 30)
			
	--10/9/18
		- Gauntlet.def
			- Changed gauntlet damage from 50 to 200.
			- Changed deathpush from 200 to 200000. (Enemies explode when killed)
		- Player.def
			- Equipped Gauntlet, Blaster, MachineGun and Shotgun as starting weapons
		-GLORY KILL DELIVERABLE NEARLY COMPLETE