# Regulace
- [Definice](#definice)
- [Regulovana velicina](#regulovana-velicina)
- [Referencni hodnota](#referencni-hodnota)

# Teorie rizeni
- [Prekmit](#prekmit)



## Definice
- Regulace je proces automatického udržování určité veličiny **(regulovaná veličina)** na stanovené hodnotě nebo hodnotách **(referenční nebo požadovaná hodnota)**.
- Protože regulace **působí proti odchylce od požadované hodnoty**, jedná se o **zápornou zpětnou vazbu.**
- Zejména větší **poruchy obvykle způsobí viditelnou odchylku** regulované veličiny, která se jen pomalu zmenšuje, někdy s kolísáním okolo požadované hodnoty 
- 

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
- **Záporná odchylka znamená, že zpětná vazba je příliš velká (je nutné snížení akční veličiny).**


## Referencni hodnota
- In cybernetics and control theory, **a setpoint (SP set point)** is the **desired or target value for an essential variable, or process value (PV)** of a control system, which may differ from the actual measured value of the variable.
- A setpoint can be any physical quantity or parameter that a control system **seeks to regulate**, such as temperature, pressure, flow rate, position, speed, or **any other measurable attribute**

- The PID controller calculates an **error signal by taking the difference between the setpoint and the current value of the process variable.** Mathematically, this error is expressed as:
![formula](https://wikimedia.org/api/rest_v1/media/math/render/svg/9fbb3562ba86333446b6cb4d281451429c7f218f)
- where **e(t)** is the error at a given time t, **SP** is the setpoint, **PV(t)**  is the process variable at time t.
- The PID controller uses this **error signal** to determine how to **adjust the control output to bring the process variable as close as possible to the setpoint** while **maintaining stability and minimizing overshoot(prekmit)**.

- **Departure(odchylka) of such a variable from its setpoint** is one basis for error-controlled regulation using negative feedback for automatic control


////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////



                                                                   Teorie rizeni



////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////

## Prekmit
- a 












