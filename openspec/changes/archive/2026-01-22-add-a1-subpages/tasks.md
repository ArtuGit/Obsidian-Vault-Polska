# Tasks: Add A1 subpages for learning plan

## 1. Prepare structure
- [ ] Confirm the authoritative topic list is exactly the `[[A1/...]]` links in `content/Plan nauki A1.md`.
- [ ] Confirm every linked file exists under `content/A1/`.
- [ ] Agree on the minimal lesson template (see `design.md`).

## 2. Populate A1 lesson pages (non-empty)
Fill each file with content that follows the template and content rules.

### Pronunciation & spelling
- [ ] `content/A1/Alfabet i wymowa.md`
- [ ] `content/A1/Akcent i intonacja.md`
- [ ] `content/A1/Łączenia i uproszczenia w mowie.md`
- [ ] `content/A1/Ortografia podstawowa.md`

### Basic communication situations
- [ ] `content/A1/Powitania i pożegnania.md`
- [ ] `content/A1/Przedstawianie się.md`
- [ ] `content/A1/Uprzejmość i zwroty grzecznościowe.md`
- [ ] `content/A1/Pytania podstawowe.md`
- [ ] `content/A1/Prośby i polecenia.md`

### Numbers & time
- [ ] `content/A1/Liczby 0-100.md`
- [ ] `content/A1/Liczebniki porządkowe.md`
- [ ] `content/A1/Godziny i czas.md`
- [ ] `content/A1/Dni tygodnia.md`
- [ ] `content/A1/Miesiące i pory roku.md`
- [ ] `content/A1/Daty.md`
- [ ] `content/A1/Liczby w praktyce.md`

### Thematic vocabulary
- [ ] `content/A1/Kolory.md`
- [ ] `content/A1/Rodzina.md`
- [ ] `content/A1/Dom i mieszkanie.md`
- [ ] `content/A1/Jedzenie i napoje.md`
- [ ] `content/A1/Zakupy.md`
- [ ] `content/A1/Restauracja i kawiarnia.md`
- [ ] `content/A1/Transport.md`
- [ ] `content/A1/Miasto i kierunki.md`
- [ ] `content/A1/Pogoda.md`
- [ ] `content/A1/Zdrowie podstawy.md`
- [ ] `content/A1/Praca i szkoła podstawy.md`
- [ ] `content/A1/Zainteresowania i czas wolny.md`

### Grammar: A1 minimum
- [x] `content/A1/Alfabet gramatyczny.md`
- [x] `content/A1/Rzeczownik podstawy.md`
- [ ] `content/A1/Rodzaj rzeczownika.md`
- [ ] `content/A1/Liczba pojedyncza i mnoga.md`
- [ ] `content/A1/Przymiotnik podstawy.md`
- [ ] `content/A1/Stopniowanie przymiotników podstawy.md`
- [ ] `content/A1/Zaimki osobowe.md`
- [ ] `content/A1/Zaimki wskazujące.md`
- [ ] `content/A1/Czasownik podstawy.md`
- [ ] `content/A1/Koniugacja teraźniejszy.md`
- [ ] `content/A1/Negacja nie.md`
- [ ] `content/A1/Pytania tak-nie i pytajniki.md`
- [ ] `content/A1/Przyimki podstawowe.md`
- [ ] `content/A1/Przypadki wstęp.md`
- [ ] `content/A1/Biernik (kogo? co?).md`
- [ ] `content/A1/Miejscownik (o kim? o czym?).md`
- [ ] `content/A1/Narzędnik (z kim? z czym?).md`

### Language functions
- [ ] `content/A1/Opisywanie osób i rzeczy.md`
- [ ] `content/A1/Mówienie o preferencjach.md`
- [ ] `content/A1/Umawianie się.md`
- [ ] `content/A1/Proste opowiadanie o dniu.md`

## 3. Add automated validation
- [ ] Add an npm script (e.g., `npm run validate:a1`) that fails if any `content/A1/*.md` is empty.
- [ ] Optionally enforce basic structure checks described in `design.md`.
- [ ] Wire it into `npm test` or CI so regressions are caught.

## 4. Validate
- [ ] Run `npm run format`.
- [ ] Run `npm run check`.
- [ ] Run `npm run build`.
