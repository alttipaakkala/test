Tehtävä: Uusi salt demoni

Aluksi asennetaan nethack käsin ja asennuksen jälkeen se poistetaan.

	sudo apt-get update
	sudo apt get install nethack
	sudo apt purge nethack

Luodaan kansio /srv/salt hakemistoon ja kansioon luodaan uusi tiedosto 
init.sls
	mkdir nethack
	sudoedit init.sls

Muokataan init.sls tiedostoa 

	nethack:
	 pkg.installed 

Ja asennetaan demoni 

	sudo salt '*' state.apply nethack


