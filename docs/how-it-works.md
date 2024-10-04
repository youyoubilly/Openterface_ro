# Cum Funcționează

## Descrierea Procesului

- **Streaming Ecran**: Mini-KVM-ul capturează fluxul de ecran de la computerul țintă și îl afișează în aplicația de pe computerul gazdă. Astfel, utilizatorii pot vizualiza și gestiona sistemul țintă direct de pe mașina gazdă.
- **Controlul Cursorului și Mouse-ului**: Prin mutarea mouse-ului în fereastra aplicației de pe computerul gazdă, utilizatorii pot controla cursorul de pe dispozitivul țintă, similar cu utilizarea unui VNC. Această funcționalitate permite operarea simultană a două sisteme pe un singur ecran.
- **Introducerea de la Tastatură**: Când fereastra aplicației este activă, orice apăsare de taste pe tastatura computerului gazdă este transmisă către dispozitivul țintă, permițând o tastare și introducere de comenzi fără întreruperi.
- **Conversia Semnalelor HID**: Toate intrările de la tastatură și mouse din aplicație sunt convertite în semnale de control Human Interface Device (HID), care sunt apoi trimise către computerul țintă.
- **Sincronizare**: Aplicația asigură sincronizarea ecranului și cursorului computerului țintă cu afișajul computerului gazdă, facilitând o experiență unificată pentru utilizator.

Puteți explora software-ul [Software](/app) și hardware-ul [Hardware](/open-hardware) open-source Openterface pentru mai multe detalii.