# Unit 5 : Power Supplies

### SMPS

- **Switch mode power supplies (SMPSs)** are used in range of application as an efficient and effective source of power.
- This is in major part of their efficiency.
- For anybody still working on a desktop, look for the fan in the CPU that’s where the SMPS is .
- SMPS offers advantages in size, weight , cost , efficiency and overall performance.
- Basically, it is a device in which energy conversion and regulation is provided by power semiconductors that are continuously switching on and off.

### Functional Block Diagram of SMPS

![smps.PNG](Unit%205%20Power%20Supplies/smps.png)

- A switch regulator foes the regulation in the SMPS. A series switching element turns the current supply to a smoothing capacitator on and off. The voltage on the capacitator controls the time the series element is turned.
- The continuous switching maintains the voltage at a required level.
- **Design Basics** ➖
    - AC power first passes through fuses and a line filter. Then it is rectified by a full-wave bridge rectifier.
    - The rectified voltage is next applied to the power factor correction (PFC) pre-regulator followed by the downstream DC-DC converter(s).
    - Most computers and small appliances use the International Electrotechnical Commission (IEC) style input connector.
    - As for output connectors and pinouts, except for some industries, such as PC and compact PCI, in general, they are not standardized and are left up to the manufacturer.

### Signals

- The variation of dependent parameters and independent parameters constitutes a signal.
- Signal can be also defined as a singled value function of time that conveys information.
- It may be of real value or complex value.
- Signals may be of different types : audio signals, video signals or data signals, etc.
- **Classification of Signals :**
    - Patterns of Signals :
        - **Continuous Time & Discrete Time Signal** -
            - In continuous the signal, the independent variable is a continuous function. Therefore, the amplitude of the signal exists continuously over the range of time.
            - In Discrete time signal, The independent function is discrete in type. Therefore, they are just defined only at discrete interval of time. A discrete time signal is a sampled form of continuous time signal. When each sample is quantized into a finite series of value, we get a digital signal.
            - CT Signal → Sampling → DT Signal → Quantization → Digital Signal.
        - **Deterministic & Random Signal -**
            - Deterministic signal are those which can be determined by a simple algebraic equation or tabular form or by graphical representation.
            - That is the solution of which are consistent.
            - Random signals are those which cannot be determined by a simple algebraic equation or tabular or graphical representation.
            - They are non deterministic and inconsistent. For ex : noise signals.
        - **Periodic and Non Periodic Signal** -
            - Periodic signal is that which repeats itself over a certain interval of time regularly. A signal x(t) is said to be periodic with T if : x (t + T) = x(t).
            - If the signal violates the above condition, then it is called non periodic signal i.e x (t + T)  ≠ x(t).
        - **Real & Complex Signal -**
            - Any signal x(t) is said to be real signal x R(t) if it takes the real number system.
            x(t) → R(t) - R (Real Number).
            - Complex signals take the value in complex number system.
            x(t) → x C(t) -C (Complex Number).

### Power Supply Characteristics

- **Efficiency :** Ratio  of output to input power (in %), measured at a given load current with nominal line conditions.
- **Line Regulation :** Change in value of dc output voltage resulting from a change in ac input voltage, specified as the change in +- mV or +- %.
- **Load Regulation :** Change in value of dc output voltage resulting from a change in load from open-circuit to maximum-rated output current , specified as the change in +- mv or +- %.
- **Rated Wattage :** This the nominal wattage that the power supply can deliver. Nominal wattage is a composite figure, determined by multiplying the amperages available at each of the several voltages supplied by a PC power supply by those voltages.
- **Ripple :** Rectifying and filtering a switching power supply’s output results in an ac component (ripple) that rides on its dc output. Ripple frequency is some integral multiple of the converter’s switching frequency, which depends on the converter topology.

### Power Problems

- **Surges / Spike :** Surges and spikes are short-term voltage increases. They are typically caused by lightning strikes, power outages, short circuits or malfunctions caused by power utility companies. They cause data corruption, catastrophic and costly equipment damage and incremental damage that degrades equipment performance and shortens its useful lifespans.
    - Common causes of surges/spikes :
        - Utility company loadshifting
        - Miswired electrical systems
- **Line Noise :** Line noise refers to distortion on AC, telephone/ DSL, network or coaxial lines caused by electromagnetic interference (EMI) and Radio Frequency Interference. Line noise is unavoidable and will appear on every signal at some point, though it is not always detrimental or even noticeable. It causes incremental electronic circuit damage, data corruption, audio/video quality problems and confusion between system components.
    - Common causes of line noise :
        - Radio transmissions
        - High voltage powerlines
        - Severe weather
        - Fluorescent lights
- **Brownout / Undervoltage / Sag :** A brownout is a voltage deficiency that occurs when the need of power exceeds power availability. Brownouts typically last for few minutes, but can last up to several hours, as opposed to short-term fluctuations like surges or spikes. They are caused by the disruption of an electrical grid and may be imposed by utility companies, when there is an overwhelming demand for power.
    - Brownouts more common than blackouts cause equipment failures, incremental damage, decreased equipment stability and data loss.
    - Common causes of brownouts :
        - Inadequate utility service
        - Heavy power draw in area/facility
        - Poor electrical circuit design.
- **Blackout / Power outage :** A blackout or power outage is a complete loss of utility power, whether short - or long term. Blackouts cause reduced productivity, lost revenue, system crashes and data loss. Unplanned outages may occur as aging electrical grids, and building circuits are overwhelmed by high demand. Blackouts are particularly dangerous at sites where safety or life support rely on power, such as hospitals, treatment centers and power plants.
    - Common causes by blackouts/ Power Outage
        - Utility company failure
        - Accidental AC line disconnection
        - Tripped Circuit breakers
        - Severe weather

### Symptoms of Power Problems

- The power light is off and/or the device won’t turn on.
- The power supply fan does not turn when the computer is powered on.
- The computer sounds a continuous beep. (This could also be a bad motherboard or a
stuck key on the keyboard.)
- When the computer powers on, it does not beep at all. (This could also be a bad
motherboard.)
- When the computer powers on, it sounds repeating short beeps. (This could also be a
bad motherboard.)
- During POST, a 02X or parity POST error code appears (where X is any number); one
of the POST checks is a power good signal from the power supply; a 021, 022, . . . error
message indicates that the power supply did not pass the POST test.
- The computer reboots or powers down without warning.
- The power supply fan is noisy.
- The power supply is too hot to touch.
- The computer emits a burning smell.
- The power supply fan spins, but there is no power to other devices.
- The monitor has power light, but nothing appears on the monitor, and no PC power
light illuminates.

### Protection devices : Circuit breakers, surge suppressor

- **Low Voltage Circuit Breakers :** A circuit breaker is an automatically-operated electrical switch designed to protect an electrical switch from damage caused by overload or short circuit. Unlike a fuse, which operated once and then has to be replaced , a circuit breaker  can be reset to resume normal operations. Circuit breaker are made in varying sizes, from small devices that protect an individual household appliance up to large switch gear designed to protect