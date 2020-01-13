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
                                                 
                                                     
