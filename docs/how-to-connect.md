# Cum să te Conectezi

## Interfețe

![host-side](images/product/host-htc.svg#only-light){:style="width:360px"}

![target-side](images/product/target-htc.svg#only-light){:style="width:360px"}

![host-side](images/product/host-htc_1.svg#only-dark){:style="width:360px"}

![target-side](images/product/target-htc_1.svg#only-dark){:style="width:360px"}

① ![Type-C to Host](images/shell-icons/host.svg#only-light){:style="height:15px"} ![Type-C to Host](images/shell-icons/host_1.svg#only-dark){:style="height:15px"} - **Port USB-C Gazdă** (Femelă): Ca port de dispozitiv USB, conectându-se la computerul gazdă pentru transfer de date prin hub-ul USB încorporat

② ![Type-C to Target](images/shell-icons/target.svg#only-light){:style="height:18px"} ![Type-C to Target](images/shell-icons/target_1.svg#only-dark){:style="height:18px"} - **Port USB-C Țintă** (Femelă): Ca port de dispozitiv USB, conectându-se la computerul gazdă pentru emularea ieșirii HID de tastatură și mouse prin hub-ul USB încorporat

③ ![HDMI Input](images/shell-icons/input.svg#only-light){:style="height:18px"} ![HDMI Input](images/shell-icons/input_1.svg#only-dark){:style="height:18px"} - **Port de Intrare HDMI** (Femelă): Intrare sursă HDMI de la computerul țintă

④ ![USB-A Port](images/shell-icons/switchable-usb.svg#only-light){:style="height:26px"} ![USB-A Port](images/shell-icons/switchable-usb_1.svg#only-dark){:style="height:26px"} - **Port USB-A 2.0 Comutabil** (Femelă): Ca port gazdă USB, utilizat fie de computerul gazdă, fie de computerul țintă la un moment dat, dar nu simultan.

!!! warning "Potrivire Strânsă"
    Vă rugăm să rețineți că acest port USB-A femelă este proiectat cu un mecanism de blocare, care necesită puțină forță suplimentară pentru a conecta și deconecta dispozitivele USB.

⑤ ![Toggle Switch](images/shell-icons/toggle-h-t.svg#only-light){:style="height:20px"} ![Toggle Switch](images/shell-icons/toggle-h-t_1.svg#only-dark){:style="height:20px"} - **Comutator**: Pentru comutarea conexiunii portului USB-A 2.0 între computerul gazdă și computerul țintă

⑥ ![Extension Pins](images/shell-icons/pins.svg#only-light){:style="height:15px"} ![Extension Pins](images/shell-icons/pins_1.svg#only-dark){:style="height:15px"} - **Pini de Extensie**: Pentru mai multe informații, vă rugăm să consultați [Pini de Extensie](/extension-pin) pentru utilizare de către dezvoltatori.

## Pași de Conectare

![to-host](images/product/to-host.svg#only-light){:style="height:260px"} ![to-host](images/product/to-host_1.svg#only-dark){:style="height:260px"}
![to-target](images/product/to-target.svg#only-light){:style="height:260px"} ![to-target](images/product/to-target_1.svg#only-dark){:style="height:260px"}

Pentru a configura Mini-KVM-ul, urmați acești pași în ordine:

1. **Conexiunea Computerului Gazdă** (Partea Portocalie):
    - Conectați computerul gazdă la mini-KVM folosind cablul USB Type-C portocaliu de 1,5m. Introduceți-l în portul femelă Type-C de pe partea portocalie a mini-KVM-ului.

    !!! note "Aplicația Gazdă Necesită"
        Computerul gazdă trebuie să aibă aplicația gazdă instalată. Pentru mai multe informații și linkuri de descărcare, vă rugăm să consultați [Documentația Aplicației](/app).

2. **Conexiunea Dispozitivului Țintă** (Partea Neagră):
    - Conectați dispozitivul țintă la mini-KVM folosind cablul USB Type-C negru de 0,3m. Introduceți-l în portul femelă Type-C de pe partea neagră a mini-KVM-ului.

3. **Conexiunea Ieșirii Video a Țintei** (Partea Neagră):
    - Conectați portul de ieșire video al dispozitivului țintă la portul femelă HDMI de pe partea neagră a mini-KVM-ului. Utilizați cablul HDMI negru de 0,3m sau orice alt cablu adecvat de la sursa video la HDMI, cum ar fi un cablu convertor VGA la HDMI.

    !!! note "Nicio Aplicație Necesită pentru Țintă"
        Nu este necesară nicio preinstalare sau configurare pe dispozitivul țintă. Atâta timp cât dispozitivul țintă suportă operațiuni UI cu ieșire video (HDMI, VGA, etc.) și are un port USB pentru a primi semnale de control emulat de tastatură și mouse (HID), poate fi utilizat. Astfel, platformele de dispozitive țintă suportate includ Windows, macOS, Linux, Android și iOS.

4. **Conexiunea Portului USB-A 2.0 Comutabil** (Opțional):
    - Dacă doriți să conectați un dispozitiv USB la Portul USB-A 2.0 Comutabil, este recomandat să faceți acest lucru după ce ați finalizat cele trei conexiuni de mai sus și ați asigurat că aplicația gazdă este deschisă.