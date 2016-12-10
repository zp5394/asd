#ChatDB

Avtorja: 
+ Nik Dizdarevič 63130033
+ Žan Pogačnik 63140324

Projekt predstavlja aplikacijo, ustvarjeno v programskem jeziku C#, ki omogoča uporabnikom pogovarjanje v spletni klepetalnici. Aplikacija uporablja podatkovno bazo za hranjenje sporočil in uporabnikov in omogoča tudi registracijo novih uporabnikov. 

##Zaslonska slika programa
slika

##Opis aplikacije 
Aplikacija je sestavljena iz dveh WebForm-ov; Chat.aspx in Login.aspx. Zraven imamo tudi podatkovno bazo, v kateri hranimo dve tabeli, tabelo Pogovor in tabelo Uporabnik. 
#####Registracija & vpis
Ko uporabnik hoče dostopati do aplikacije, ga najprej preusmerimo na Login.aspx, kjer ima na voljo registracijo ali prijavo. Če je že prej vnešen v podatkovno bazo se lahko prijavi s svojim uporabniškim imenom in geslom, drugače pa se mora registrirati. Ob registraciji poda svoj ime in priimek, uporabniško ime, ki ga hoče uporabljati ter geslo. Polje za ime in priimek zahteva dve besedi, polje za uporabniško ime je obvezno, geslo pa more uporabnik vnesti v dva polja, ki se morata ujemati. Geslo mora tudi biti sestavljeno iz dveh velikih črk, dveh številk, en poseben znak in mora imeti najmanj osem znakov. Ko klikne na gumb za registracijo, se podatki iz vnosnih polj shranijo v tabelo Uporabnik. Ta tabela ima štiri stolpce; username, ime, priimek, geslo. Stolpec username služi kot primarni ključ, saj dva uporabnika ne moreta imeti enako uporabniško ime. Preden se geslo zapiše v tabelo, ga še zahaširamo s fukncijo Md5.  
#####Chat.aspx
Po uspešni registraciji in/ali prijavi uporabnika preusmerimo na Chat.aspx. Tam lahko uporabnik vidi ostale prijavljene uporabnike, in sporočila, ki so jih poslali. Ko uporabnik pošlje sporočilo se le to shrani v tabelo Pogovor, kjer imamo dva stolpca; username in besedilo. V stolpec username se shrani uporabnikovo ime, v stolpcu besedilo pa tisto, kar je napisal.  
#####Problemi & izboljšave
Največji problemi pri izdelavi aplikacije je zagotavljanje povezave med aplikacijo in podatkovno bazo; tako branje kot pisanje v le to. 
Aplikacijo bi lahko izboljšali na več načinov, kot na primer, takoj ko se uporabnik registrira ga že preusmeri na Chat.aspx, namesto da se mora potem uporabnik ponovno vpisati. Lahko bi tudi hranili slike uporabnikov, ki bi jih prikazovali zraven uporabnikovega imena. 
####Opis nalog
Večino funkcionalnosti v aplikaciji je implementiral Nik Dizdarevič, poročilo pa sem spisal jaz.

Seznam uporabnikov že v podatkovni bazi:
+ username: [] geslo:
+ username: "user"	geslo: AB12!lolekbolek
