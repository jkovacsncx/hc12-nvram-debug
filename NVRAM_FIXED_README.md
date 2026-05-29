# NVRAM_FIXED.bin - Helyreállítási Útmutató

## Mi történt?
- Az eredeti gépből: NVRAM.bin (működő konfiguráció)
- A sérült gépbe: NVRAM_FIXED.bin (javított másolat)

## Tartalom
- Magic Number: 123456
- 6 konfigurációs blokk (65 karakter mindegyik)
- Szeparátor: ☺ (speciális karakter)
- Padding: nullák az 131,072 bájtig

## Telepítés
1. Készítsd elő a sérült gépet (reset, UART csatlakozás)
2. Töltsd fel a NVRAM_FIXED.bin-t az eszközbe
3. Indítsd újra

## Ellenőrzés
- Első 100 karakter: 1234560000000000000000000000000000000000000000000000000000000000☺00000˙0602301401...
- Utolsó 100 karakter: minden 0 (padding)
- Teljes méret: 131,072 karakter (UTF-8)
