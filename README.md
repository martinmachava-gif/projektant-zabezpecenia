# Projektant zabezpečenia

Program pre Windows na návrh kamerových systémov (CCTV), zabezpečovacích systémov (PZS) a kontroly vstupu (EKV)
na pôdoryse – zjednodušený „AutoCAD“ pre montážnikov a projektantov. Beží lokálne, projekty nikam neodosiela
(kvôli licencii sa raz za týždeň spojí s licenčným serverom – posiela len kód počítača, licenčný kľúč a verziu).

**Stiahnutie:** [ProjektantZabezpecenia.exe z poslednej verzie](https://github.com/martinmachava-gif/projektant-zabezpecenia/releases/latest/download/ProjektantZabezpecenia.exe)
(všetky verzie sú v časti [Releases](https://github.com/martinmachava-gif/projektant-zabezpecenia/releases)).
Je to jeden súbor pre Windows 10/11 (64-bit), netreba nič inštalovať. Pri prvom spustení môže Windows ukázať
„Systém Windows ochránil váš počítač“ – program nie je digitálne podpísaný, stačí *Ďalšie informácie → Spustiť aj tak*.

## Čo vie

- **podklad**: PDF (aj viacstranové, aj otočené strany z CAD), obrázok (PNG, JPG …) alebo **DXF** z AutoCADu
  (čiary, oblúky, kružnice, krivky, bloky, texty s diakritikou); pri DXF sa vyberú vrstvy, ktoré sú **steny**
- **kalibrácia mierky**: klik na dva body so známou vzdialenosťou a zadanie skutočnej dĺžky; meranie vzdialeností
- **kreslenie**: steny (hrúbka, uzavretie), miestnosť jedným ťahom, čiary, obdĺžniky, texty, kóty;
  prichytávanie k bodom/stredom/stenám, mriežka, ortho (Shift), zadanie dĺžky číslom + Enter
- **zariadenia z knižnice**: kamery bullet/dome/turret/PTZ/fisheye, NVR, switch, ústredňa, PIR, záclonový,
  magnetický kontakt, detektor skla, dymový, sirény, klávesnica, čítačka, zámok, … – automatické označenie (C01, P03 …)
- **zorné polia kamier** orezané o steny (tiene za stenami, prechod cez dvere), **DORI zóny** podľa rozlíšenia a uhla,
  detekčné zóny PIR a detektorov skla; natáčanie a zmena dosahu/uhla myšou za úchyty
- **káble** medzi zariadeniami s typom, dĺžkou z pôdorysu, prídavkom a rezervou v %
- **podlažia**, **vrstvy** (skryť / zamknúť), späť/znova, kopírovanie, prečíslovanie
- **tlač a PDF** v mierke (A4 – A0) s legendou, grafickou mierkou a rohovou pečiatkou
- **výkaz materiálu do Excelu**: počty podľa modelov, metre káblov, ceny z knižnice, zoznam zariadení a káblov
- vlastná **knižnica modelov** (výrobca, cena, uhol, dosah, rozlíšenie, IR) a typov káblov
- **automatická aktualizácia** z GitHubu (Pomoc → Skontrolovať aktualizácie)
- **licencia**: 14 dní zadarmo plná verzia, potom s licenčným kľúčom (Pomoc → Licencia);
  bez licencie ostáva otváranie a prezeranie projektov, meranie a tlač

## Ovládanie

Koliesko = zoom, stredné tlačidlo alebo medzerník + ťahanie = posun, Home = celé podlažie.
Nástroje: V výber, S stena, M miestnosť, L čiara, O obdĺžnik, T text, D kóta, K kábel, Q meranie.
Prehľad všetkých skratiek: Pomoc → Ovládanie a klávesové skratky (F1).

## Licencia a použité knižnice

Od verzie 1.1.0 program potrebuje licenciu. Po prvom spustení ponúkne **14 dní zadarmo** plnú verziu
(raz na počítač, treba internet). Potom sa zadá **licenčný kľúč** v okne Pomoc → Licencia; licencia platí
na počítači, kde bola aktivovaná, a dá sa preniesť na iný (Deaktivovať na tomto počítači). Počítač bez internetu
sa dá aktivovať ručne kódom poslaným e-mailom. Bez licencie môžete projekty ďalej otvárať, prezerať, merať v nich
a tlačiť.

Zdrojový kód programu nie je verejný. Všetky práva vyhradené.

Program používa tieto knižnice tretích strán:
- [PDFium](https://pdfium.googlesource.com/pdfium/) – © The PDFium Authors, licencia BSD 3-Clause a Apache 2.0
  (zostavenie [pdfium-binaries](https://github.com/bblanchon/pdfium-binaries))
- [PDFsharp](https://github.com/empira/PDFsharp) 6.2 – © empira Software GmbH, licencia MIT
- [.NET](https://dotnet.microsoft.com/) – © Microsoft, licencia MIT
