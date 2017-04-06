# Gestió de Volums Lògics

#### Descripció del que són:

El LMV (Gestor de volums lògics, Logical Volume Manager) és un sistema de particions independents de l'estructura subjacent del disc, amb el que es posible crear un espai d'emmagatzematge abstracte, així com particions virtuals, de manera que es més fàcil d'ampliar o disminuir particions.


#### Els tres blocs bàsics:

    - PV (Physical Volume) = Identificador de discs.
    - VG (Volume Group) = Discs virtuals.
    - LV (Logical Volume) = Particions.

#### Comandes:

    - pvs : Proporciona informació del volums físics. 
    - vgs : Proporciona informació dels volums de grup.
    - lvs : Proporciona informació dels volums lògics. 

#### Entorn de pràctiques:

Obrirem el programama virt-manager, crearem la maquina virtual, afegirem un hardware i tres discs virtuals de 200M que es dirán **dev/vda**, **dev/vdb**, **dev/vdc**.

##### Pràctica 1: Creació d'un volum lògic a partir d'un dels tres discs durs (vda per exemple). Aquest volum lògic ha de ser del total de capacitat del disc. El volum de grup s'ha de dir practica1 i el volum lògic dades.

    · Creació del volum lògic > vgcreate practica1 /dev/vda

    · Capacitat  total del volum lògic > lvcreate -L 100%FREE -n dades practica1

##### Pràctica 2: Creació d'un sistema de fitxers xfs al volum lògic creat i muntatge a /mnt. També s'ha de crear un fitxer amb dd de 180MB.

    · Creació del sistema de fitxers xfs >  mkfs.ext4 /dev/practica1/dades

    · Muntatge a /mnt >  mount /dev/practica1/dades /mnt

    · Creació fitxer de 180MB >  dd if=/dev/zero of=test.img bs=1k count=180000

##### Pràctica 3: Creació d'un RAID 1 als dos discos sobrants (vdb i vdc per exemple).

    · Creació d'un RAID 1 a /vdb i /vdc >  mdadm -- create /dev/md1 -level=1 --raid-devices=2 /dev/vdb /dev/vdc

##### Pràctica 4: Ampliació del volum lògic de dades al raid.

    · Ampliació del volum lògic de dades al raid >  lvextend -L +50M /dev/practica1/dades

##### Pràctica 5: Ampliació del sistema de fitxers xfs al tamany actual del volum lògic dades (s'ha de poder fer sense desmuntar-lo de /mnt ja que és xfs). Una vegada creat crearem un nou fitxer de 180M.

    · Ampliació del sistema de fitxers xfs al tamany actual del volum de dades >  xfs growfs /dev/practica1/dades
    
    ·Creació d'un nou fitxer de 180M >  dd if=/dev/zero of=test img bs=1k count=180000
