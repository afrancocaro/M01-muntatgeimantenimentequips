# Tallafocs
#### Què es un sistema tallafocs? Quina és la seva finalitat?

Es un sistema que proporciona seguretat de xarxa mitjançant el filtrat del tràfic d'entrada i sortida basat en un conjunt de regles definides per l'usuari. La seva finalitat és la de reduir o eliminar la concurréncia de les comunicacións de xarxa no desitjats al temps que permet tota la comunicació legítima flueixi lliurement.
#### Quines generacions de tallafocs hi ha hagut i què millorava cadascun?
1. Filtrat de paquets: Permeten o denegen els paquets basats en portades dels paquets individuals.
2. Filtrat amb estat: Determinen l'estat de la conexió del paquets.
3. Filtrat d'aplicació (sense estat): Permeten o denegen els paquets basats en portades dels paquets individuals.

#### Quines capes té el model OSI?

7. Aplicació
6. Presentació
5. Sessió
4. Transport 
3. Xarxa
2. Enllaç de dades
1. Física

#### Quines capes té el model TCP/IP? En aquest cas feu una breu descripció de les funcionalitats de cada capa.

4. Aplicació: Nivell que els programes més habituals utilitzen per comunicar-se amb la xarxa.
3. Transport: Soluciona problemes com la fiabilitat i seguretat, que les dades arribin al destí i que ho fagin en l'ordre correcte.
2. Internet: Soluciona els problemes de transportar paquets a una xarxa.
1. Accés al medi: S'utilitza per passar paquets de la capa d'internet d'un dispositiu a la capa internet d'un altre.

#### A quina capa/capes sol treballar tradicionalment un tallafocs?

Un tallafocs sol treballar des de la capa 3 (Transport) fins a la capa 4 (Aplicació) del model TCP/IP.

## Tallafocs Linux

#### Busqueu quins són els tradicionals sistemes de tallafocs incorporats en linux i anomeneu-los.

- firewalld
- iptables

#### Quins dels anteriors tallafocs estan instal.lats al fedora de classe? Com ho comproveu?

Els dos hi estan instal·lats per defecte al Linux i, per tant, estan instal·lats al Fedora de classe.

- firewalld: systemctl status firewalld.service (Més de Fedora 19)
- iptables: systemctl status iptables.service (Menys de Fedora 19)

#### Algun dels anteriors tallafocs es troba activat? 

El firewalld està desactivat, i les iptables, sempre estàn actives a Linux.

#### Instal.leu el servidor web httpd o nginx i activeu-ne el servei (dnf installl ...  ; systemctl ....). Indiqueu les comandes i comproveu que des d'una altra màquina podeu accedir via web a la vostra IP (digueu-li a un company). Hauria de sortir la plana per defecte.

- dnf install nginx
- systemctl start nginx.service

#### Activeu el servei firewall. Indiqueu com ho feu.

- systemctl start firewalld.service

#### Comproveu si ara es pot seguir accedint.

No podem continuar accedint-hi degut a què el firewalld bloqueja per defecte el tràfic entrant a la nostra màquina.

## Tallafocs Win7

#### Porta aquest SO algún tallafocs incorporat?

Porta per defecte un tallafocs anomenat Firewall de Windows, que hi es activat.

#### Arrenqueu una màquina win7 a isard.escoladeltreball.org

#### Indiqueu com arribar al tallafocs (passos i pantalles).

1. Obrim el menú d'Inici.
2. Obrim el "Panel de Control".
3. Fem click sobre "Sistema y Seguridad".
4. Fem click sobre "Firewall de Windows".

#### Es troba activat en aquest windows?

Sí, hi és activat per defecte.

#### Busqueu un altre tallafocs per windows. Indiqueu la plana web i les prestacions que ens dona. Intenteu que NOMÉS sigui tallafocs.

Tinywall:  
- Funciona en segon pla per no molestar al usuari.
- No és intrusiu (no et bombardeja amb popups).
- És molt lleuger (1MB).
- És gratuït i sense publicitat.
- Et permet un control total sobre les seves característiques.
