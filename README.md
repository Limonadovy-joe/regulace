# Regulace
- Regulace je proces automatického udržování určité veličiny **(regulovaná veličina)** na stanovené hodnotě nebo hodnotách **(referenční nebo požadovaná hodnota)**.
- Protože regulace **působí proti odchylce od požadované hodnoty**, jedná se o **zápornou zpětnou vazbu.**
- Zejména větší **poruchy obvykle způsobí viditelnou odchylku** regulované veličiny, která se jen pomalu zmenšuje, někdy s kolísáním okolo požadované hodnoty

- [Definice](#definice)
- [Regulovana velicina](#regulovana-velicina)
- [Referencni hodnota](#referencni-hodnota)
- [Closed-loop controller](#closed-loop-controller)
- [Open-loop controller](#open-loop-controller)
- [Kladna zpetna vazba](#kladna-zpetna-vazba)
- [Zaporna zpetna vazba](#zaporna-zpetna-vazba)
- [Omezení zpětné vazby](#Omezení-zpětné-vazby)
- [Feed forward](#feed-forward)
- [Nespojite regulatory](#nespojite-regulatory)

- [Prekmit](#prekmit)
    - [Co zpusobuje prekmit](#co-zpusobuje-prekmit) 


# Teorie rizeni
-  Základní dělení je na klasickou **teorii řízení** a na **moderní teorii řízení.**
    -  Klasicka teorie rizeni je založena na **vnějším popisu systémů.**
    -  tento přístup se soustředí na vztahy **mezi vstupními a výstupními signály** a často využívá **přenosovou funkci nebo impulzní odezvu k charakterizaci systému.**
    -  tento přístup je vhodný, když není možné nebo **praktické studovat vnitřní fungování systému.**
    -  **Vlastnosti vnějšího popisu systému:**
        - **Zaměření na vstupy a výstupy**: Vnější popis systému analyzuje, jak systém reaguje na **různé vstupní signály, a jaké výstupní signály produkuje.**  
        - **Použití matematických nástrojů**: Často se používají matematické nástroje jako **Laplaceova transformace, Z-transformace, přenosové funkce a impulzní odezvy k modelování a analýze systému.**
        
-  **Moderní teorii řízení**
    - vznikla v 60. letech, odlišuje se od „klasické teorie, je založena na **stavovém popisu systemu**
    - současné době se oba způsoby popisu silně prolínají a oba se používají při návrhu regulátorů
    - Moderní teorie řízení chápe návrh regulátoru jako **optimalizační úlohu.**

- [Klasicka teorie rizeni](#klasicka-teorie-rizeni)
  - [Prenosova funkce](#prenosova-funkce)
  - [Frekvenční charakteristika](#frekvenční-charakteristika)
  - [Impulsní charakteristika](#impulsní-charakteristika)
  - [Přechodová charakteristika](#přechodová-charakteristika)
  - [Diferenciální rovnice](#diferenciální-rovnice)


- [Moderni teorie rizeni](#moderni-teorie-rizeni)
  - [Optimalizacni uloha](#optimalizacni-uloha)
      - [Ucelova funkce](#ucelova-funkce) 
  - [Stavovy popis systemu](#stavovy-popis-systemu)
      - [Prvni stavova rovnice](#prvni-stavova-rovnice)
  





## Regulovana velicina
- In **control theory**, a process variable (**PV**; also process value or process parameter) **is the current measured value** of a particular part of a process which is being **monitored or controlled**. An example of this would be the temperature of a furnace.
- The **current temperature is the process variable**, while the **desired temperature is known as the set-point (SP).**

- Measurement of process variables is essential in control systems to controlling a process. **The value of the process variable is continuously monitored** so that control may be exerted.
- Four commonly measured variables that **affect chemical and physical processes are:** **pressure, temperature, level and flow.**

![current](https://upload.wikimedia.org/wikipedia/commons/e/ee/Set-point_control.png)
- Block diagram of a **negative feedback control system** used to maintain PV = SP
-  The difference between the **PV and SP is the error (e)**.
- The **SP-PV error** is used to exert control on a process so that **the value of PV equals the value of the SP**. A classic use of this is in the **PID controller**.

![current](https://upload.wikimedia.org/wikipedia/commons/thumb/d/d5/Set-point_control-cs.svg/885px-Set-point_control-cs.svg.png)
- Blokový diagram systému se **zápornou zpětnou vazbou**, který slouží pro udržování požadované hodnoty regulované veličiny řízeného systému ovlivňovaného poruchami pomocí **chybou řízené regulace**.
- **Kladná regulační odchylka znamená, že zpětná vazba je příliš malá (je nutné zvýšení akční veličiny)**;
- **Záporná regulační odchylka znamená, že zpětná vazba je příliš velká (je nutné snížení akční veličiny).**


## Referencni hodnota
- In cybernetics and control theory, **a setpoint (SP set point)** is the **desired or target value for an essential variable, or process value (PV)** of a control system, which may differ from the actual measured value of the variable.
- A setpoint can be any physical quantity or parameter that a control system **seeks to regulate**, such as temperature, pressure, flow rate, position, speed, or **any other measurable attribute**

- The PID controller calculates an **error signal by taking the difference between the setpoint and the current value of the process variable.** Mathematically, this error is expressed as:
![formula](https://wikimedia.org/api/rest_v1/media/math/render/svg/9fbb3562ba86333446b6cb4d281451429c7f218f)
- where **e(t)** is the error at a given time t, **SP** is the setpoint, **PV(t)**  is the process variable at time t.
- The PID controller uses this **error signal** to determine how to **adjust the control output to bring the process variable as close as possible to the setpoint** while **maintaining stability and minimizing overshoot(prekmit)**.

- **Departure(odchylka) of such a variable from its setpoint** is one basis for error-controlled regulation using negative feedback for automatic control


## Closed-loop controller
- closed-loop controller or **feedback controller** is a control loop which incorporates feedback, in contrast to an open-loop controller or non-feedback controller.
- **uses feedback to control states or outputs of a dynamical system.**
- **process inputs (e.g. voltage applied to an electric motor)** have an effect on the process outputs **(e.g., speed or torque of the motor)**, which is measured with sensors and processed by the controller; **the result (the control signal) is "fed back" as input to the process, closing the loop**
- **Open-loop control systems** do not make use of feedback, and run only in pre-arranged ways.

## Open-loop controller
- non-feedback controller, is a control loop part of a control system in which the **control action is independent of the "process output"**, **which is the process variable that is being controlled.**
- It does not use **feedback to determine if its output has achieved the desired goal of the input command or process setpoint.**

## Kladna zpetna vazba
- Kladná zpětná vazba nastává, **když systém reaguje na regulační odchylku způsobem, který tuto odchylku zvětšuje.**
- Pokud zvýšení hodnoty, přiváděné z výstupu na vstup, způsobí další zvýšení hodnoty na výstupu, jedná se o kladnou zpětnou vazbu.
- Kladná zpětná vazba se obvykle využívá **k zesílení nebo k akceleraci žádoucích jevů.** 
- **Akustická zpětná vazba**
  -  je zvláštní druh kladné zpětné vazby, ke kterému dochází, pokud **existuje zvuková smyčka mezi zvukovým vstupem (například mikrofonem nebo kytarovým snímačem) a zvukovým výstupem (například reproduktorem).**
  -  je signál zachycený mikrofonem zesílen(zesilovacem) a vyzářen reproduktorem.
 
## Zaporna zpetna vazba
- Záporná zpětná vazba nastává, **když systém reaguje na regulační odchylku způsobem, který tuto odchylku zmenšuje.**
- Pokud zvýšení hodnoty, přiváděné z výstupu na vstup, způsobí snížení hodnoty na výstupu, jedná se o zápornou zpětnou vazbu.
- Tento druh vazby se využívá v regulační technice pro udržení stálých parametrů systémů, neboť v případě výskytu výchylky (regulační odchylky) od ustáleného stavu dokáže zpětná vazba působit proti této výchylce a potlačit ji.

## Omezení zpětné vazby
- výstup procesu, který je ovlivněn zpětnou vazbou, **působí v každé iteraci na jeho vstup**, naznačuje, že celkový **stav zpětnovazební veličiny se bude zvyšovat nebo snižovat geometrickou řadou**, čili bude mít exponenciální průběh.
- Geometrická posloupnost je druh matematické posloupnosti, kde každý člen kromě prvního je **stálým násobkem předchozího členu**. Tento násobek se nazývá **kvocient geometrické posloupnosti**
- Geometrickou posloupnost s nezápornými členy lze chápat jako **zúžení exponenciální funkce na obor přirozených čísel**

V reálném světě průběh veličin, které jsou regulovany pomoci zpětné vazby,bude omezen ve své:
- **plynulosti**
  - exponenciální průběh je ideálním případem, kdy se zpoždění jednotlivých iterací limitně blíží k nule.
  - **Místo hladké exponenciely bude reálný průběh více „schodovitý“** (každý schod na grafu bude představovat jednu iteraci), avšak přesto bude mít exponenciální charakter.
- **konečnosti**
  - u záporné zpětné vazby dříve či později dojde **k setření rozdílu mezi ještě klesající veličinou a její nulovou hodnotou**.
  - Systém je navržen tak, aby s časem odchylku úplně eliminovat, tedy aby **aktuální hodnota veličiny konvergovala k požadované hodnotě.**
  - U kladné zpětné vazby se exponenciálně rostoucí veličina musí dříve či **později střetnout s některou z mezí systému.**

## Feed forward
- **dopredne** rizeni
- a feedforward control system is a control system that **uses sensors to detect disturbances affecting the system** and **then applies an additional input to minimize the effect of the disturbance(sum).**
- A control system which has only **feed-forward behavior responds to its control signal in a pre-defined way without responding to the way the system reacts**; it is in contrast with a system that also has **feedback, which adjusts the input to take account of how it affects the system**, and how the system itself may vary unpredictably.
- In a feed-forward system, the **control variable adjustment is not error-based**. Instead it is based on knowledge about the process in the form of a mathematical model of the process and knowledge about, or measurements of, the process disturbances


![img](https://upload.wikimedia.org/wikipedia/en/c/c7/Control_Systems.png)



## Nespojite regulatory
- Regulátor, jehož **výstupní signál neprobíhá spojitě v závislosti na vstupním signálu.**
    - mají výstup, který může nabývat **pouze omezeného počtu hodnot**, obvykle dvou (zapnuto/vypnuto) nebo tří (např. nízký, střední, vysoký). Nejznámějším příkladem nespojitého regulátoru je **dvoustavový (on/off) regulátor.** 
- Charakteristickou vlastností nespojitého regulátoru je to, že **akční veličina - u(t)** může nabývat pouze **omezených počtů hodnot**.
- Nejčastěji v praxi používáme regulátory dvoupolohové. Vzácněji se používají i regulátory vícepolohové.
- **Charakteristiky nespojitého regulátoru:**
    - **Nelineární odezva:** **Výstup regulátoru se mění skokově, což vede k nelineární odezvě.**
    - **Hysterze:** Často je přidána hystereze, **aby se zabránilo příliš častému přepínání mezi stavy**, což by vedlo k opotřebení mechanických částí.
    - v termostatech nebo ve spínání topných těles 
- Dvoupolohový regulátor se od spojitého liší tím, **že neovládá akční člen spojitě**, ale pouze jej **přestavuje do jedné ze dvou krajních mezních poloh.**
- Regulátor je vybaven definovanou **necitlivostí** na změnu regulované veličiny v **rozmezí ± δ kolem žádané hodnoty**. **Pásmo necitlivosti je nutné proto, aby akční člen nekmital příliš rychle a často** a tím pádem se rychle neopotřeboval nebo se zničil.


## Prekmit
- **overshoot**
 - dočasné překročení požadované hodnoty (referencni hodnoty) výstupní veličiny regulovaného systému **během přechodového děje**
- Překmity jsou často nežádoucí, protože mohou způsobit nestabilitu nebo snížit přesnost systému.
- V oblasti automatizace a regulace systémů jsou **překmity důležité pro charakterizaci přechodového procesu.**
- **Přechodový proces,dej** se měří pomocí **přechodové charakteristiky**. Přechodová charakteristika popisuje, jak se **výstup systému mění v čase v reakci na krokovou změnu vstupu -  náhlou změnu vstupní veličiny z jedné konstantní hodnoty na jinou.**
- Vyjádřený procentuálně – **relativní překmit κ,** také **přeregulování**, je maximální hodnota minus ustálená hodnota vydělená ustálenou hodnotou

- **Dynamická Odezva**
    - Překmit se objevuje během dynamické odezvy systému, kdy dochází k **přechodu ze stavu mimo rovnováhu do nového ustáleného stavu.**
- **Druhého Řádu:**
    - **V lineárních systémech druhého řádu** je překmit často analyzován pomocí **přenosové funkce a charakteristických kořenů (pólů) systému**. Překmit závisí na parametrech, jako je **tlumící faktor (ζζ) a přirozená frekvence (ωnωn​).**
- **Přenosová Funkce:**
    - **U lineárních časově invariantních (LTI) systémů** je přenosová funkce **G(s)** často analyzována pro určení překmitu pomocí **inverzní Laplaceovy transformace.**
 
### Co zpusobuje prekmit
- Překmit u PID regulátoru je jev, kdy **výstup systému překročí svou požadovanou hodnotu (nastavenou hodnotu) a následně se vrací zpět.**

- **Vysoká proporční složka (Kp)**:
    - Tato složka je **přímo úměrná chybě a její účinek je řízen konstantou Kp.**
    - Proporční složka PID regulátoru **reaguje přímo úměrně k chybě (rozdíl mezi požadovanou a aktuální hodnotou)**. Pokud je hodnota Kp​ příliš vysoká, regulátor bude **reagovat příliš agresivně na chybu**, což způsobí rychlé změny ve výstupu a může vést k překmitům.
    - Kvůli rychlé reakci na chybu může vysoké Kp​ způsobit **oscilace okolo požadované hodnoty**. Tyto oscilace jsou důsledkem toho, že systém je příliš citlivý

- **Příliš nízká nebo vysoká integrační složka (Ki):**
    - Integrační složka se snaží **eliminovat ustálenou chybu tím, že kumuluje chybu v čase.** Pokud je hodnota **Ki​ příliš vysoká, regulační akce se může stát příliš silnou - jak často a jak silně se bude akcni clen (např. topení) spouštět v závislosti na kumulaci chyby v čase** a může způsobit překmit. Na druhé straně, pokud je Ki​ příliš nízká, systém může **být pomalý a nebude dostatečně reagovat na změny.**
    - **V diskrétním čase (kde počítáme hodnoty v konkrétních časových krocích, posloupnost)** se to vyjadřuje jako suma. napr Uvažujme regulátor, který **vzorkuje chybu každou sekundu (Δt=1s):**

- **Nedostatečná derivační složka (Kd):**
    - Derivační složka **reaguje na rychlost změny chyby** a **pomáhá tlumit oscilace a překmit**. Pokud je Kd příliš nízká, systém nebude dostatečně tlumený, což může vést k překmitům. Naopak, **příliš vysoká hodnota Kd​ může způsobit nadměrné tlumení a zpomalit odezvu systému**


