# architecture
1.Στο αρχείο starter_se.py περιλαμβανονται 3 μοντελα επεξεργαστων  το  Atomic που  εχει AtomicSimpleCpu επεξεργαστη και καθολου μνημη cache, το Minor που εχει ΜinorCPU επεξεργαστη και  μνημες  cache l1 instructions ,l1 data, walkcache και l2, καθως και το HPI  με επεξεργαστη τον  HPI.HPI  και μνημες  HPI.HPI_ICache, HPI.HPI_DCache, HPI.HPI_WalkCache,  HPI.HPI_L2.
Στη συνεχεια υπαρχει η κλαση SimpleSeSystem ,η οποια δημιουργει ενα βασικο συστημα επεξεργαστη και θετει ορισμενες χαρακτηριστικες παραμετρους ως εξής :  cache_line_size = 64 (μηκος της μνημης cache) , συστημα αναφορας τασης : VoltageDomain(voltage="3.3V") ,συστημα αναφορας συχνοτητας επεξεργαστη :SrcClockDomain(clock="1GHz", )

Στο αρχειο config.ini παρατηρω οτι υπαρχουν τα εξης στοιχεια:
time_sync_period=100000000000
cache_line_size=64
voltage=3.3        
Στο αρχειο config.json  υπαρχουν τα εξης στοιχεια :

"voltage": [
                3.3
            ],      
                    "cache_line_size": 64, 
                                  
                                  "time_sync_period": 100000000000,

Μεσα στη main και σαν default  συστημα εξομοιωσης υπαρχει το atomic  το οποιο θετει τα εξής χαρακτηριστικά στο σύστημα
συχνοτητα επεξεργαστη 4GHz , αριθμος πυρηνων 1 ,τεχνολογια μνημης DDR3 @1600MHz 8x8 ,καναλια μνημης 2 ,μεγεθος μνημης 2 GigaByte ,memory rank none




3.Τρέχοντας το προγραμμα μου σε default ρυθμισεις και σε MinorCPU προκύπτουν τα εξης :
   Numbers of second simulated 0.000050
   
  Για 2.5 GHz  Numbers of second simulated  0.000045  
  
 Στα 2.5 GHz και για TimingSimpleCPU  εχουμε:
 Numbers of second simulated  0.000059 
    
 Στα 1 GHz για TimingSimpleCPU εχουμε :
   Numbers of second simulated 0.000063 
   
   Στα 2.5 η διαφορα στους  χρονους εκτελεσης ειναι 0.000014
   
   Στα 1 η διαφορα ειναι 0.000013
  
