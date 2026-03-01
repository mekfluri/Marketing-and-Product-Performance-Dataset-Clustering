Segmentacija Marketinških Kampanja pomoću Klasterizacije
Opis projekta
Ovaj projekat fokusiran je na analizu i segmentaciju baze od 10.000 marketinških kampanja. Cilj je bio da se primenom tehnika mašinskog učenja (nevođeno učenje) identifikuju ključne grupe kampanja na osnovu njihovih performansi i budžeta, kako bi se omogućila efikasnija alokacija resursa i personalizacija marketing strategija.

Ciljevi analize
Identifikacija optimalnog broja segmenata unutar gustog skupa podataka.

Poređenje performansi različitih algoritama za klasterizaciju.

Vizuelizacija strukture podataka pre i nakon obrade radi lakše interpretacije poslovnih rezultata.

Korišćeni algoritmi i metode
U okviru projekta testirano je pet različitih modela kako bi se pronašlo najstabilnije rešenje:

K-Means (k=4): Glavni model koji je pokazao najvišu matematičku preciznost.

Mini-Batch K-Means: Brža verzija algoritma korišćena za proveru stabilnosti granica klastera.

Hijerarhijska klasterizacija (Ward metoda): Korišćena za analizu unutrašnje strukture i hijerarhije podataka.

DBSCAN: Testiran radi identifikacije prirodne gustine i izolacije šuma (outlier-a).

Mean Shift: Korišten za automatsko detektovanje centara gustine bez unapred definisanog broja grupa.

Metodologija rada
Preprocesiranje: Izvršena je standardizacija podataka i logaritamska transformacija ključnih varijabli (Budget, Revenue) radi smanjenja asimetričnosti.

Evaluacija: Kvalitet klasterizacije ocenjen je pomoću tri metrike: Silhouette Score, Davies-Bouldin Index i Calinski-Harabasz Index.

Redukcija dimenzionalnosti: Korišćena je PCA (Principal Component Analysis) metoda za prebacivanje podataka u 2D prostor radi vizuelizacije.

Instalacija i pokretanje
Da biste pokrenuli ovaj projekat, potrebno je da imate instaliran Python i sledeće biblioteke:

Bash
pip install pandas numpy matplotlib seaborn scikit-learn
Koraci za pokretanje:
Klonirajte ili preuzmite projekat.

Osigurajte da se dataset nalazi u istom direktorijumu kao i skripta.

Pokrenite skriptu ili Jupyter Notebook okruženje.

Zaključak analize
Rezultati su pokazali da je K-Means sa 4 klastera najadekvatniji model za ovaj set podataka. Iako su podaci inicijalno delovali kao homogena masa, vizuelizacija mape gustine (KDE plot) nakon klasterizacije jasno je potvrdila postojanje četiri centra gravitacije, što omogućava preciznu podelu kampanja u četiri različita poslovna segmenta.