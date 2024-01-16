# dip225-PROJEKTS

PROJEKTA MĒRĶIS/UZDEVUMS

Pirms es sāku skaidrot, savu projekta mērķi, es gribu izskaidrot savu ideju un kā tā radās. Ikdienā kā hobiju, man patīk izšūt, un pašlaik es izšuju ļoti apjomīgu darbiņu jeb gleznu, kurš ir 45 x 34cm liels, ar 60 krāsām un ar 76800 šuvēm jeb izšūtiem kvadrātiņiem. Vienu dienu kamēr es izšuvu un paralēli vajadzēja izdomāt projekta darbam ideju, man prātā ienāca jautājums, cik procentuāli daudz, pabeidzot vienu krāsu, es esmu izdarījusi no visa darba. Un tā lai to man pašai nevajadzētu katru reizi, kad es pabeidzu krāsu, skaitīt es izdomāju izstrādāt programmu, kas to izdarīs manā vietā, jo Jūs varat iedomāties cik liels man apgrūtinājums ir katru reizi skaitīt procentus tādam apjomīgam darbam. Šim projektam klāt ir pievienots attēls, kurā ir tabula ar informāciju, kuru es pārrakstīju excel failā un ar kuru es visu šo projekta darbu strādāju, šī lapa nāca klāt manam izšuvuma komplektam.

Projekta mērķis bija izstrādāt programmu, kas manā vietā procentuāli izrēķinātu manu paveikto darbu. Programmas uzdevums bija sekojošs, Terminālī man ir jāievada cik daudz krāsas es vēlos ievadīt, un tad es ievadu visas paveiktās krāsas, un tad programma izrēķina cik procentuāli es esmu pabeigusi darbu. Tā lai šo uzdevumu paveiktu, es izveidoju excel failu, kur es manuāli ievadīju visu informāciju par krāsām, darba lapā "Sheet1" no pievienotās bildes, krāsas cipars, pašu krāsu, krāsas diegu skaitu un cik daudz kvadrātiņus katra krāsa aizņem. Tad es tajā pašā excel failā izveidoju atsevišķu darbalapu, kurā programma ievietoja krāsas ciparu, kurus es iepriekš ievadīju terminālī. Tad programma salīdzina abas darba lapaskrāsas numurus un ja "Done" darbalapas numuri sakrīt ar "Sheet1" darbalapas krāsas numuriem, tad saskaita krāsas kvadrātiņus un ar formulu((pabeigtās krāsas kvadrātiņi kopā/ visi krāsas kvadrātiņi kopā)*100), šī formula man aprēķināja procentus no paveiktā darba, un rezultātu izvada terminālī. Pie sava koda es esmu papildus pievienojusi iekomentētu kodu, kurš aprēķina cik procentus no visa darba būs izdarīts, ja es pabeigšu vienu konkrēti izvēlēto krāsu, piemēram, sarkanu. Šo papildus kodu es izveidoju priekš sevis tīri intereses pēc, jo izšujot tas man arī bija ienācis prāta, cik procentuāli daudz aizņem viena krāsas grupa.



IZMANTOTĀS PYTHON BIBLIOTĒKAS

Savā projektā es izmantoju tikai openpyxl bibliotēku, ar kuras palīdzību es varēju automatizēt un strādāt ar exceli. Ar šo bibliotēku, es nolasīju exceli, un pievienoju ievadīto informāciju no termināla jaunā darba lapā, un izmantoju to informāciju, lai izpildītu savu projekta uzdevumu.
Lai iepazītos ar visām bibliotēkas metodēm, es izgāju cauri bibliotēkas dokumentācijai(https://openpyxl.readthedocs.io/en/stable/api/openpyxl.html), un atradu metodēs, kuras man palidzētu tikt līdz rezultātam. Es protams arī izmantoju citas mājaslapas, kuras man palīdzēja uztaisīt savu programmu, piemēram, stackoverflow, geeksforgeeks utt.


IZMANTOTĀS METODES

Kā jau minēju iepriekš daļa no manām izmantotajām metodēm ir no openpyxl bibliotēkas, piemēram, load_workbok() un cell(), bet es arī izmantoju metodēs, kuras mēs bijām jau lietojuši kursa gaitā, piemēram, range(), sum(), round() utt.
Zemāk es aprakstīšu, katru metodi, ko es izmantoju, un kāpēc es to izmantoju:

load_workbook() - es izmantoju, lai ielādētu savā programmā jau iepriekš izveidotu, gatavu excel failu;

wb['Sheet1']  - es izmantoju, lai tiktu klāt specifiskai darba lapai;

max_row - es izmantoju, lai noteiktu savā excel failā cik ir maksimālais rindu skaits, un lai tālāk strādātu ar dotajiem datiem;

append()  - es izmantoju, lai pievienotu kādu noteiktu vērtību sarakstam;

range() - es izmantoju, lai pateiktu savai programmai, kādā intervālā nolasīt informāciju;

cell() - es izmantoju, lai piekļūtu klāt citas darba lapas šūnām un atkārtotā ciklā pievienotu tajās šūnās manas ievadītās vērtības no termināla;

value - es izmantoju, lai piešķirtu vērtībām tai attiecīgo vērtību, piemēram, man vajadzēja, lai manas jauni ievadītās vērtības, kuras tika pievienotas jaunajai darbalapai tiktu nolasītas kā int skaitli, ja man būtu ievadīta string vērtība tad ar šo metodi tā arī tiktu nolasīta kā string vērtība;

sum() - es izmantoju, lai saskaitītu gan visas D kollonas vērtības, kas bija visas krāsas kvadrātiņi(failā ar nosaukumu "Stitches"), un man arī vajadzēja sasummēt terminālī ievadīto kvadrātiņu summu, lai es varētu izrēķināt procentus paveiktajam darbam;

round()  - es izmantoju pašās beigās, lai noapaļotu procentus, vienkārši, lai gala rezultāts būtu, nosacīti, skaistāks un precīzāks;

save() -  šo metodi es izmantoju, lai saglabātu savu excel failu, pēc tā brīža kad programma no termināla ievadīja skaitļus jaunajā darba lapā(ar nosaukumu "Done");

close() - es izmantoju, lai pēc programmas palaišanas tā pēc rezultātu izvadīšanas aizver excel failu.
