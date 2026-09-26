# Dove vanno 1.158 miliardi — piano dei 10 capitoli

Stato: **bozza in attesa di ok** (26 settembre 2026).
Modello di design e struttura: `capitolo-1-la-mappa.html` (CSS, font, token, dark mode, stampa riusati identici).
Output finale: un solo `index.html` (indice in cima, 10 capitoli in sequenza, CSS di stampa), più `fonti.json` e `VERIFICHE.md`.

## Blocco da risolvere prima di iniziare

Il proxy di rete di questo ambiente rifiuta (403) tutte le fonti primarie: istat.it, mef.gov.it, dt.mef.gov.it, rgs.mef.gov.it,
de.mef.gov.it, finanze.gov.it, bancaditalia.it, ec.europa.eu, inps.it, itinerariprevidenziali.it, upbilancio.it, corteconti.it,
enea.it, gimbe.org, agenas.gov.it, mimit.gov.it, anticorruzione.it, dovevannoinostrisoldi.com, oecd.org, imf.org, eca.europa.eu, mase.gov.it.
La ricerca web funziona e mi ha permesso di individuare gli URL esatti qui sotto, ma **non posso leggere i documenti**.
Senza lettura alla fonte ogni numero resterebbe `[DA VERIFICARE]`, quindi la regola "nessun numero senza fonte" non è rispettabile.
Serve allargare l'accesso di rete dell'ambiente (o aggiungere i domini sopra alla lista consentita).

## Ancore di coerenza (capitolo 1, non si toccano)

| Grandezza | Valore | Anno | Fonte |
|---|---|---|---|
| Uscite totali PA | 1.158 mld (51,1 % PIL) | 2025 | Istat, conto PA 22/9/2026 |
| Entrate totali PA | 1.088 mld (48,0 % PIL) | 2025 | Istat, conto PA 22/9/2026 |
| Interessi | 87 mld (3,9 % PIL) | 2025 | Istat |
| Disavanzo | 69,7 mld (3,1 % PIL) | 2025 | Istat |
| Debito | 3.096 mld (137,1 % PIL) | fine 2025 | Istat, notifica 22/4/2026 |
| Spesa per funzione COFOG | 1.109 mld, di cui: protezione sociale 468, sanità 146, affari economici 112, istruzione 89, interessi 88, servizi generali 83, ordine pubblico 39, difesa 28, resto 56 | 2024 | Eurostat gov_10a_exp (21/7/2026) |

Ogni capitolo settoriale parte dalla sua fetta COFOG 2024 e la riconcilia esplicitamente con le fonti di settore (perimetri diversi: SEC vs bilancio, competenza vs cassa, PA vs Stato). Le agevolazioni fiscali (cap. 4), gli appalti (cap. 7) e l'evasione (cap. 8) **non si sommano** ai 1.158: sono rispettivamente minori entrate, valore dei bandi e gettito mancante. Ogni capitolo lo dice in una frase.

Nota sul capitolo 1: le prime due fonti puntano alla home istat.it. Propongo di sostituire i link con gli URL esatti (notifica: `https://www.istat.it/wp-content/uploads/2026/04/Notifica_22_04_2026.pdf`; conto PA 22/9/2026: URL da individuare una volta sbloccata la rete), lasciando dati e testo identici. Dimmi se sei d'accordo.

---

## 1. La mappa — fatto
Grafico: barra "ogni 100 € spesi" (COFOG 2024). Tabella: il conto 2025.
Fonti: Istat conto PA 22/9/2026 · Istat notifica 22/4/2026 · Eurostat gov_10a_exp.

## 2. Pensioni e assistenza
Lede (bozza): «Quattro euro su dieci vanno a pensioni e assistenza. Ma non tutti arrivano dai contributi.»
**Grafico principale**: barra impilata dei 468 mld di protezione sociale 2024 divisa per rischio COFOG (vecchiaia, superstiti, malattia e invalidità, famiglia, disoccupazione, casa ed esclusione sociale). Sotto, una seconda barra "chi paga": contributi sociali vs fiscalità generale.
**Tabella "il conto"**: spesa pensionistica, spesa assistenziale, entrate contributive, trasferimenti dallo Stato all'INPS, numero pensionati, pensione media.
**Fonti da leggere**:
1. Eurostat, gov_10a_exp, sottofunzioni GF10, Italia 2024 — `https://ec.europa.eu/eurostat/databrowser/view/gov_10a_exp/default/table?lang=en`
2. INPS, Rendiconto sociale 2025 (pubblicato 30/6/2026) — `https://www.inps.it/it/it/dati-e-bilanci/rendiconti-sociali/rendiconti-sociali-2025/rendiconto-sociale-2025.html`
3. Itinerari Previdenziali, XIII Rapporto "Il bilancio del sistema previdenziale italiano" (gennaio 2026, dati 2024) — `https://www.itinerariprevidenziali.it/wp-content/uploads/2026/01/XIII-Rapporto-Il-Bilancio-del-Sistema-Previdenziale.pdf`
Di supporto: Istat, Annuario statistico 2025 cap. 5 "Protezione sociale" (Sespros, dati 2023) — `https://www.istat.it/storage/ASI/2025/capitoli/C05.pdf`; Istat Noi Italia, protezione sociale — `https://noi-italia.istat.it/pagina.php?id=3&categoria=18&action=show&L=0`.
Rischio noto: Itinerari Previdenziali separa "previdenza" e "assistenza" con criteri propri; lo dico nella nota di metodo e uso l'INPS per il confronto.

## 3. Interessi e debito
Lede (bozza): «Ogni anno 87 miliardi escono per pagare prestiti passati. Più della sanità di tre regioni.»
**Grafico principale**: colonne degli interessi annui 2015–2025 in miliardi, con la linea del costo medio all'emissione dei titoli (%). Fa vedere il calo fino al 2021 e la risalita.
**Tabella "il conto"**: debito fine 2025, composizione per strumento (BTP, BOT, indicizzati, CCT), vita media, costo medio all'emissione 2024/2025/2026, chi detiene il debito (Banca d'Italia ed Eurosistema, banche e assicurazioni italiane, famiglie, esteri).
**Fonti da leggere**:
1. Banca d'Italia, "Finanza pubblica: fabbisogno e debito", statistiche 14/8/2026 (dati a giugno 2026, con serie 2025) — `https://www.bancaditalia.it/pubblicazioni/finanza-pubblica/2026-finanza-pubblica/statistiche_FPI_20260814.pdf`
2. MEF Dipartimento del Tesoro, composizione dei titoli di Stato — `https://www.dt.mef.gov.it/it/debito_pubblico/dati_statistici/composizione_titoli_stato/index_new.html` e vita media ponderata — `https://www.dt.mef.gov.it/it/debito_pubblico/dati_statistici/vita_media_ponderata/`; Linee guida della gestione del debito 2026 (costo medio) — `https://www.dt.mef.gov.it/export/sites/sitodt/modules/documenti_it/debito_pubblico/presentazioni_studi_relazioni/Linee-Guida-della-Gestione-del-Debito-Pubblico-Anno-2026.pdf`
3. Istat, Notifica indebitamento netto e debito, 22/4/2026 (interessi 2022–2025) — `https://www.istat.it/wp-content/uploads/2026/04/Notifica_22_04_2026.pdf`; Eurostat, euro indicators 22/4/2026 sul debito — `https://ec.europa.eu/eurostat/web/products-euro-indicators/w/2-22042026-bp`
Per la serie 2015–2021 degli interessi: Istat, Conti economici nazionali (settembre 2025) — `https://www.istat.it/wp-content/uploads/2025/09/Conti-economici-nazionali-Anni-2023-2024.pdf`.

## 4. Agevolazioni fiscali
Lede (bozza): «Lo Stato rinuncia a incassare decine di miliardi ogni anno. Questa spesa non compare tra le uscite.»
**Grafico principale**: barre orizzontali delle 10 spese fiscali più costose (miliardi di minor gettito) sul totale delle 573 misure censite; a parte, il Superbonus come caso a sé.
**Tabella "il conto"**: numero misure, costo totale stimato, quota IRPEF, costo del Superbonus a consuntivo ENEA, stima finale Corte dei conti, quota PNRR giudicata dalla Corte dei conti europea.
**Fonti da leggere**:
1. MEF, Rapporto annuale sulle spese fiscali 2025 (allegato al bilancio 2026) — `https://www.mef.gov.it/export/sites/MEF/documenti-allegati/2025/RSF-2025-bis.pdf`
2. ENEA, report mensile Superbonus (ultimo disponibile, dati al 31/8/2026 se pubblicato) — URL esatto da individuare su enea.it a rete sbloccata
3. Corte dei conti, Relazione sul rendiconto generale dello Stato 2025 e memoria del Procuratore generale (giudizio di parificazione, giugno 2026) — `https://www.corteconti.it/Home/Organizzazione/UfficiCentraliRegionali/UffSezRiuniteSedeControllo/RelRendiconto`
Di supporto: UPB, Rapporto sulla politica di bilancio 2026 (giugno 2026) — `https://www.upbilancio.it/wp-content/uploads/2026/06/UPB-Rapporto-sulla-politica-di-bilancio-2026.pdf`; Corte dei conti europea, relazione speciale 20/2026 sul Superbonus (URL da individuare su eca.europa.eu).
Nota di metodo obbligatoria: i crediti d'imposta "pagabili" (Superbonus, Transizione 4.0) in SEC 2010 sono contati come spesa, non come minore entrata: questo capitolo dice quanto di essi è già dentro i 1.158.

## 5. Sanità
Lede (bozza): «146 miliardi, tredici euro ogni cento. Dove finiscono: stipendi, farmaci, dispositivi, privati convenzionati.»
**Grafico principale**: barra impilata della spesa sanitaria corrente 2025 per voce economica (personale, beni e servizi con farmaci e dispositivi separati, assistenza convenzionata: medici di base, farmacie, privato accreditato, altro).
**Tabella "il conto"**: spesa sanitaria pubblica 2025 e % PIL, Fondo sanitario nazionale 2025, spesa privata delle famiglie, spesa per dispositivi medici e tetto di legge, payback richiesto alle imprese, risultato d'esercizio aggregato delle regioni.
**Fonti da leggere**:
1. MEF-RGS, "Il monitoraggio della spesa sanitaria", rapporto n. 12 (2025) e aggiornamento 2026 se pubblicato — `https://www.rgs.mef.gov.it/VERSIONE-I/attivita_istituzionali/monitoraggio/spesa_sanitaria/`
2. Corte dei conti, Relazione sul rendiconto 2025, volume sulla sanità (giugno 2026) — `https://www.corteconti.it/Home/Organizzazione/UfficiCentraliRegionali/UffSezRiuniteSedeControllo/RelRendiconto`
3. Fondazione GIMBE, rapporto 2026 e comunicato 28/4/2026 sul DFP — `https://press.gimbe.org/press/comunicati/comunicato.it-IT.html?id=493` (URL del rapporto completo da individuare)
Di supporto: dovevannoinostrisoldi.com per i dispositivi medici — `https://www.dovevannoinostrisoldi.com/spese/sanita`; AGENAS (URL del documento sui dispositivi da individuare: oggi trovo solo il programma HTA 2026–2028).
Riconciliazione: sanità COFOG 2024 = 146 mld; spesa sanitaria corrente SEC 2025 ≈ 141–142 mld secondo le anticipazioni di stampa: la differenza di perimetro (investimenti, spesa sanitaria di altri enti) va spiegata in nota.

## 6. Sussidi alle imprese
Lede (bozza): «112 miliardi per "affari economici": strade, treni, energia, agricoltura e aiuti diretti alle imprese.»
**Grafico principale**: barra impilata dei 112 mld COFOG GF04 2024 per sottofunzione (trasporti, energia e combustibili, agricoltura, industria e commercio, R&S economica, altro), con evidenziata la parte che sono trasferimenti alle imprese.
**Tabella "il conto"**: contributi alla produzione e agli investimenti (conto PA Istat 2025), aiuti concessi registrati nel Registro Nazionale Aiuti (ultimo anno), incentivi erogati dalla Relazione MIMIT, numero di misure attive.
**Fonti da leggere**:
1. Eurostat, gov_10a_exp, sottofunzioni GF04, Italia 2024 — `https://ec.europa.eu/eurostat/databrowser/view/gov_10a_exp/default/table?lang=en`
2. MIMIT, Relazione annuale sugli interventi di sostegno alle attività economiche e produttive ("Relazione 266", ultima edizione) — `https://www.mimit.gov.it/it/incentivi/valutazione-e-monitoraggio-degli-incentivi` (URL del PDF da individuare)
3. Corte dei conti, Relazione sul rendiconto 2025 (capitolo sviluppo economico) e Rapporto sul coordinamento della finanza pubblica 2026 — `https://www.corteconti.it/Home/Documenti/RapportoCoordinamentoFP`
Di supporto: Registro Nazionale Aiuti, open data — `https://www.rna.gov.it` (URL della pagina dati da individuare).
Nota: i crediti d'imposta alle imprese sono in parte già nel cap. 4; il capitolo dice quali voci si sovrappongono.

## 7. Appalti e partecipate
Lede (bozza): «Nel 2025 lo Stato ha messo a gara 310 miliardi di lavori, servizi e forniture. E possiede migliaia di società.»
**Grafico principale**: colonne del valore delle procedure di gara 2019–2025 (ANAC), divise per lavori, servizi, forniture, con la quota PNRR evidenziata.
**Tabella "il conto"**: valore e numero delle procedure 2025, quota PNRR, acquisti di farmaci e dispositivi; partecipate: numero società, addetti, utile o perdita aggregata, società in perdita da tre anni.
**Fonti da leggere**:
1. ANAC, Relazione annuale 2026 sull'attività 2025 (presentata 21/4/2026) — `https://www.anticorruzione.it/documents/91439/393633199/Anac+-+Relazione+annuale+2026+su+attivit%C3%A0+2025.pdf/165c4f77-a913-1fde-ff23-887cbcee3095?t=1776845818213`
2. MEF Dipartimento dell'economia, Rapporto sulle partecipazioni pubbliche (ultima edizione, dati 2023 o 2024) — `https://www.de.mef.gov.it/it/attivita_istituzionali/partecipazioni_pubbliche/censimento_partecipazioni_pubbliche/` (URL del rapporto da individuare)
3. Corte dei conti, Sezione delle autonomie, "Gli organismi partecipati dagli enti territoriali e sanitari" (ultima relazione) — `https://www.corteconti.it/Download?id=c42e4301-46d5-42fa-acd0-1dce418fc243` (da verificare che sia l'edizione più recente)
Nota obbligatoria: il valore delle gare è "a base d'asta" e pluriennale, non spesa dell'anno. Il raccordo con i 1.158 passa per consumi intermedi e investimenti fissi del conto PA.

## 8. Evasione
Lede (bozza): «Circa cento miliardi l'anno di tasse e contributi dovuti non vengono pagati. Più degli interessi sul debito.»
**Grafico principale**: barre orizzontali del tax gap per imposta (IVA, IRPEF lavoro autonomo e impresa, IRES, IRAP, IMU, accise, contributi), ultimo anno stimato.
**Tabella "il conto"**: gap complessivo (intervallo), propensione all'evasione, gettito recuperato dall'attività di contrasto nell'ultimo anno, confronto con gli interessi del cap. 3.
**Fonti da leggere**:
1. MEF, Relazione sull'economia non osservata e sull'evasione fiscale e contributiva 2025 (23/10/2025, stime al 2022) — `https://www.mef.gov.it/export/sites/MEF/documenti-pubblicazioni/rapporti-relazioni/documenti/Relazione-evasione-fiscale-e-contributiva-2025_2310_ore1230.pdf`
2. Camera dei deputati, scheda "Lotta all'evasione fiscale e attività di riscossione" (dati di recupero) — `https://temi.camera.it/leg19/temi/19_tl18_accertamento_e_riscossione.html`
3. Osservatorio CPI, lettura della Relazione 2025 — `https://osservatoriocpi.unicatt.it/ocpi-pubblicazioni-evasione-fiscale-in-calo-le-stime-aggiornate-della-relazione-2025`
Attenzione: la Relazione 2026 esce di norma a fine ottobre; se arriva prima della chiusura del dossier sostituisce la 2025.

## 9. Italia vs Europa
Lede (bozza): «Spendiamo più della media UE in pensioni e interessi, meno in istruzione e sanità. Il totale è simile.»
**Grafico principale**: grafico a punti per funzione COFOG in % del PIL, Italia, Germania, Francia, Spagna, media UE27, anno 2024 (protezione sociale, sanità, istruzione, interessi, affari economici, difesa, servizi generali).
**Tabella "il conto"**: spesa totale, entrate, disavanzo e debito 2025 in % PIL per i 4 paesi e l'UE27.
**Fonti da leggere**:
1. Eurostat, gov_10a_exp (COFOG 2024, aggiornato 21/7/2026) — `https://ec.europa.eu/eurostat/databrowser/view/gov_10a_exp/default/table?lang=en`
2. Eurostat, gov_10a_main (aggregati principali) — `https://ec.europa.eu/eurostat/databrowser/view/gov_10a_main/default/table?lang=en`
3. Eurostat, euro indicators 22/4/2026: disavanzo — `https://ec.europa.eu/eurostat/web/products-euro-indicators/w/2-22042026-ap` e debito — `https://ec.europa.eu/eurostat/web/products-euro-indicators/w/2-22042026-bp`
Di supporto: Eurostat Statistics Explained, "Government expenditure by function – COFOG" — `https://ec.europa.eu/eurostat/statistics-explained/index.php?title=Government_expenditure_by_function_%E2%80%93_COFOG`.

## 10. Le opzioni sul tavolo
Lede (bozza): «Sette misure di cui si discute, con il loro conto. Nessuna è gratis e nessuna basta da sola.»
**Grafico principale**: barre orizzontali del valore stimato di ciascuna misura (miliardi l'anno, intervallo min–max quando le fonti divergono), accanto alla scala dei 69,7 mld di disavanzo.
Per ogni misura una scheda uniforme: valore stimato · chi l'ha proposta · chi ci perde · obiezioni documentate.
Le sette misure proposte (da confermare):
1. Revisione delle spese fiscali (proposte: Corte dei conti, FMI 2026, OCSE 2026; obiezioni: UPB e MEF sul carattere strutturale di molte voci, effetti sul ceto medio)
2. Recupero di evasione e compliance (proposte: MEF, FMI; obiezioni: UPB e Corte dei conti sulle stime di gettito effettivo e sulla non ripetibilità)
3. Sussidi ambientalmente dannosi (proposta: Catalogo MASE; obiezioni: costi per famiglie e trasporto, Confindustria e sindacati)
4. Spending review e centralizzazione acquisti (proposte: FMI 1 % PIL, Corte dei conti, Consip; obiezioni: rendimenti storici bassi, Corte dei conti)
5. Pensioni: uscite anticipate e indicizzazione (proposte: OCSE, UPB, RGS tendenze 2026; obiezioni: sindacati, Itinerari Previdenziali sull'equità generazionale)
6. Riordino delle partecipate (proposta: Corte dei conti, MEF; obiezioni: servizi locali, ANCI)
7. Chiusura e controllo dei crediti edilizi (proposta: Corte dei conti, Corte dei conti europea; obiezioni: filiera edilizia, contenziosi)
**Fonti da leggere**:
1. OCSE, Economic Survey Italy 2026 (aprile 2026) — `https://www.oecd.org/content/dam/oecd/en/publications/reports/2026/04/oecd-economic-surveys-italy-2026_3fd3b6aa/539538b2-en.pdf`
2. FMI, Italy 2026 Article IV staff report (luglio 2026) — `https://www.imf.org/en/publications/cr/issues/2026/07/23/italy-2026-article-iv-consultation-press-release-staff-report-and-statement-by-the-577963`
3. UPB, Rapporto sulla politica di bilancio 2026 (giugno 2026) — `https://www.upbilancio.it/wp-content/uploads/2026/06/UPB-Rapporto-sulla-politica-di-bilancio-2026.pdf`
Di supporto: Corte dei conti, Rapporto sul coordinamento della finanza pubblica 2026; MASE, Catalogo dei sussidi ambientalmente dannosi (ultima edizione, URL da individuare); RGS, "Le tendenze di medio-lungo periodo del sistema pensionistico e socio-sanitario, aggiornamento 2026" (URL da individuare su rgs.mef.gov.it).

---

## Consegna finale
- `dossier/index.html`: indice ancorato in cima, 10 `<section id="cap-N">` in sequenza, un solo `<style>` (quello del modello) più le regole di stampa per l'interruzione di pagina a ogni capitolo.
- `dossier/fonti.json`: per ogni fonte `{ id, ente, titolo, data_pubblicazione, url, capitoli, data_accesso }`.
- `dossier/VERIFICHE.md`: elenco dei numeri da ricontrollare a mano, con fonte, pagina o tabella e motivo del dubbio.
