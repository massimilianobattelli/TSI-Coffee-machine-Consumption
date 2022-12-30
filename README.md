# LabBigData

Progetto di Laboratorio di Big Data, Data Minings, e Data Analytics

Il file 'Data.csv' contiene i dati relativi al consumo di energia elettrica della macchina del caffè di Alexide.

La colonna Date rappresenta data e ora della registrazione del sensore. Si noti che le date sono espresse in UTC. Per convertirle nella timezone locale utilizzare
df['Date'] = pd.to_datetime(df['Date'], utc = True).dt.tz_convert('Europe/Berlin')

La colonna Energy rappresenta il consumo di energia totale, espresso in Wmin (Watt minuto), a partire dall'accensione del sensore. Si noti che il sensore è stato riavviato diverse volte nel periodo di osservazione e, a seguito di ciascun riavvio, il conteggio è ripartito da 0.

La colonna *Topic** rappresenta il topic del messaggio mqtt ricevuto dal sensore.

Obiettivo:
  - Rappresentare i consumi totali in kWh (kiloWatt ora) con una heatmap che abbia sull'asse x le ore del giorno e sull'asse y il giorno della settimana.
