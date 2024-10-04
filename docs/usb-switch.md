# Mecanica Portului USB Comutabil

![switch-graphics](images/product/switch-graphics.svg#only-light){:style="width:460px"}
![switch-graphics](images/product/switch-graphics_1.svg#only-dark){:style="width:460px"}

Dispozitivul mini-KVM dispune de un port USB-A 2.0 comutabil care poate fi alternat între computerul gazdă și cel țintă, dar nu ambele simultan. Această funcționalitate este controlată atât de un comutator fizic, cât și de un comutator software în aplicația gazdă. Acest document explică mecanica și logica din spatele acestor comutatoare.

## Tipuri de Comutatoare

- **Comutator Software**: Un buton de comutare în aplicația gazdă.
      - Comută conexiunea portului USB între computerul gazdă și cel țintă

- ![Toggle Switch](images/shell-icons/toggle-h-t.svg#only-light){:style="height:20px"} ![Toggle Switch](images/shell-icons/toggle-h-t_1.svg#only-dark){:style="height:20px"} **Comutator Hardware**: Un comutator fizic cu două poziții pe dispozitiv.
      - Poziția interioară: Conectează la computerul gazdă
      - Poziția exterioară: Conectează la computerul țintă

## Configurare Inițială și Sincronizare

Când mini-KVM-ul este conectat corect și aplicația gazdă este lansată:

1. Conexiunea reală a portului USB al dispozitivului (circuitul) se conectează inițial la gazdă.
2. Aplicația gazdă detectează poziția actuală a comutatorului hardware, care este setată fie la computerul gazdă, fie la cel țintă.
3. Comutatorul software se sincronizează cu poziția comutatorului hardware.
4. Conexiunea reală a circuitului este actualizată pentru a se potrivi cu pozițiile comutatoarelor.

!!! avertisment "Limitare Hardware"
    Dacă un dispozitiv USB este deja conectat la dispozitiv înainte de pornire sau de lansarea aplicației gazdă, computerul gazdă va emite un avertisment despre eliminarea nesigură a dispozitivului USB. Aceasta este o limitare hardware pentru versiunea 1.9. Prin urmare, se recomandă să nu conectați niciun dispozitiv USB înainte de a porni dispozitivul sau de a lansa aplicația noastră gazdă.

## Stări Operaționale

Datorită prezenței atât a comutatoarelor hardware, cât și a celor software, pot apărea patru stări posibile:

- **Starea 1** (Sincronizat, Conectat la Gazdă):
      - Comutator Hardware: Indică Gazda ![host-computer](images/shell-icons/host-computer.svg#only-light){:style="height:18px"} ![host-computer](images/shell-icons/host-computer_1.svg#only-dark){:style="height:18px"}
      - Comutator Software: Indică Gazda ![host-computer](images/shell-icons/host-computer.svg#only-light){:style="height:18px"} ![host-computer](images/shell-icons/host-computer_1.svg#only-dark){:style="height:18px"}
      - Conexiune Port USB: Conectat la Gazdă ![host-computer](images/shell-icons/host-computer.svg#only-light){:style="height:18px"} ![host-computer](images/shell-icons/host-computer_1.svg#only-dark){:style="height:18px"}

- **Starea 2** (Sincronizat, Conectat la Țintă):
      - Comutator Hardware: Indică Ținta ![target-computer](images/shell-icons/target-computer.svg#only-light){:style="height:18px"} ![target-computer](images/shell-icons/target-computer_1.svg#only-dark){:style="height:18px"}
      - Comutator Software: Indică Ținta ![target-computer](images/shell-icons/target-computer.svg#only-light){:style="height:18px"} ![target-computer](images/shell-icons/target-computer_1.svg#only-dark){:style="height:18px"}
      - Conexiune Port USB: Conectat la Țintă ![target-computer](images/shell-icons/target-computer.svg#only-light){:style="height:18px"} ![target-computer](images/shell-icons/target-computer_1.svg#only-dark){:style="height:18px"}

- **Starea 3** (Desincronizat, USB Conectat la Gazdă):
      - Comutator Hardware: Indică Ținta ![target-computer](images/shell-icons/target-computer.svg#only-light){:style="height:18px"} ![target-computer](images/shell-icons/target-computer_1.svg#only-dark){:style="height:18px"}
      - Comutator Software: Indică Gazda ![host-computer](images/shell-icons/host-computer.svg#only-light){:style="height:18px"} ![host-computer](images/shell-icons/host-computer_1.svg#only-dark){:style="height:18px"}
      - Conexiune Port USB: Conectat la Gazdă ![host-computer](images/shell-icons/host-computer.svg#only-light){:style="height:18px"} ![host-computer](images/shell-icons/host-computer_1.svg#only-dark){:style="height:18px"}

- **Starea 4** (Desincronizat, USB Conectat la Țintă):
      - Comutator Hardware: Indică Gazda ![host-computer](images/shell-icons/host-computer.svg#only-light){:style="height:18px"} ![host-computer](images/shell-icons/host-computer_1.svg#only-dark){:style="height:18px"}
      - Comutator Software: Indică Ținta ![target-computer](images/shell-icons/target-computer.svg#only-light){:style="height:18px"} ![target-computer](images/shell-icons/target-computer_1.svg#only-dark){:style="height:18px"}
      - Conexiune Port USB: Conectat la Țintă ![target-computer](images/shell-icons/target-computer.svg#only-light){:style="height:18px"} ![target-computer](images/shell-icons/target-computer_1.svg#only-dark){:style="height:18px"}

## Tranziții și Logică de Stare

### Din **Starea 1** (Sincronizat la Gazdă)

- ^^***Scenariul 1a***^^: Utilizatorul Mută Comutatorul Hardware la Țintă
      - Actualizează variabila internă de stare la Țintă ![target-computer](images/shell-icons/target-computer.svg#only-light){:style="height:18px"} ![target-computer](images/shell-icons/target-computer_1.svg#only-dark){:style="height:18px"}
      - Actualizează afișajul aplicației gazdă pentru a arăta Ținta ![target-computer](images/shell-icons/target-computer.svg#only-light){:style="height:18px"} ![target-computer](images/shell-icons/target-computer_1.svg#only-dark){:style="height:18px"}
      - Comută conexiunea reală a circuitului la Țintă ![target-computer](images/shell-icons/target-computer.svg#only-light){:style="height:18px"} ![target-computer](images/shell-icons/target-computer_1.svg#only-dark){:style="height:18px"}
      - Tranziție la Starea 2, sincronizat

- ***Scenariul 1b***: Utilizatorul Apasă Comutatorul Software la Țintă
      - Actualizează variabila internă de stare la Țintă ![target-computer](images/shell-icons/target-computer.svg#only-light){:style="height:18px"} ![target-computer](images/shell-icons/target-computer_1.svg#only-dark){:style="height:18px"}
      - Poziția comutatorului hardware rămâne neschimbată (indicând Gazda ![host-computer](images/shell-icons/host-computer.svg#only-light){:style="height:18px"} ![host-computer](images/shell-icons/host-computer_1.svg#only-dark){:style="height:18px"})
      - Comută conexiunea reală a circuitului la Țintă ![target-computer](images/shell-icons/target-computer.svg#only-light){:style="height:18px"} ![target-computer](images/shell-icons/target-computer_1.svg#only-dark){:style="height:18px"}
      - Tranziție la Starea 3, desincronizat

### Din **Starea 2** (Sincronizat la Țintă)

- ^^***Scenariul 2a***^^: Utilizatorul Mută Comutatorul Hardware la Gazdă ![host-computer](images/shell-icons/host-computer.svg#only-light){:style="height:18px"} ![host-computer](images/shell-icons/host-computer_1.svg#only-dark){:style="height:18px"}:
      - Actualizează variabila internă de stare la Gazdă ![host-computer](images/shell-icons/host-computer.svg#only-light){:style="height:18px"} ![host-computer](images/shell-icons/host-computer_1.svg#only-dark){:style="height:18px"}
      - Actualizează afișajul comutatorului software pentru a arăta Gazda ![host-computer](images/shell-icons/host-computer.svg#only-light){:style="height:18px"} ![host-computer](images/shell-icons/host-computer_1.svg#only-dark){:style="height:18px"}
      - Comută conexiunea reală a circuitului la Gazdă ![host-computer](images/shell-icons/host-computer.svg#only-light){:style="height:18px"} ![host-computer](images/shell-icons/host-computer_1.svg#only-dark){:style="height:18px"}
      - Tranziție la Starea 1, sincronizat

- ***Scenariul 2b***: Utilizatorul Apasă Comutatorul Software la Gazdă ![host-computer](images/shell-icons/host-computer.svg#only-light){:style="height:18px"} ![host-computer](images/shell-icons/host-computer_1.svg#only-dark){:style="height:18px"}:
      - Actualizează variabila internă de stare la Gazdă ![host-computer](images/shell-icons/host-computer.svg#only-light){:style="height:18px"} ![host-computer](images/shell-icons/host-computer_1.svg#only-dark){:style="height:18px"}
      - Poziția comutatorului hardware rămâne neschimbată (indicând Ținta ![target-computer](images/shell-icons/target-computer.svg#only-light){:style="height:18px"} ![target-computer](images/shell-icons/target-computer_1.svg#only-dark){:style="height:18px"})
      - Comută conexiunea reală a circuitului la Gazdă ![host-computer](images/shell-icons/host-computer.svg#only-light){:style="height:18px"} ![host-computer](images/shell-icons/host-computer_1.svg#only-dark){:style="height:18px"}
      - Tranziție la Starea 4, desincronizat

### Din **Starea 3** (Desincronizat, USB Conectat la Gazdă)

- ^^***Scenariul 3a***^^: Utilizatorul Mută Comutatorul Hardware la Țintă ![target-computer](images/shell-icons/target-computer.svg#only-light){:style="height:18px"} ![target-computer](images/shell-icons/target-computer_1.svg#only-dark){:style="height:18px"}:
      - Fără modificări ale variabilelor
      - Tranziție la Starea 2, sincronizat

- ***Scenariul 3b***: Utilizatorul Apasă Comutatorul Software la Gazdă ![host-computer](images/shell-icons/host-computer.svg#only-light){:style="height:18px"} ![host-computer](images/shell-icons/host-computer_1.svg#only-dark){:style="height:18px"}:
      - Actualizează variabila internă de stare la Gazdă ![host-computer](images/shell-icons/host-computer.svg#only-light){:style="height:18px"} ![host-computer](images/shell-icons/host-computer_1.svg#only-dark){:style="height:18px"}
      - Poziția comutatorului hardware rămâne neschimbată (indicând Ținta ![target-computer](images/shell-icons/target-computer.svg#only-light){:style="height:18px"} ![target-computer](images/shell-icons/target-computer_1.svg#only-dark){:style="height:18px"})
      - Comută conexiunea reală a circuitului la Gazdă ![host-computer](images/shell-icons/host-computer.svg#only-light){:style="height:18px"} ![host-computer](images/shell-icons/host-computer_1.svg#only-dark){:style="height:18px"}
      - Tranziție la Starea 1, sincronizat

### Din **Starea 4** (Desincronizat, USB Conectat la Țintă)

- ^^***Scenariul 4a***^^: Utilizatorul Mută Comutatorul Hardware la Gazdă ![host-computer](images/shell-icons/host-computer.svg#only-light){:style="height:18px"} ![host-computer](images/shell-icons/host-computer_1.svg#only-dark){:style="height:18px"}:
      - Fără modificări ale variabilelor
      - Tranziție la Starea 1, sincronizat

- ***Scenariul 4b***: Utilizatorul Apasă Comutatorul Software la Țintă ![target-computer](images/shell-icons/target-computer.svg#only-light){:style="height:18px"} ![target-computer](images/shell-icons/target-computer_1.svg#only-dark){:style="height:18px"}:
      - Actualizează variabila internă de stare la Țintă ![target-computer](images/shell-icons/target-computer.svg#only-light){:style="height:18px"} ![target-computer](images/shell-icons/target-computer_1.svg#only-dark){:style="height:18px"}
      - Poziția comutatorului hardware rămâne neschimbată (indicând Gazda ![host-computer](images/shell-icons/host-computer.svg#only-light){:style="height:18px"} ![host-computer](images/shell-icons/host-computer_1.svg#only-dark){:style="height:18px"})
      - Comută conexiunea reală a circuitului la Țintă ![target-computer](images/shell-icons/target-computer.svg#only-light){:style="height:18px"} ![target-computer](images/shell-icons/target-computer_1.svg#only-dark){:style="height:18px"}
      - Tranziție la Starea 2, sincronizat

!!! avertisment "Amintiți-vă să ejectați unitatea flash înainte de a comuta"
    Dacă portul USB este utilizat de o unitate flash, asigurați-vă că ejectați unitatea flash înainte de a comuta pentru a transfera utilizarea portului la un alt computer.

!!! avertisment "Limitări de putere USB"
    Puterea furnizată de portul USB depinde de placa de bază a gazdei. Nu se recomandă conectarea dispozitivelor USB care necesită multă putere. De obicei, consumul de energie nu ar trebui să depășească 1.5W. Conectarea dispozitivelor de mare putere poate duce la funcționare instabilă sau la posibile daune.

!!! Notă "Ghid pentru Utilizatori"
    - **Prioritatea Comutatorului Software**: Indiferent de poziția comutatorului hardware, apăsarea comutatorului software va schimba imediat direcția circuitului.

    - **Sincronizarea Comutatorului Hardware**: Orice comutare manuală a comutatorului hardware va alinia starea acestuia cu comutatorul software, trecând fie la Starea 1, fie la Starea 2 din stările desincronizate Starea 3 sau Starea 4. Cu toate acestea, această sincronizare nu modifică neapărat conexiunea reală a circuitului.

    - **Monitorizarea Comutatorului Hardware**: Comutatorul hardware, deși este fizic, este monitorizat de software și nu controlează direct direcția circuitului. În schimb, software-ul interpretează poziția comutatorului și gestionează comutarea reală a circuitului.

## De ce Contează Comutarea USB Controlată de Software

Îmbunătățirea comutării USB controlate de software introdusă în versiunea 1.9 este o caracteristică esențială pentru planurile noastre viitoare de dezvoltare, în special în sprijinirea soluțiilor KVM-over-IP, cum ar fi VNC (pe care încă nu le-am implementat). Această capacitate permite utilizatorilor să comute și să partajeze de la distanță portul USB între computerele țintă și gazdă, ceea ce este deosebit de important pentru facilitarea transferurilor de fișiere într-o configurație la distanță.

Această caracteristică deschide o lume de posibilități pentru gestionarea și controlul de la distanță. De exemplu, permite transferuri de fișiere între dispozitive fără intervenție fizică, îmbunătățind eficiența depanării și gestionării sistemului de la distanță.

Aveți idei creative despre cum să valorificați această caracteristică? Ne-ar plăcea să discutăm cu voi! Alăturați-vă comunității Openterface [community](/community/) și împărtășiți-vă gândurile 😃
