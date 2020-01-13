# Circuite-digitale-CMOS-consumul-de-putere-si-metode-de-minimizare-a-consumului-de-putere
Acest proiect prezinta o perspectiva asupra consumului de putere in circuitele digitale CMOS si cateva tehnici de optimizare a consumului de putere. 

#Introducere

Portile logice sunt realizate cu tranzistori cu efect de camp (MOS) complementari (C) si reprezinta elementele fundamentale de constructie ale circutelor logice moderne. Tehnologia ce foloseste circuite cu tranzistori MOS complementari este numita CMOS, si permite obtinerea la ora actuala a celor mai mari viteze la o putere consumata relativ redusa, fiind folosita in realizarea tuturor microprocesoarelor moderne.
Disiparea puterii este definită ca energia furnizată de la sursă la sistem.Odata cu creșterea substanțială a calculatoarelor portabile, disiparea puterii a devenit o preocupare majoră acum. Aceasta duce la o creștere a densității cipului și frecventa de operare. Efectul direct al creșterii puterii disipate este o creștere a temperaturii, care în cele din urmă duce la o defecțiune a dispozitivului, cu excepția cazului în care este îngrijit.Acest lucrarea discută despre diferite surse de disipare a puterii și tehnici probabile de reducere a puterii la nivel de circuit si dispozitiv.


#Consumul de putere

Două componente determină consumul de energie electrică într-un circuit CMOS:
            - consumul de putere statica;
            - consumul de putere dinamica

Dispozitivele CMOS au un consum static foarte scăzut, care este rezultatul curentului de scurgere. Acest consum de energie apare când toate intrările sunt ținute la un anumit nivel logic valid și circuitul nu se află în stări de încărcare. Dar, când comutata la o frecvență mare,consumul dinamic de energie poate contribui semnificativ la consumul total de energie.Consumul de putere determină consumul de energie de la sursa de alimentare şi provoacă încălzirea cipului în timpul funcţionării.Cunoaşterea acestui parametru este importantă pentru a calcula capacitatea sursei de alimentare, durata de viaţă a bateriei, dimensionarea liniilor de alimentare, modul de incapsulare şi modalitatea de răcire a capsulei
Consumul de putere are trei componente:
            -Pdyn – puterea dinamică disipată în urma încărcări şi descărcări capacităţi de sarcină
            -Pdp – puterea dinamică disipată datorită conducţiei simultane a tranzistoarelor nMOS şi pMOS
            -Pstat – puterea statică disipată datorită curentului care circulă între liniile de alimentare în regim static de funcționare
            
                                                     Ptot=Pdyn+Pdp+Pstat
 #Puterea statica    
 
 Pe durata starilor stabile unul dintre tranzistoare este blocat si prin urmare nu exista cale de curent inchisa intre VDD si GND.Ideal, inversorul nu consuma putere.In cazul real, exista un curent de scurgere prin jonctiunile drena-substrat sursasubstrat care sunt polarizate invers, precum si un curent de sub-prag prin tranzistoare.       
Consumul de energie statică este produsul curentului de scurgere al dispozitivului și al tensiunii de alimentare. Consumul total de energie statică,PS, poate fi obținut astfel:

                                      PS= (curent de scurgere)x(tensiune de alimentare)  
                              
 
Curentul de scurgere ICC, împreună cu tensiunea de alimentare, determină consumul de energie statică în dispozitivele CMOS. Acest consum de energie statică este definit ca fiind silențios,PS si poate fi calculat astfel:

                                                       Ps= Vcc x Icc
                                                       
unde Vcc este tensiunea de alimentare,iar Icc este curentul prin dispozitiv.


#Puterea dinamica

 Consumul de energie dinamică al unui circuit CMOS este calculat prin adăugarea consumului de energie tranzitorie (PT) și
consumul de energie cu sarcină capacitivă (PL).

Consumul de energie tranzitorie

Consumul de energie tranzitorie se datorează curentului care curge doar atunci când tranzistoarele dispozitivelor trec de la o stare logică la alta. Acesta este rezultatul curentului necesar pentru încărcarea nodurilor interne (curentul de comutare), plus curentul
(curent care curge de la VCC la GND când tranzistorul cu canal p și tranzistorul cu canal n se pornesc în același timp în timpul tranziției logice). Frecvența cu care se comută dispozitivul, plus timpii de creștere și cădere a semnalului de intrare cat si nodurile interne ale dispozitivului, au un efect direct asupra duratei curentului de "spike". Pentru tranziții rapide la intrare,curentul porții este neglijabil în comparație cu curentul de comutare. Din acest motiv, curentul de alimentare dinamic este guvernat de capacitanța internă a circuitului și de curentul de încărcare și descărcare a capacitatii de încărcare.
Consumul de energie tranzitorie poate fi calculat astfel:

                                                        Pt=Cpd x Vcc^2 x fi x Nsw
                                                        
unde Pt=consumul de energie tranzitorie,Vcc= tensiunea de alimentare,fi= frecventa semnalului de intrare,Nsw=numarul de biti,Cpd=capacitatea puterii disipate dinamice

Consumul de energie al sarcinii capacitive

Puterea suplimentară este consumată la încărcarea capacității de încărcare externă și depinde de frecvența de comutare. Următoarea ecuația poate fi utilizată pentru a calcula această putere dacă toate ieșirile au aceeași sarcină și se comută la aceeași frecvență de ieșire.

                                                         PL= Cl x Vcc^2 x fo x Nsw
                                                    
PL= consumul de putere al sarcinii capacitive, Vcc=tensiunea de alimentare, fo=frecventa semnalului de iesire, CL= capacitatea externa,Nsw=numarul total de biti al comutarii la iesire.



# Metode de optimizare a consumului de putere

Majoritatea optimizărilor descrise în cele ce urmează se concentrează pe minimizarea puterii activității de comutare la diferite niveluri de abstractizare. În circuitele VLSI care folosesc porți logice bine concepute, puterea activitatii de comutarereprezintă peste 90% din puterea totală disipata.


#Optimizare la nivel de circuit

Tehnicile de optimizare sunt realizate pentru a reduce puterea activității de comutare a porților logice individuale și a circuitelor combinaționale la nivel de tranzistor.

Optimizarea in cazul unui design complex ai gate-ului:

In cazul unui design mai complex,de exemplu f=(a+b)c, se pot face optimizari privind plasarea individuala a tranzistorilor din poarta.De exemplu,partea N al unei porti CMOS implementand functia de mai sus,perechea de tranzistori paraleli a+b poate fi conectata la poarta de iesire.

Optimizare la nivel de dimensiune al transistorului:

Intr-un circuit combinational, dimensiunea tranzistorilor poate avea un impact major asupra delayului circuitului cat si al puterii disipate. Daca  tranzistorii dintr-o anumita poarta sunt numerosi,atunci delayul portii va creste,la fel si puterea disipata.Solutia este gasirea unui numar potrivit de tranzistori care minimizeaza puterea disipata chiar daca este o problema mai dificila.




