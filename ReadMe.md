# Segmentacija Marketinških Kampanja pomoću Klasterizacije

Ovaj projekat fokusiran je na analizu i segmentaciju baze od 10.000 marketinških kampanja. Cilj je bio da se primenom tehnika mašinskog učenja identifikuju ključne grupe kampanja na osnovu njihovih performansi i budžeta.

## Ciljevi analize

- Identifikacija optimalnog broja segmenata unutar gustog skupa podataka.
- Poređenje performansi različitih algoritama za klasterizaciju.
- Vizuelizacija strukture podataka pre i nakon obrade.

## Korišćeni algoritmi i metode

U okviru projekta testirano je pet različitih modela kako bi se pronašlo najstabilnije rešenje:

1. **K-Means (k=4)**
2. **Mini-Batch K-Means**
3. **Hijerarhijska klasterizacija (Ward metoda)**
4. **DBSCAN**
5. **Mean Shift**

## Metodologija rada

- **Preprocesiranje**: Izvršena je standardizacija podataka i logaritamska transformacija ključnih varijabli (`Budget`, `Revenue`) radi smanjenja asimetričnosti.
- **Evaluacija**: Kvalitet klasterizacije ocenjen je pomoću tri metrike: Silhouette Score, Davies-Bouldin Index i Calinski-Harabasz Index.
- **Redukcija dimenzionalnosti**: Korišćena je PCA (Principal Component Analysis).

## Instalacija i pokretanje

Da biste pokrenuli ovaj projekat, potrebno je da imate instaliran Python i sledeće biblioteke:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn
```

## Koraci za pokretanje

1. Klonirajte ili preuzmite projekat.
2. Osigurajte da se dataset nalazi u istom direktorijumu kao i skripta.
3. Pokrenite skriptu ili Jupyter Notebook okruženje.

## Zaključak analize

Rezultati su pokazali da je **K-Means sa 4 klastera** najadekvatniji model za ovaj set podataka. Iako su podaci inicijalno delovali kao homogena masa, vizuelizacija mape gustine (KDE plot) nakon klasterizacije jasno je potvrdila postojanje četiri centra gravitacije, što omogućava preciznu podelu kampanja u četiri različita poslovna segmenta.