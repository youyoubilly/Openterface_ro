---
date: 2024-08-22
authors:
  - Openterface
categories:
  - Updates
---

# Depășirea Obstacolelor: Actualizare Progres și Noua Cronologie

Salutare tuturor,

Sper că sunteți bine. A trecut ceva timp de la ultima noastră actualizare. Mi-aș fi dorit să vă spun că totul a mers ca pe roate pentru Openterface, dar am întâmpinat câteva obstacole care vor întârzia termenul de livrare. Deși nu ne așteptam la asta, abordăm aceste provocări cu hotărâre și facem progrese constante, având multe vești bune de împărtășit. Această postare durează aproximativ **7 minute de citit**, așa că haideți să intrăm în detalii pentru a ști exact unde ne aflăm și ce urmează.

## Reglementări, Producție și Calitate

Înainte de a începe producția, a trebuit să trecem testele de calitate necesare conform reglementărilor, în special certificarea CE. Deoarece versiunea noastră toolkit include nu doar Mini-KVM-ul, ci și mai multe accesorii, fiecare parte a trebuit să treacă testele CE. Aceste teste au durat mai mult decât ne așteptam (se pare că cablurile pot fi destul de pretențioase), dar vestea bună este că **am trecut certificarea CE pentru Mini-KVM-ul nostru și toate componentele sale!** Mai jos este o prezentare generală a certificărilor pentru toate părțile noastre: Mini-KVM, cablu HDMI, cablu Type-C portocaliu, cablu Type-C scurt negru și cablu VGA2HDMI. Cu certificarea în mână, cronologia noastră de producție este acum sigură, iar producătorii noștri **produc în prezent toate părțile** în timp ce vorbesc.

![240823-0](pic/240823-0.jpg)
*Cerinte UKCA și CE sunt aceleași pentru produsele noastre electronice, cu CE acoperind și conformitatea RoHS.*

Acum două săptămâni, am vizitat unul dintre producătorii noștri pentru a instrui managerii de linie în controlul calității pentru cablurile portocalii înainte de a le expedia către noi. Acum, TOATE cablurile portocalii au fost produse și stau într-un colț al studioului nostru.
![240823-1](pic/240823-1.jpg)
*Kevin și Shawn explicau metodele de testare pentru a se asigura că cablul portocaliu funcționează corect cu Mini-KVM-ul nostru Openterface.*

Vom face aceeași sarcină în această săptămână pentru a instrui echipa de control al calității la linia de producție pentru celelalte părți. Iată mostre de cabluri suplimentare.
![240823-2](pic/240823-2.jpg)
*Marcate cu mândrie cu logo-ul nostru TechxArtisan, acestea sunt mostre de cablu HDMI, cablu Type-C scurt și cablu VGA-to-HDMI.*

Așteptăm ca celelalte părți și Mini-KVM-urile să sosească în curând de la producătorii noștri, moment în care vom verifica din nou calitatea fiecărei componente și le vom împacheta corespunzător în studioul nostru înainte de expediere. Cu alte cuvinte, **echipa noastră va asigura personal calitatea** înainte de a ajunge în mâinile voastre.

## Expediere, Posibile Întârzieri și Noua ETA

**Incertitudinea actuală constă în procesul de expediere**. După ce am investigat mai multe companii de transport, am constatat că expedierea va dura mai mult timp, deoarece probabil vom transfera coletele printr-un depozit înainte de a ajunge la depozitul Crowd Supply. Încă dezbatem dacă să alegem transportul maritim sau aerian—vă rugăm să aveți răbdare câteva zile în plus în timp ce stabilim aranjamentele.

Vama este un alt obstacol potențial care ar putea cauza întârzieri neașteptate. Odată ce produsele noastre ajung la depozitul Crowd Supply din SUA, vor dura una până la două săptămâni pentru a fi expediate global în funcție de fiecare comandă. Pentru susținătorii din afara SUA, coletele individuale vor trebui să treacă prin expedierea globală și vama în țara de destinație.

Ținând cont de situația actuală și adăugând un timp de rezervă, rămân optimist că vom finaliza livrarea înainte de sfârșitul acestui an, cu **o nouă ETA la mijlocul lunii ianuarie**. Îmi pare sincer rău pentru inconvenient și apreciez sprijinul și răbdarea voastră în timpul acestei schimbări.

## Hardware Finalizat V1.9

După cum știți din postarea noastră anterioară de pe [Reddit](https://www.reddit.com/r/Openterface_miniKVM/comments/1e25pco/openterface_minikvm_v19_with_pins_for_more/), am decis să **actualizăm hardware-ul nostru la V1.9**, incluzând un set de pini de expansiune hackabili. Acest lucru nu făcea parte din planul original pentru campania de crowdfunding, dar credem că îmbunătățește semnificativ **potențialul hardware-ului pentru utilizări mai largi**.

![240823-3](pic/240823-3.jpg)
*Pinii VCC, GND, Target D+, Target D-, Host D+ și Host D-—unde ‘D’ înseamnă date USB.*

O motivație cheie a fost să permitem **comutarea USB-ului la nivel de software**. De ce este important acest lucru? Pe foaia noastră de parcurs, **ne propunem să susținem o soluție KVM-over-IP**, cum ar fi VNC, în viitor. Ideea este să potrivim controlul local KVM cu protocolul VNC, permițând utilizatorilor să controleze de la distanță computerul țintă prin computerul gazdă. Într-un astfel de scenariu de la distanță, capacitatea utilizatorilor de a comuta portul USB este esențială, mai ales când sunt necesare transferuri de fișiere între gazdă și țintă.

**Pinii de expansiune deschid și mai multe posibilități**, cum ar fi integrarea cu iPadOS, controlul ATX, puntea de rețea și bypass-ul audio. Deși nu voi intra în toate detaliile aici, vă încurajez să vă alăturați comunității Openterface pentru a discuta mai departe cu noi.

Această actualizare hardware ar putea extinde potențial soluția noastră Openterface pentru a funcționa prin IP și a include funcții mai avansate, menținând în același timp punctul său forte ca un instrument KVM-over-USB plug-and-play—perfect pentru profesioniștii IT care navighează în medii IT nesigure, cum ar fi centrele de date necunoscute.

Sunt fericit să raportez că V1.9 a trecut testele noastre interne de bază și va fi finalizat ca versiunea oficială pentru toți susținătorii noștri. Cu toate acestea, această actualizare hardware va necesita teste suplimentare, iar orice dezvoltare bazată pe acești pini de expansiune va fi experimentală și probabil să aibă erori. Aici puteți contribui. Contăm pe comunitatea open-source pentru a ne ajuta să îmbunătățim Openterface împreună.

## Mai Multe Actualizări Software

Pe frontul software, facem progrese interesante. Ne ocupăm acum de **aplicația Openterface pentru Android**! Verificați acest [tweet](https://x.com/TechxArtisan/status/1825460088922071398) pentru o demonstrație timpurie care arată controlul KVM lin, mișcarea mouse-ului și clicurile în acțiune. Mai multe funcții sunt pe drum și, ca întotdeauna, odată ce am finisat puțin codul, **această aplicație va fi și ea open-source** pe repo-ul nostru GitHub [Openterface_Android](https://github.com/TechxArtisanStudio/Openterface_Android).
![240823-4](pic/240823-4.jpg)
*Folosind doar degetele noastre pentru a controla un computer Linux de pe o tabletă Android. Frumos!*

Versiunea noastră QT tocmai a primit o actualizare utilă—acum puteți [transfera text de la gazdă la țintă](https://x.com/TechxArtisan/status/1825919721960780131)! Deci, acum această funcție este suportată pe aplicațiile gazdă macOS, Windows și Linux.

În plus, plănuim să adăugăm o funcție distractivă—[o mișcare automată a mouse-ului pentru a preveni adormirea computerului țintă](https://x.com/TechxArtisan/status/1825471186668847241). Ar trebui să mergem cu mingea de ping-pong care sare pe ecran sau cu efectul clasic de screensaver DVD? Votați și comentați pe [tweet](https://x.com/TechxArtisan/status/1825470086800691459) 😃

## Designul Pachetului, Etichetare și Manual

Am [experimentat cu diverse machete și designuri de ambalaje](https://www.reddit.com/r/Openterface_miniKVM/comments/1elm4vq/almost_ready_to_finalize_our_package_design/) pentru a găsi echilibrul perfect între mai mulți factori cheie:

- Selectarea materialelor suficient de rezistente pentru a proteja produsul și părțile sale în timpul transportului,
- Crearea de etichete informative care să ajute utilizatorii să înțeleagă produsul dintr-o privire,
- Asigurarea conformității cu reglementările,
- Realizarea unui ambalaj atrăgător din punct de vedere vizual,
- Și fiind eco-friendly prin minimizarea utilizării plasticului oriunde este posibil.

În plus, am făcut mai multe îmbunătățiri la vechea geantă toolkit, inclusiv:

- Spațiu de stocare mai mare,
- Un fermoar portocaliu elegant,
- Materiale exterioare și interioare îmbunătățite,
- Și un buzunar din plasă super elastic.

Am ales acest material deoarece atinge echilibrul ideal între a fi prietenos cu bugetul, plăcut la atingere și suficient de durabil pentru a proteja obiectele din interior. **Suntem încrezători că vă va plăcea**.

![240823-5](pic/240823-5.jpg)

Actualizăm și etichetele de pe carcasa de aluminiu pentru a le face cât mai informative și atrăgătoare din punct de vedere vizual. Sperăm că aceste îmbunătățiri vor îmbunătăți experiența utilizatorului și vor face mai ușor să începeți cu Openterface.

![240823-6](pic/240823-6.jpg)

Finalizăm manualul Openterface, care va fi disponibil în engleză, germană, franceză, japoneză și chineză. Ne cerem scuze dacă am omis limba voastră—cutia noastră nu este de dimensiunea TARDIS-ului (cutia polițistului din Doctor Who)! Dar vom face tot posibilul să adăugăm mai multe traduceri pe site-ul nostru.

![240823-7](pic/240823-7.jpg)

## Revizuirea Limbajului Comunitar

Am folosit ChatGPT pentru a ajuta la traduceri, dar uneori poate rata formulările și cuvintele. Dacă nu este prea mare deranjul, aș aprecia foarte mult orice ajutor în revizuirea conținutului în alte limbi, în special pentru materialele tipărite pe care urmează să le finalizăm. Am actualizat tot conținutul textului pentru ambalaj în folderul nostru GitHub [product-printed-materials](https://github.com/TechxArtisanStudio/Openterface/tree/main/product-printed-materials), unde puteți revizui și trimite orice îmbunătățiri. Puteți, de asemenea, să-mi trimiteți un mesaj direct. Mulțumesc!

## Observații Finale și Progres Continu

Ne cerem scuze din nou pentru întârzieri și schimbarea ETA-ului produsului nostru. Vă mulțumim pentru răbdare și pentru că ați rămas alături de noi—lucrăm din greu pentru a vă aduce acest produs cât mai curând posibil! Vă voi actualiza imediat ce aranjăm expedierea. Mai multe actualizări sunt pe drum, așa că vă rugăm să vă alăturați comunității Openterface și să rămâneți la curent!

Cu drag,

Billy Wang  
Product Manager  
Echipa Openterface | TechxArtisan