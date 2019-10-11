# installer plik

```
wget 'https://github.com/root-gg/plik/releases/download/1.2.2/plik-1.2.2-linux-64bits.tar.gz'
tar xf plik-1.2.2-linux-64bits.tar.gz


```

Linux

copier plik dans /usr/bin/.

```
	cp plik-1.2.2/clients/linux-amd64/plik /usr/bin/
```

MacOs
```
	cp plik-1.2.2/clients/darwin-amd64/plik /usr/bin/.
```

```
echo '
Debug = false
Quiet = false
URL = "https://plik.root.gg"
OneShot = false
Removable = false
Stream = false
Secure = false
SecureMethod = "openssl"
Archive = false
ArchiveMethod = "tar"
DownloadBinary = "curl"
Comments = ""
Yubikey = false
Password = ""
TTL = 2592000
AutoUpdate = true
Token = ""

[SecureOptions]
  Cipher = "aes-256-cbc"
  Openssl = "/usr/bin/openssl"
  Options = "-md sha256"

[ArchiveOptions]
  Compress = "gzip"
  Options = ""
  Tar = "/bin/tar"
' > ~/.plikrc
```

tester plik

```
cd
mkdir testplik
cd testplik
touch testfile
plik .
```


# supports de cours

https://drive.google.com/open?id=1t63frMu8oX8G8bbUNKugs4SgRt5hVsRi

# un peu de doc
https://www.google.com/search?q=commandes+de+bases+linux&oq=commandes+de+&aqs=chrome.1.69i57j69i59j0l3j69i60.4859j0j7&sourceid=chrome&ie=UTF-8

# sujet
## procedure de rendu
vous devez créer un répertoire rendu et m'envoyer le lien plik par mail sur thekit+ipssi5@gmail.com
le titre du mail devra être "[IPSSI5e] votre nom"

voici un exemple de procédure pour ne rendre que l'exercice01
```
mkdir ~/rendu
cd rendu
mkdir ex01
cd ex01
nano date.sh
cd ~/rendu
plik .
```

copier le lien et l'envoyer par mail

## ex01 date.sh
faire un script `ex01/date.sh`
qui affiche la date avec le nombre de secondes depuis le 1er janvier 1970

```
   man date
```
## ex02 cd.sh
faire un script `ex02/cd.sh`
qui crée un répertoire, va dedans
affiche le contenu

## ex03 verification.sh
faire un script `ex03/verification.sh`
qui regarde si un fichier "efface_moi" existe
si le fichier existe il l'efface, sinon il affiche "nothing to do"

 indice dans votre `~/.profile` (oui ici pour les utilisateurs de mac https://gist.github.com/edwinksl/dafc0594176df6058bb395e985833189)

## ex04 test_curl.sh
faire un script `ex04/test_curl.sh`
qui test si un site fonctionne et affiche "OK" si c'est le cas "FAIL" si ce n'est pas le cas

indice, utilisez curl

## ex05 historique.sh
faire un script `ex05/historique.sh`
qui affiche l'historique mais uniquement les 15 dernières lignes

le script sera testé en faisant

```
    . ./affiche_histo.sh
```


## ex06 en_cache.php
donnez moi un fichier php `en_cache.php` qui se met en cache 2 minutes sur un CDN ou un reverse proxy

## ex07 cache schema
faire un schmema dans `ex07/schema.jpg`
dessinez-moi un schema d'infrastructure de cache, qui doit contenir 
- un reverse proxy ou cache
- un serveur d'application(type php)
- un utilisateur internet
- une base de donnée
- internet
Des flèches et du texte explicatif seront les bienvenues

## ex08 awk1.sh
faire un script `ex08/awk1.sh`
qui affiche les utilisateurs de /etc/passwd rangés par ordre alphabétique

commande autorisés : awk / sort

exemple de sortie sur un linux
```
avahi
avahi-autoipd
backup
bin
colord
daemon
Debian-exim
```

## ex09 awk2.sh
faire un script `ex09/awk2.sh`
qui affiche les ids des utilisateurs rangés par ordre numérique

commande autorisés : awk / sort

exemple de sortie du script
```
0
1
2
3
4
5
...
1000
64055
65534
```

## ex10 md5
mettez dans un fichier `ex10/md5.txt`
Votre prénom et la somme md5 de votre prénom
exemple
```
thibault
61ee381f89af8762e4c4c25841d86433
```

## ex11 mkdir
faire un script `ex11/mkdir.sh`
qui crée en une seule ligne
1 répertoire `output`
2 répertoires a et b, ceci en une seule ligne

point supplémentaire si vous utilisez {} en bash

exemple de résultat d'exécution du script

```
mkdir: created directory 'output'
mkdir: created directory 'output/a'
mkdir: created directory 'output/b'
#kit@bladrom /tmp $ find output/
output/
output/b
output/a
```


## ex12 boucle
faire un script `ex12/boucle.sh`

qui lit un fichier `list.txt` et créé
- un répertoire `output`
dans ce répertoire crée
- un fichier pour chaque ligne dans le fichier de liste

ppour ce faire utilisez:
while
read

list.txt
```
fichier1_luke
fichier1_je
fichier2_suis
fichier3_ton
fichier4_pere
```

la sortie attendue est:


$ find output/
```
output/
output/fichier1_luke
output/fichier1_je
output/fichier2_suis
output/fichier3_ton
output/fichier4_pere
```

## ex13 ansible apache2.yml
créer un fichier de role ansible `ex13/apache2.yml`

qui installe le package apache2

note: le fichier ne sera pas executé sous ansible mais vérifié à la main

## ex14 ansible 
créer un fichier de role ansible `ex14/ansible.yml`

qui installe copie un fichier `file.conf` dans le repertoire `/etc/file.conf`

note: le fichier ne sera pas executé sous ansible mais vérifié à la main

## ex15 quel intéret de faire l'installation de prometheus via ansible ?
réponse dans `ex15/answer.txt`

# faire son rendu
vous devez avoir si vous avez tout fait dans votre répertoire ~/rendu

```
~/rendu _ ls -l
total 0
drwxr-xr-x 1 kit kit 0 Oct 11 11:25 ex01
drwxr-xr-x 1 kit kit 0 Oct 11 11:25 ex02
drwxr-xr-x 1 kit kit 0 Oct 11 11:25 ex03
drwxr-xr-x 1 kit kit 0 Oct 11 11:25 ex04
drwxr-xr-x 1 kit kit 0 Oct 11 11:25 ex05
drwxr-xr-x 1 kit kit 0 Oct 11 11:25 ex06
drwxr-xr-x 1 kit kit 0 Oct 11 11:25 ex07
drwxr-xr-x 1 kit kit 0 Oct 11 11:25 ex08
drwxr-xr-x 1 kit kit 0 Oct 11 11:25 ex09
drwxr-xr-x 1 kit kit 0 Oct 11 11:25 ex10
drwxr-xr-x 1 kit kit 0 Oct 11 11:25 ex11
drwxr-xr-x 1 kit kit 0 Oct 11 11:25 ex12
drwxr-xr-x 1 kit kit 0 Oct 11 11:25 ex13
drwxr-xr-x 1 kit kit 0 Oct 11 11:25 ex14
drwxr-xr-x 1 kit kit 0 Oct 11 11:25 ex15
```
vous faite donc votre rendu comme ceci
```
cd ~/rendu
plik .
```

et copier coller le lien que plik vous donne, exemple 
```
$ plik . 
Upload successfully created at Fri, 11 Oct 2019 11:27:12 CEST : 
    https://plik.root.gg/#/?id=S2Nz0NYGVBQcXF5m   <----------------------------- CE LIEN ICI

..tar.gz : 234 B 1.07 KB/s                                                      

Commands : 
curl -s "https://plik.root.gg/file/S2Nz0NYGVBQcXF5m/lX6gvLJYdKmx1Zrt/..tar.gz" | tar xvf - --gzip
```

donc dans cet EXEMPLE vous envoyer par mail le lien plik  trouvé: https://plik.root.gg/#/?id=S2Nz0NYGVBQcXF5m 

