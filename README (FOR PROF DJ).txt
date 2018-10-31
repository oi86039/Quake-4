DOOM 2016 Gameplay Mod - by Omar Ilyas

	Deliverable List (for easy grading)
		Complete:
		-- Modify Player movement
		-- Enemies Drop pickups on death
		-- Glory Kill System - increase gibs when attacking with melee
		-- Berserk Powerup
		
		Incomplete:
		-- Weapon Attachment system
		-- Double Jump (Part of Modify Player Movement)

	-All Completed Deliverables
		-- Modify Player Movement (excluding Double Jump)
			
			TO TEST:
				Use WASD to move the character and spacebar to jump. You'll notice they move much faster than previously, and can no longer take fall damage.
				
			Changes:	
				Player speed was increased to 300 (previously 160)
				Walk and Crouch speed were increased to 140 (previously 80)
				Jump Height increased to 96 (previously 48)
				Fall Damage was 'effectively' removed. It is still calculated, but the height needed to register damage cannot be achieved without noclip.
			
		-- Enemies Drop pickups on death
			
			TO TEST:
				Kill any ememy of choice and look at their death location. You will see a set assortment of items that range from a health pack to ammo packs. The items can then be grabed and applied to your player character.
				
				Changes:
					Whenever an AI entity dies, a random integer value is generated. That random value is then used to determine what items will drop from an enemy upon death.
						99% chance of spawning a small health pack
						50% chance of spawning an armor shard
						40% chance of spawning 1 clip of machinegun ammo and 1 clip of shotgun ammo
		
		-- Glory Kill System - increase gibs when attacking with melee
	
			TO TEST:
				Using the gauntlet, kill a StroggMarine (the very first enemy in the game is a StroggMarine), or attack a dead StroggMarine corpse. If performed correctly, the body will explode with a huge blood effect and spawn more gibs than normal (about 15-20 gibs). There may also be a bit of lag when an enemy explodes into blood. 
				
				(This deliverable is best tested using the beserk powerup (see below), as gauntlet attacks always gib StroggMarines immediately with beserk enabled)
				
				Changes:
					Removed the if statement within Actor.cpp that stops gibbing if an enemy has been gibbed once. This creates the giant blood effect and the lag effect when an enemy is gibbed, as the method doesn't stop until the enemy stops being hit by the player.
					Added multiple Gib spawn lines to spawnArgs when gibs are called.
					There is a chance to have weapons also gib enemies, but range weapons typically don't do enough damage to an ememy to gib them. Meleeing enemies is the most reliable way to gib.
	
		-- Berserk Powerup
		
			TO TEST:
				Use Ctrl+Alt+~ to open the console in game. Once in the console, type the command "give beserk" (excluding quotes) and press enter, then escape the console by pressing Esc twice. You'll notice a timer on the far right of the screen; this indicates that the powerup is working!
				To test its effects, kill any ememy using the gauntlet while beserk is active. They will immediately be gibbed upon being attacked! Guns are 'effectively' useless while beserk is equipped, but the gauntlet is 'effectively' a oneshot kill for all enemies!
				
				(--It is best to test this powerup last, as there is a powerup glitch that prevents powerups from being turned off, even after the timer runs out. This keep the powerup effect of almost no weapon damage while keeping the one-shot gauntlet damage in effect. These changes will be applied unless the game is reloaded to a save where the the powerup is not active.)
		
			Changes:
				Added a new powerup to Player.def and Player.h labeled Powerup_Beserk.
				Copied the methods of quad damage and renamed them to fit with beserk instead.
				Altered the properties of the copied method so that melee damage was 999f and projectile damage was 0.00001f.
					Thus, projectiles are 'effectively' useless as they still do damage, but too little to have an effect.
		
	-Incomplete Deliverables
		-- Weapon Attachment system
		-- Double Jump (Part of Modify Player Movement)
			- Remenants of Double Jump code are in the Player.cpp and Physics_Player.cpp files, but they are non-functional.