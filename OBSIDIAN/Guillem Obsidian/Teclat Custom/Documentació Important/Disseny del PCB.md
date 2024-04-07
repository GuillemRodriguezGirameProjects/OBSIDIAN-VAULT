## Coses a tenir en consideració

En quant al disseny del PCB s'ha de tenir en compte s'han de tenir en consideració les següents parts del PCB.

>[!note] OJUT!
>TODO: mirar el com s'ha de fer perquè el disseny del PCB serveixi també per l'altre banda del PCB al moment de girar-lo al fer l'altre meitat.
>
>En teoria no hi hauria d'haver molts problemes si es fa servir ThroughHoleSoldering en comptes de SurfaceMountSoldering però hehe, mai se sap.

### Parts del PCB

**Matriu de switches:** La matriu de Switches i el com es connecten al controlador

**Controllador:** El controllador s'ha de soldar al PCB ja sigui directament o amb Sockets per poder reutilitzar-lo després

**Power Switch:** una palanca que permet encendre i apagar el PCB. 
	En el Power Switch hi ha 3 potes:
		1- La pota 1 és la que li ha d'entrar el corrent. És l'Input del Switch. Aquesta pota ha de rebre el negatiu de la Bateria
		2 i 3 -  Les potes 2 i 3 són les potes que es connecten amb la 1 depenent de l'estat del switch. Cap de les dues té una funcionalitat dedicada així que es pot fer servir qualsevol de les 2 per tot el que es necessiti.
		En aquest cas el que es necessita és que una de les potes estigui connectada a GND per així tancar el circuit i que l'altre no estigui connectada a res per poder tenir el circuit del PCB obert i així tenir el teclat apagat.

		En el meu cas faré servir el Pin 2 com a GND i el Pin 3 el deixaré intacte.

**Reset Button:** Un botó que fa que el MicroController es resetegi.
	 S'ha de connectar la Pota GND a GND i l'altre pota al Reset del MicroController.

**Pins de la Bateria:** Per poder reutilitzar la Bateria necessitem connectar-la amb uns pins al PCB. Aquests poden estar en qualsevol lloc del PCB però s'ha de tenir en compte quin Pin es connectará al Positiu de la Batería i quin al Negatiu. 

### OPCIONALS
Pantalla OLED: Es pot instal·lar una pantalla OLED per poder veure informació del MicroController, com la connexió actual, la Layer, el percentatge de bateria i més.
	La Pantalla Oled ha de connectar-se en la sortida de Voltatge del MicroController per poder funcionar.
	Després la info del MicroController s'envia amb dos dels pins que es triin del Controller. Aquests pins té pinta que s'han de triar utilitzant el Firmware. Així que en el meu cas ZMK.
