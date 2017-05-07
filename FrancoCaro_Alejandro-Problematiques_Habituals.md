# Problemàtiques Habituals

##### Descriu com arribes a aquestes conclusions (totes les possibilitats) en analitzar el comportament d'un ordinador:

###### Botón power on roto:
    1-Apretem el botó,però l'ordinador no encén.
    2-Amb un tester y comprovem que la fuente de alimentación tingui tensió, així comprovem que la placa funciona correctament.
    3-Obrim la placa i juntem els pins de la placa base, si va el problema es de del botó o dels cables que el conecten, si no va, el problema es de la placa base.
    4-Connectem la placa base a una altra caixa i funciona correctament.

###### Botón power on se queda clavado en ON:
    1-Apretem el botó amb l'ordinador encés però el botò no hi reacciona a l'ordre d'apagarse, o quan el botò es queda atrapat a la carcasa de la caixa.
    
###### Fuente rota del todo:
    1-Mirem si hi està tot conectat a l'ordinador i també si hi ha corrent, però no s'encén.
    
###### Fuente medio rota:
    1-Mirem si hi està tot conectat a l'ordinador i també si hi ha corrent, però s'apaga i es reinincia constantment, degut a tensió errònea, sobretensións o sobrecalentaments.
    
###### RAM mal puesta:
    1-A l'hora d'ininciar l'ordinador sonen 3 beeps de so que indiquen que hgi està mal posada la memòria RAM.
    2-Probem en un altre port de RAM si funciona.
    
###### RAM rota:
    1-1-A l'hora d'ininciar l'ordinador sonen 3 beeps de so que indiquen que hgi està mal posada la memòria RAM.
    2-Probem en un altre port de RAM si funciona.
    3-Probem una altra RAM en els diferents ports per veure si funcionen.
    
###### RAM medio rota: (unos KB mal)
    1-A l'hora d'ininciar l'ordinador sonen 3 beeps de so que indiquen que no hi ha memòria RAM.
    2-No detecta tot el tamany que correspón a la RAM.
    
###### Sin RAM:
    1-A l'hora d'ininciar l'ordinador sonen 3 beeps de so que indiquen que no hi ha memòria RAM.
    
###### Gráfica pinchada rota:
    1-Comprovar que la pantalla no hi estgui negre i s'encengui.
    2-Conectar una pantalla diferent a l'ordinador.
    3-Canviar la gráfica.
    
###### CPU rota/ no hay CPU/chipset roto:
    1-Apretem el botó per encendre l'ordinador, però si no hi encén no hi ha CPU/chipset, està mal posada al módul, o no funciona.
    
###### Placa rota:
    1-Mirem Si Arrenca el pc. 
    2-Mirar si li arriba corrent amb un tester.
    3-Mirar si els pins del socket estàn bé.
    4-Mirar si el conector de Power ATX esta fet malbé.
    5-Mirar si el conector de Ventilador esta ben conectat.
    5-Mirar si conectem al panel posterior coses si les detecta (ja sigui ports usb, audio etc...)
    6-Sino cambiem la placa.
    
###### Placa medio rota:
    1-Mirem si arrenca el pc. 
    2-Fem comprovacions de temperatura etc.. 
    3-Si tot funciona bé quan connectem coses a la placa, ja sigui SATA , RAM , CPU.
    4-Si detecta dispositius interns i externs etc..
    5-Sino cambiem la placa.
    
###### Teclado roto: Depende de la configuración de la BIOS (halt on all errors:All but keyboard).
    1-Iniciem l'ordenador i el teclat no s'ilumina ni funciona quan teclegem.
    2-Comprovem que el cable està correctament endollat a placa o via Buetooth, i cambiar-lo de port USB, si segueix sense funcionar el teclat funciona malament. 
    4-Normalment la BIOS mana un missatge de que el teclat no està conectado o no el detecta.
    5-Intentem entrar a la BIOS però no podem encara que prenem la tecla correcta. 
    6-Connectem un altre teclat i veiem que funciona perfectament.
    
###### Falta ratón: No se queja.
    1-Mirem si esta ben conectat al port USB.
    2-Mirem si li falten els drivers perquè funcioni i si segueix sense anar.
    3-Mirem si es plug and play o si el laser del ratoli esta fet malbé.
    4-Sino funciona connectem un altre ratolí.
    
###### Falla CD/DVD: No se queja.
    1-Provar amb un altre cd/dvd.
    1-Mirem si esta conectat a la placa el connector SATA/IDE.
    3-Si el connector de la font està ben conectat.
    4-Mirem si els drivers estàn ben instalats i si la detecta el sistema.
    5-Cambiem la disquetera.
    
    Falta Disco Duro/Disco sin formatear: Hará pitido POST OK. Mensaje de SYSTEM NOT FOUND.
##### PRIMERA POSIBILITAT:
    1-Arrenquem amb una live iso del Gparted i veiem que no detecta cap disc.
    2-Obrim la caixa i veiem que no hi ha cap disc dur.
    3-Arranquem amb una live iso del Gparted i veiem que el disc dur està buit.
##### SEGONA POSIBILITAT:
    4-La màquina s’encén però no acaba d’arrencar, el que fem és obrir l’ordinador i comprovar que estigui tot ben connectat (el cable SATA a la placa o al Disc dur).
    5-Un cop comprovat ens donem compte de que el disc dur és nou per tant no està formatejat, la solució és fer un sistema de fitxers en aquest disc de nou.
    
###### BIOS mal flasheada: No arranca. No hay problema en el caso DUAL BIOS.
    1-Mirar que surt per pantalla i reinstalar la BIOS resetejarla amb els Jumper, els pins de la placa referents a la BIOS.
    
###### Disco duro con error SMART: Error POST. Hard drive SMART error. Permite omitir el error.
#####  PRIMERA POSIBILITAT:
    1-Arrenquem amb una live/iso del Gparted i veiem que no detecta cap disc.
    2-Obrim la caixa i veiem que no hi ha cap disc dur.
    3-Arrenquem amb una live/iso del Gparted i veiem que el disc dur està buit.
##### SEGONA POSIBILITAT:
    4-Amb el Hirens Boot cd fer un test del disc. 
    5-Si està fet malbé el que s'ha de fer és guardar totes les dades (backup) i canviar aquest disc per un de nou.
    
###### Pantalla rota/cable roto: Arranca con normalidad.
    1-Arranquem l'ordinador, sona el beeps (xiulets) de POST i el teclat i el ratolí s'iluminen, però no veiem res a la pantalla.
    2-Comprovem que el cable de vídeo estigui en bon estat i ben connectat canviant-ho per un altre.
    3-Comprovem si el cable de la pantalla està en bon estat, si està ben endollat, o si al monitor li arriba electricitat.
    4-Canviem la pantalla, o el cable de vídeo o d'electricitat per uns altres.
    
###### USB del frontal cruzado: Puede quemar la placa. Puede quemar los pendrive.
    1-El PC no detecta l'USB, obrim la caixa i comprovem que tots els cables estiguin ben connectats. 
    2-Ens donem compte de que el cable que connecta amb l'USB frontal està creuat, s’ha de tornar ha restablir de nou al seu lloc correctament.

######  USB del frontal conectado mal en placa (otro conector que no es USB): Quema los pendrive (sobrevoltaje).
    1-El PC no detecta l'USB, obrim la capsa i mirem a la placa la qual ens donem compte de que els cables estàn malament col·locats als pins, els connectem al seu lloc.
    
###### Pila de la BIOS esgotada
    1-Quan reiniciem la màquina, veiem que l'hora ni la data és la que hauria de ser.
    2-Entrem a la BIOS per canviar-la però al sortir no ens ha guardat els canvis.
    3-Canviar la pila esgotada de la BIOS.
    4-Canviar de nou l'hora i la data de manera que quedi actualitzada i la mostri correctament.
