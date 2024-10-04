# Control de Bază

![use-case-pc-angled-view](images/product/use-case-pc-angled-view.jpg)

## 💻 Compatibilitate

- **Software Gazdă**: Instalează aplicația noastră [host app](/app) pentru macOS, Windows și Linux pentru a controla dispozitivele țintă. Asigură-te că sistemul gazdă este compatibil cu versiunea corespunzătoare a aplicației.
- **Compatibilitate Dispozitiv Țintă**: Nu este necesară pre-instalarea sau configurarea pe dispozitivul țintă. Atâta timp cât dispozitivul țintă suportă operațiuni UI cu ieșire video (de exemplu, HDMI, VGA) și are un port USB pentru a primi semnale emulate de control tastatură și mouse (HID), poate fi utilizat. Platformele țintă suportate includ Windows, macOS, Linux, Android și iOS.

## 🖱 Control Mouse

- **Mod Absolut**: Cursorul mouse-ului de pe dispozitivul țintă este mapat direct la o poziție specifică pe ecranul gazdei prin aplicația noastră. Asta înseamnă că oriunde miști mouse-ul gazdei în aplicația noastră, mouse-ul dispozitivului țintă va urma aceeași mișcare. Reține că poate exista o ușoară întârziere în mișcările cursorului. Poți alege să ascunzi sau să afișezi cursorul mouse-ului gazdei în timp ce este în aplicația noastră.

- **Mod Relativ**: Mișcarea mouse-ului de pe dispozitivul țintă este relativă la poziția curentă a mouse-ului gazdei. Asta înseamnă că mișcarea mouse-ului gazdei va deplasa cursorul dispozitivului țintă cu o anumită distanță în aceeași direcție, fără un punct de început sau sfârșit fix. Poți ieși din acest mod relativ folosind un anumit scurtătură.

## ⌨️ Tastatură

Când aplicația este focalizată, poți tasta orice direct, iar aceste apăsări de taste vor fi transmise către computerul țintă.

## ⚙️ Acces la Nivel BIOS

- **Acces BIOS**: Folosește aplicația noastră pentru a accesa BIOS-ul dispozitivelor țintă. Acest lucru îți permite să controlezi și să configurezi setările direct din BIOS.

??? tip "Apăsări de taste pentru a intra în BIOS pentru diferite plăci de bază"

    - F2: Dell, Lenovo, ASUS, Acer, Toshiba, Samsung, Sony
    - F1: Lenovo
    - Del: ASUS, Acer, Gigabyte, MSI
    - F10: HP
    - Buton Assist: Sony
    - Tasta Option (⌥): Apple (pentru a accesa managerul de pornire)

## 🔊 Sunet

- **Transmisie Audio**: Sunetul computerului țintă este transmis prin portul de intrare HDMI al mini-KVM-ului. Când folosești aplicația noastră, sunetul de la computerul țintă va fi redat prin computerul gazdă, asigurându-te că auzi totul fără întreruperi.

## 🎥 Video

- **Afișare Video**: Aplicația noastră îți permite să vizualizezi ecranul computerului țintă fără probleme. Suportă rezoluții video de până la 1920x1080 la 30Hz pentru afișare în aplicație. Intrarea video maximă suportată este de până la 3840x2160 la 30Hz prin HDMI. În plus, cu utilizarea unui adaptor, poate acomoda și surse de intrare video VGA, Micro HDMI, DVI și altele.

## 🔄 Port USB Comutabil

- **Utilizarea Portului USB**: Mini-KVM-ul dispune de un port USB-A 2.0 comutabil care poate fi alternat între computerele gazdă și țintă, dar nu ambele simultan.
- **Metode de Comutare**: 
    - Comutator Hardware: Un comutator fizic pe dispozitiv
    - Comutator Software: Un buton în aplicația gazdă
- **Logica Comutării**: Pentru informații mai detaliate despre logica de funcționare a portului USB comutabil, inclusiv interacțiunea dintre comutatoarele hardware și software, configurarea inițială, stările operaționale și tranzițiile de stare, te rugăm să consulți documentația [USB Switch](usb-switch.md).

!!! warning "Important"
    - Amintește-ți să scoți în siguranță orice unități USB conectate înainte de a comuta conexiunea portului.
    - Portul USB are limitări de putere. Nu conecta dispozitive care necesită multă putere, deoarece acest lucru poate duce la funcționare instabilă sau la posibile daune.
