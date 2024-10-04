# Ghid pentru Pinii de Extensie

![change-cap](images/product/change-cap.svg#only-light){:style="height:300px"}
![change-cap](images/product/change-cap_1.svg#only-dark){:style="height:300px"}

Openterface Mini-KVM include pini de extensie pentru dezvoltare avansată și experimente cu [Software Deschis](/app). Acești pini nu sunt expuși în configurația standard a carcasei.

### Accesarea Pinilor de Extensie pentru Dezvoltare

Pentru a accesa pinii de extensie:

1. Dezasamblați dispozitivul
2. Înlocuiți capacul original al carcasei cu un capac special pentru pini de extensie
3. Descărcați modelul 3D pentru capacul pinilor de extensie din [repositorul nostru GitHub](https://github.com/TechxArtisanStudio/Openterface_Mini-KVM_Hardware)

!!! warning "Anulare Garanție"
    Îndepărtarea carcasei originale anulează garanția produsului. Toate modificările sau dezasamblările sunt realizate pe riscul utilizatorului.

!!! note "Funcții Experimentale"
    Funcțiile dezvoltate folosind acești pini sunt experimentale și nu au fost complet testate. Openterface nu este responsabil pentru eventualele daune, răniri sau defecțiuni rezultate din modificări, expunerea pinilor de extensie sau alte alterări ale dispozitivului.

### Configurația Pinilor

![target-side](images/product/extension-pins-1.svg#only-light){:style="height:200px"}
![host-side](images/product/extension-pins-2.svg#only-light){:style="height:200px"}
![target-side](images/product/extension-pins-1_1.svg#only-dark){:style="height:200px"}
![host-side](images/product/extension-pins-2_1.svg#only-dark){:style="height:200px"}

Pinii de extensie oferă următoarele conexiuni:

1. Alimentare USB 5V pentru componente externe
2. Date pozitive către hub-ul USB al gazdei
3. Date negative către hub-ul USB al gazdei
4. Date pozitive către hub-ul USB al țintei
5. Date negative către hub-ul USB al țintei
6. Împământare

!!! danger "Conexiuni Incorecte"
    Inversarea VCC și GND poate provoca daune severe dispozitivului și componentelor conectate. Verificați întotdeauna conexiunile pinilor înainte de a alimenta dispozitivul.
