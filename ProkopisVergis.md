# Αποθετήριο του μαθήματος: Ανάλυση Δεδομένων

## Ονοματεπώνυμο
## [Προφίλ Github: aggelos2000430](https://github.com/aggelos2000430)

| Εβδομάδα | Παραδοτέα | Ολοκλήρωση Παραδοτέου :heavy_check_mark: |
| --- | --- | --- |
| 1 | Δημιουργία προφίλ στην πλατφόρμα + Fork του αποθετηρίου του μαθήματος| :heavy_check_mark: |
| 2 | Δημιουργία του αρχείου .md στο προφίλ σας και αντιγραφή του πίνακα παραδοτέων στο προσωπικό σας αρχείο με τίτλο το ονοματεπώνυμο σας με λατινικούς χαρακτήρες που αποτελεί και την τελική αναφορά του μαθήματος| :heavy_check_mark: |
| 3 | Συγγραφή μιας σύντομης περιγραφής για την σημασία της ανάλυσης δεδομένων στον σύγχρονο κόσμο | :heavy_check_mark: |
| 4 | Εκτέλεση του κώδικα στο σύστημά σας | :heavy_check_mark: |
| 5 | Αντιγραφή του python κώδικα και λεπτομερής σχολιασμός του, εντός της αναφοράς σας | :heavy_check_mark: |
| 6 | Προφορική υποστήριξη της αναφοράς σας | :heavy_check_mark: |


## Παραδοτέο 3
Η ανάλυση δεδομένων είναι η διεξοδική μελέτη ενός συνόλου πληροφοριών, στόχος του οποίου είναι η εξαγωγή συμπερασμάτων που επιτρέπουν σε μια εταιρεία ή οντότητα να λάβει απόφαση.

## Παραδοτέο 5
with open('sorting_runtimes.txt', 'r') as file: (opens the sorting_runtimes.txt file)
    data = file.read().splitlines() (reads data fron txt file)

runtimes = {}

for i in range(0, len(data), 8): (loop)
    algorithm = data[i].split(' - ')[0] (sets algorithm equal to data seperated by '-'
    runtime = float(data[i+1].split(' - ')[1].split(' ')[0]) (sets runtime equal to decimal)
    runtimes[algorithm] = runtimes.get(algorithm, 0) + runtime (runs a function)

for algorithm, runtime in runtimes.items():
    avg_runtime = runtime / 10 (gives an avcerage time of each sorting algorithm)

fastest_algorithm = min(runtimes.items(), key=lambda x: x[1]) (sets each time the quickest algorithm)
print(f"The fastest sorting algorithm is {fastest_algorithm[0]} with an average runtime of {fastest_algorithm[1]/10:.6f} seconds.") 

