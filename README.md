# Konvolucija v frekvenčnem prostoru

Demonstrirajte razumevanje konvolucije s svojo implementacijo konvolucije v frekvenčnem prostoru s katero "popačite" oz. spremenite podan signal s podanim impulzom.

Na spletni strani http://www.voxengo.com/impulses/ najdete impulzne odzive posameznih prostorov (npr. hala, garažna hiša), s katerimi lahko zvok spremenimo tako, kakor bi se nahajali v tem prostoru.

Pripravite Python skripto ki ima definirane (vsebuje) naslednje funkcije:

## def konv_frekvenca_mono(signal, impulz):

- funkcija prejme 2 parametra:
  - funkcija prejme vektor (x, 1), v katerem se nahaja normaliziran signal za obdelavo
  - funkcija prejme vektor (y, 1), v katerem se nahaja normaliziran impulz
- poskrbite / predpostavljajte, da sta podan signal in impulz vzorčena z enako vzorčevalno frekvenco
- funkcija vrne spremenjen vektor
  - vektor naj bo oblike (z, 1), upoštevajte spremembo velikosti glede na impulz
  - vektor naj bo normaliziran na velikost med -1 in 1
- funkcija naj konvolucijo implementira v frekvenčnem prostoru
  - pretvorite podana signala v v frekvenčni prostor (uporabite funkcijo fft)
  - opravite konvolucijo v frekvenčnem prostoru
  - pretvorite popačen signal nazaj v časovni prostor (uporabite funkcij ifft)

## def konv_frekvenca_stereo(signal, impulz):

- funkcija prejme 2 parametra:
  - funkcija prejme vektor (x, 2), v katerem se nahaja normaliziran signal za obdelavo
  - funkcija prejme vektor (y, 2), v katerem se nahaja normaliziran impulz
- poskrbite / predpostavljajte, da sta podan signal in impulz vzorčena z enako vzorčevalno frekvenco
- funkcija vrne spremenjen vektor
  - vektor naj bo oblike (z, 2), upoštevajte spremembo velikosti glede na impulz
  - vektor naj bo normaliziran na velikost med -1 in 1
- funkcija naj konvolucijo implementira v frekvenčnem prostoru
  - pretvorite podana signala v vfrekvenčni prostor (uporabite funkcijo fft)
  - opravite konvolucijo v frekvenčnem prostoru
  - pretvorite popačen signal nazaj v časovni prostor (uporabite funkcij ifft)

Pripravite še odsek kode katero lahko lahko samostojno zaženete kot demo:

## if __name__ == '__main__':

- pripravite demo katerega lahko poženete
  - pripravite signal dolžine 10 vzorcev
  - pripravite impulz dolžine 3 vzorcev
  - kličite funkcijo konv_frekvenca_mono s pravilno obliko signala
  - kličite funkcijo konv_frekvenca_stereo s pravilno obliko signala
  - izpišite signal, impulz ter rezultat funkcije v terminal