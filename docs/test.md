# Testare & Dezvoltare

## 💻 Compatibilitate

- **Suport OS**: Verifică dacă diferitele versiuni de OS pot utiliza aplicația gazdă corespunzătoare.
- **Testare Performanță**: Evaluează performanța pe diverse sisteme gazdă.
- **Testare Versiuni OS**: Asigură compatibilitatea pe diferite versiuni de OS.
- **Probleme Specifice Dispozitivelor**: Identifică și rezolvă problemele specifice anumitor dispozitive sau versiuni de OS.

## 🖱 Control Mouse

<div class="annotate" markdown>

- **Latență Mișcare**: Asigură un control fluid și receptiv.
- **Butoane Mouse**: Testează butoanele stânga, dreapta și mijloc; click & drag.
- **Derulare**: Evaluează viteza și direcția de derulare.
- **Acuratețea** mapării poziției mouse-ului în modul *Absolut* (1)
- **Sensibilitatea** mișcării mouse-ului în modul *Relativ* (2)

</div>

1. Asigură-te că poziția mouse-ului pe țintă este mapată corect pe gazdă. Acest lucru poate fi influențat de rezoluția țintei și de modificările dimensiunii ferestrei aplicației.
2. Asigură-te că mișcarea mouse-ului corespunde așteptărilor intuitive.

## ⌨️ Tastatură

<div class="annotate" markdown>

- **Receptivitate Tastare**: Asigură-te că răspunde așteptărilor intuitive.
- **Mapare Completă a Tastaturii**: În special pentru diverse simboluri speciale.
- **Modificatori**: Taste precum `Ctrl`, `Shift`, `Alt` și `Cmd` sau `Win`.
- **Combinații de Taste**: Suportă tehnic până la 8 taste modificatoare și 6 taste suplimentare apăsate simultan.
- **Taste Media & ACPI**: Taste precum `Volum-`, `Volum+`, `Mute`, `Wake-up`, `Sleep` și `Power`.
- **Layout-uri Tastatură**: Asigură o asociere consistentă pentru diverse layout-uri. (1)

!!! tip

    - **Tester Tastatură**: Poți utiliza un instrument online de testare a tastaturii atât pe computerul gazdă, cât și pe cel țintă pentru a verifica dacă apăsările de taste sunt sincronizate.
    - **Chip CH9329**: Verifică [detaliile](https://github.com/TechxArtisanStudio/Openterface_Mini-KVM_Hardware/tree/main/CH9329) pentru a înțelege limitele controlului tastaturii/mouse-ului în Openterface Mini-KVM.

</div>

1. ⌨️ 🌏 Layout-urile tastaturii variază la nivel global în funcție de regiuni și limbi, cu tipuri populare precum QWERTY, AZERTY, QWERTZ și Dvorak.

## ⚙️ Acces la Nivel BIOS

- **Intrare BIOS**: Testează intrarea în BIOS în timpul secvenței de boot.
- **Funcționalitate**: Asigură control complet al tastaturii și mouse-ului în BIOS.
- **Compatibilitate**: Verifică accesul la BIOS pe diferite mărci și modele de plăci de bază.

## 🔊 Sunet

- **Calitatea Sunetului**: Evaluează claritatea și sincronizarea redării audio.
- **Latență**: Măsoară eventualele întârzieri între acțiuni și sunetul corespunzător.
- **Compatibilitate**: Testează diverse ieșiri audio pe diferite sisteme de operare.

## 🎥 Video

- **Suport Rezoluție**: Testează diverse rezoluții și raporturi de aspect ale ecranului.
- **Rată Cadre**: Evaluează performanța la diferite rate de reîmprospătare.
- **Calitatea Afișajului**: Verifică eventualele artefacte vizuale sau probleme de latență.

## 🔄 Port USB Comutabil

- **Testare Comutator**: Testează comutatorul în diverse scenarii pentru fiabilitate.
- **Compatibilitate Port**: Asigură-te că portul USB-A 2.0 suportă diverse dispozitive USB, precum stick-uri de memorie și camere web.
- **Limitări de Putere**: Confirmă capacitatea de alimentare a portului și adecvarea acestuia pentru diferite dispozitive.

## 🔌 Conectare & Deconectare

- **Testare Conexiune**: Testează scenarii cu diferite secvențe de conectare și deconectare.
- **Gestionare Erori**: Asigură-te că dispozitivul recunoaște și se recuperează din conexiuni necorespunzătoare.
- **Stabilitate**: Verifică stabilitatea atunci când dispozitivele sunt conectate și deconectate repetat.

## 📝 Transfer Text

- **Testare Funcționalitate**: Verifică dacă aplicația gazdă poate transfera cu succes text de pe computerul gazdă pe dispozitivul țintă folosind coduri ASCII.
- **Integritatea Conținutului**: Asigură-te că textul transferat de pe gazdă pe dispozitivul țintă rămâne intact și este reprodus corect.
- **Gestionarea Caracterelor Speciale**: Testează funcția de transfer text cu diverse caractere ASCII pentru a asigura gestionarea și reproducerea corectă pe dispozitivul țintă.
- **Testare Lungime Text**: Testează funcția de transfer text cu texte de diferite lungimi pentru a verifica dacă poate acomoda diverse dimensiuni de text fără probleme.
- **Gestionare Erori**: Testează scenarii de eroare, cum ar fi pierderea conexiunii sau întreruperea în timpul transferului de text, pentru a asigura că aplicația gazdă gestionează aceste situații cu grație și oferă feedback adecvat utilizatorului.
- **Testare Performanță**: Evaluează performanța funcției de transfer text în diverse condiții, inclusiv pe computere mai vechi sau mai lente, pentru a identifica eventualele probleme cu recepționarea semnalelor HID și pentru a asigura o funcționare lină.
- **Testare Interfață Utilizator**: Asigură-te că interfața utilizatorului a aplicației gazdă oferă controale intuitive și feedback pentru inițierea și monitorizarea operațiunilor de transfer text, făcându-l ușor de înțeles și utilizat eficient.

## Diverse

- **Gestionare Erori**: Testează mecanismele de gestionare a erorilor pentru o recuperare grațioasă din întreruperi.
- **Performanță**: Evaluează performanța mini-KVM-ului în diverse scenarii de lucru.
- **Stabilitate**: Efectuează teste de stres pentru stabilitate și fiabilitate pe termen lung.