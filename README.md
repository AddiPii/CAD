# AddiPi CAD Repository

3D-printable mechanical parts and CAD sources for an AddiPi setup, including:
- a Raspberry Pi + camera case,
- an adjustable stand,
- source CAD files,
- pre-sliced files and ready-to-print packages.

---

## Quick Language Navigation

- [English Documentation](#english-documentation)
- [Dokumentacja Polska](#dokumentacja-polska)

---

## English Documentation

### 1. Project Overview

This repository contains mechanical design assets for an AddiPi hardware setup. The project is split into two major mechanical modules:

- **CASE (rasp + cam)**: enclosure elements for Raspberry Pi and camera mounting.
- **STAND**: stand components designed to hold or position the assembly.

The repo combines editable CAD source files (`.SLDPRT`, `.SLDASM`), printable exchange formats (`.3MF`, `.STEP`), and generated printer toolpaths (`.gcode`).

### 2. Main Repository Structure

```text
CAD/
|- Full Assembly.SLDASM
|- CASE (rasp + cam)/
|  |- files/              # Main CAD/source and printable files
|  |- gcode/              # Prepared G-code files
|  |- grabcad/            # Legacy/external references and releases
|  |- Ready To Print/     # Ready-made print packages (.3MF)
|- STAND/
|  |- files/              # Stand part files
|  |- gcode/              # Prepared G-code files
|  |- own parts/          # Original stand CAD components
|  |- Ready To Print/     # Ready-made print packages (.3MF)
```

### 3. File Types and Their Purpose

- **`.SLDPRT`**: SolidWorks part files (editable source geometry).
- **`.SLDASM`**: SolidWorks assembly files for complete fit checks.
- **`.3MF`**: print-ready model containers, often including orientation/settings.
- **`.STEP`**: neutral CAD exchange format for non-SolidWorks software.
- **`.gcode`**: machine instructions generated for specific print parameters.

### 4. What Is Ready to Print

Ready-to-print content is provided in two formats:

- **Pre-sliced `.gcode`** in `gcode/` directories.
- **Prepared `.3MF`** projects in `Ready To Print/` directories.

From file naming conventions, slicing profiles appear to target setups like:
- **PLA** filament,
- **0.4 mm** nozzle,
- **Prusa MK3S** class printer.

Always verify compatibility with your own printer, firmware, bed size, and material before starting a print.

### 5. Recommended Workflow

1. Open assemblies/parts in SolidWorks to review fit and dimensions.
2. If needed, export custom geometry to `.STEP`/`.STL`.
3. Slice in your preferred slicer (or use provided `.3MF`/`.gcode`).
4. Validate print settings (material, nozzle, supports, orientation).
5. Print, test-fit, and iterate.

### 6. Notes About Legacy/Reference Assets

The `grabcad/` directory under the case module contains release snapshots and external reference models (for example Raspberry Pi models). Use these as mechanical references and historical context.

### 7. Contributing

If you add or modify parts, consider this convention:

- Keep editable CAD in `files/` or `own parts/`.
- Export printable assets to `Ready To Print/`.
- Store matching sliced outputs in `gcode/`.
- Use descriptive file names including printer/material/nozzle/time when applicable.

### 8. Build and Manufacturing Disclaimer

All prints should be verified by the maker before real-world use. Check clearances, mounting pressure, temperatures, cable routing, and electrical safety around Raspberry Pi and camera modules.

### 9. Inspiration and Attribution

The CASE module is inspired by the Raspberry Pi 4 case project from:

- Embrace Making (YouTube): https://www.youtube.com/watch?v=kXgKs1Zv43U
- GrabCAD by 219 Design (primary reference): https://grabcad.com/library/case-for-raspberry-pi-4-1
- Thingiverse files: https://www.thingiverse.com/thing:4912025/files

Original reference files are published under **CC BY 4.0** license terms. In this repository, `BottomShell` was modified so it fits **Raspberry Pi 3 Model B**.

---

## Dokumentacja Polska

### 1. Opis Projektu

To repozytorium zawiera zasoby CAD i pliki do druku 3D dla mechanicznej części projektu AddiPi. Projekt jest podzielony na dwa główne moduły:

- **CASE (rasp + cam)**: elementy obudowy dla Raspberry Pi i mocowania kamery.
- **STAND**: elementy podstawki/uchwytu do ustawiania zestawu.

W repozytorium znajdują się zarówno edytowalne pliki źródłowe CAD (`.SLDPRT`, `.SLDASM`), jak i formaty do druku (`.3MF`, `.STEP`) oraz gotowe ścieżki drukarki (`.gcode`).

### 2. Główna Struktura Repozytorium

```text
CAD/
|- Full Assembly.SLDASM
|- CASE (rasp + cam)/
|  |- files/              # Główne pliki CAD i modele części
|  |- gcode/              # Wygenerowane pliki G-code
|  |- grabcad/            # Archiwalne referencje i wydania
|  |- Ready To Print/     # Gotowe paczki do druku (.3MF)
|- STAND/
|  |- files/              # Pliki części podstawki
|  |- gcode/              # Wygenerowane pliki G-code
|  |- own parts/          # Oryginalne części CAD podstawki
|  |- Ready To Print/     # Gotowe paczki do druku (.3MF)
```

### 3. Typy Plików i Zastosowanie

- **`.SLDPRT`**: pliki części SolidWorks (edytowalne źródło geometrii).
- **`.SLDASM`**: pliki złożeń SolidWorks (kontrola dopasowania całego układu).
- **`.3MF`**: kontenery modeli gotowych do druku, często z orientacją i ustawieniami.
- **`.STEP`**: neutralny format CAD do wymiany między programami.
- **`.gcode`**: instrukcje ruchu drukarki wygenerowane przez slicer.

### 4. Co Jest Gotowe do Druku

W repozytorium dostępne są gotowe materiały do druku w dwóch formach:

- **Wstępnie pocięte pliki `.gcode`** w katalogach `gcode/`.
- **Przygotowane projekty `.3MF`** w katalogach `Ready To Print/`.

Nazewnictwo plików sugeruje profile dla konfiguracji takich jak:
- filament **PLA**,
- dysza **0.4 mm**,
- drukarka klasy **Prusa MK3S**.

Przed wydrukiem zawsze sprawdź zgodność z własną drukarką, firmware, polem roboczym oraz materiałem.

### 5. Zalecany Workflow

1. Otwórz części/złożenia w SolidWorks i sprawdź dopasowanie.
2. W razie potrzeby wyeksportuj geometrię do `.STEP`/`.STL`.
3. Potnij modele we własnym slicerze (albo użyj dostarczonych `.3MF`/`.gcode`).
4. Zweryfikuj parametry druku (materiał, dysza, podpory, orientacja).
5. Wydrukuj, wykonaj przymiarkę i wprowadzaj iteracje.

### 6. Uwagi o Zasobach Referencyjnych

Folder `grabcad/` w module obudowy zawiera migawki wydań oraz modele referencyjne (np. Raspberry Pi). Traktuj je jako wsparcie projektowe i kontekst historyczny.

### 7. Jak Rozszerzać Repozytorium

Przy dodawaniu lub modyfikacji części warto trzymać się konwencji:

- Edytowalne pliki CAD umieszczaj w `files/` lub `own parts/`.
- Pliki gotowe do druku eksportuj do `Ready To Print/`.
- Odpowiadające im G-code przechowuj w `gcode/`.
- Stosuj opisowe nazwy plików (drukarka/materiał/dysza/czas), gdy to możliwe.

### 8. Odpowiedzialność i Bezpieczeństwo

Każdy wydruk należy zweryfikować przed użyciem. Sprawdź luzy montażowe, temperatury pracy, naciski na elementy, prowadzenie przewodów i bezpieczeństwo elektryczne w pobliżu Raspberry Pi oraz modułu kamery.

### 9. Inspiracja i Atrybucja

Moduł CASE jest inspirowany projektem obudowy dla Raspberry Pi 4 z:

- Embrace Making (YouTube): https://www.youtube.com/watch?v=kXgKs1Zv43U
- GrabCAD od 219 Design (główna referencja): https://grabcad.com/library/case-for-raspberry-pi-4-1
- Pliki Thingiverse: https://www.thingiverse.com/thing:4912025/files

Oryginalne pliki referencyjne są udostępnione na licencji **CC BY 4.0**. W tym repozytorium zmodyfikowano `BottomShell`, aby pasował do **Raspberry Pi 3 Model B**.
