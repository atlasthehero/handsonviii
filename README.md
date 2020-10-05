##SpaceAPPS Create: Virtual planetary exploration - AquaSeeker 

=============================================================

### Who are we?

<img src="Black and Red Gaming Logo.png" alt="" class="center" width="300" height="300"/>

We are a team of mechatronics engineers that always had dreamed with "The far far away", honing our skills every day hoping to help space exploration one day 
and working to empower space and interplanetary exploration.

Am... Hands ON VIII? Yes! it was the name of a series of robotics and project management courses that we had in college, that we thought it ended in Hands ON VII but... Voilá

### Which is our north?
We believe that robotics can help a lot in exploration providing value by boosting data collection and exploration in general, in this case, mars exploration. Putting cobots on the mars surface in order to cover faster the necessity of acquiring knowledge of our friendly neighbor.

### What we are good in?
Our team covers different areas, just like electronics, mechanics, physics, generative design, artificial intelligence, embedded systems, 3d printing, and robotics.

Even tho, we had done several personal projects about aerospace and aerodynamic design.

### Cientific and technical process 

At first, we identify the most important variables that humans are looking for in the exploration of Mars. To do this, we base ourselves on the 4 scientific objectives that the Mars Exploration Program has as its principle:

<img src="/Images/Nasa_Objectives.png" class="center" width="1300" height="300"/>
<caption><center> <u> <font color='black'> Figure 1 </u><font color='black'> : Scientifc Objective of Mars Exploration Program <br> Source:  <a href="https://mars.nasa.gov/mars2020/mission/overview/" title="Mission overview">NASA-Perseverance mission overview</a> </center></caption>
 
 <br>
 <br/>

These include those related to the search for biosignatures and caching samples, as they are those that come into action when linking them with engineering applications that facilitate such processes, like the implementation of a device or artifact capable of complying with these challenges.

In order to make our autonomous system essentially useful for the mission, we identified all the instruments mounted on the Rover Perseverance, each with unique functions (which can even include several transducers and among other maneuverability devices, as is the case of the turret or robotic arm), in order to determine which of these could be distributed throughout the area in various autonomous units, in a way that allows to collect more valuable information in the shortest possible time, while allowing to increase the range of possibilities in which some data of great impact for the scientific community can be observed and captured.

To choose this instrument, we are based on some criteria related to the importance that this instrument brings within the objectives, weight and energy consumption. This categorization is based on the need to have a reduced body volume of each autonomous unit, which brings with it a low energy consumption inherent to the reduced load capacity. The following table contains specific information from the various instruments regarding the criteria mentioned above:

<img src="/Images/Instruments_Table.png" class="center" width="608" height="599"/>
<caption><center> <u> <font color='black'> Figure 2</u><font color='black'> : List of instruments mounted on Rover Perseverance <br> Source:  <a href="https://mars.nasa.gov/mars2020/spacecraft/rover" title="Perseverance Summary">NASA-Perseverance summary</a> </center></caption>
 
 <br>
 <br/>

When choosing the instrument, it is important to compare the various factors grouped in the table above. Regarding the **Power consumption** factor, it is observed that those related to the analysis of rocks and capture of graphic information (SHERLOC / WATSON, Mastcam-Z, SuperCam and PIXL) have a high energy consumption, and by far there is the chemical conversion instrument, which consumes the most (300 W). The MEDA and RIMFAX are among the least energy consumption, therefore, within this factor, they are possible candidates to choose from.

The **Mass** factor is important when selecting an instrument, based on the maneuverability that the autonomous unit will have during its routine, in turn with the power that the actuators will have to exert to move the system. All the instruments, with the exception of the MOXIE, have masses that vary between 1.6 kg (SHERLOC / WATSON) up to 6 kg (MEDA). Although these are considerable masses, the weight of a body on Mars is only a third of what it has on Earth, so this may be within a good degree of acceptance.

Finally, taking into account the **Measured variables or main objective** factor, it is important to note the homogeneity of the information captured and the position from which the information is captured. The first 4 instruments listed in the table will not increase their efficiency in capturing information if they are distributed throughout the area, since it is enough to take the samples from the Rover directly, in addition to the issue about the amount of energy each one consumes, especially the MOXIE.

This leaves us with the last two candidates: MEDA and RIMFAX. A large part of the variables obtained by MEDA are uniform, at least within a large spatial range on the Mars surface, and the variations that would be obtained when positioning several of these sensors in autonomous units whose maximum distance radius with respect to the ROVER does not would exceed 500 m (for communication issues) are minimal or imperceptible. This indicates that, similar to the factor previously addressed, the efficiency in information capture would not increase.

On the other hand, the information captured by the RIMFAX depends on the place where the mobile is placed, so that the information ratio obtained increases depending on the amount that is spread out, finally causing the efficiency of information capture to increase. One of the main objective is to find water and ice signs (if not liquid water itself) under the martian surface, and this device is the first of its category inserted onto a Rover capable of capture many geological features with no need to put a drill on the ground. (Source: <a href="https://mars.nasa.gov/mars2020/spacecraft/instruments/rimfax/" title="RIMFAX instrument">RIMFAX instrument</a>)

<img src="/Images/RIMFAX.png" class="center" width="1124" height="394"/>
<caption><center> <u> <font color='black'> Figure 3</u><font color='black'> : RIMFAX <br> The instrument is composed of an electronics box, installed within the interior of the rover, and a nadir-point antenna affixed to the exterior (rear) of the rover. Source: <a href="https://mars.nasa.gov/mars2020/spacecraft/rover" title="Perseverance Summary">NASA-Perseverance summary</a> </center></caption>
 
 <br>
 <br/>

## Project overview

As soon as we set this selection, we began to brainstorm possible solutions involving the RIMFAX module to find water on Mars. From this process we conclude that this task must be carried out efficiently and quickly, since finding water on Mars would exponentially accelerate the colonization of that planet. By priority, we propose a swarm of autonomous collaborative robots, capable of exploring the entire surface of Mars.

These robots would have the following elements for Martian exploration:

-	The robot body will be made of rugged materials to protect the electronics inside and will have heaters to keep all electronic components in proper operation. Similar components can be found into the Rovers missions and the recent Ingenuity (from Perseverance mission). (Source: <a href="https://mars.nasa.gov/technology/helicopter/" title="Ingenuity">Ingenuity</a>)
-	Central processing unit where all decisions will be made.
-	Temperature sensor to transmit its value to the CPU and this control the heaters.
-	Battery level sensor
-	Inertial Measurement Unit (IMU) to identify and control the robot's imbalance and prevent the robot from overturning.
-	For navigation we will implement a LIDAR device.
-	For power generation we will implement solar panels. It is proved that this power resource is adequate for this devices. As an example, the Ingenuity works with solar power, which energy is contained later in a battery pack. (Source: <a href="https://mars.nasa.gov/mer/mission/technology/power/" title="Technologies of Broad Benefit:
Power">Technologies of Broad Benefit: Power</a> , <a href="https://mars.nasa.gov/files/mars2020/MarsHelicopterIngenuity_FactSheet.pdf" title="NASA Ingenuity Factsheet">NASA Ingenuity Factsheet</a>)
-	Its traction system will be using mechanum wheels with electric motors directly connected to these wheels, thus avoiding a steering system.
-	Antennas to communicate with satellites to report their status, and their location in case of finding groundwater.

These robots would reach the Martian surface through a similar capsule in which astronauts from the Apollo 11 mission arrived. When the gate is opened, they would go out in different directions in search of water sources.

### Solar Energy usage as main power source

Getting the most out of the solar energy that a solar cell receives is a complex design job. In general, the energy obtained E (W) from a solar panel is defined by means of the following general expression:

<img src="https://render.githubusercontent.com/render/math?math=E = A * \eta * \phi * P_{r}">

Where:
- <img src="https://render.githubusercontent.com/render/math?math=A"> is the total area of the panel (<img src="https://render.githubusercontent.com/render/math?math=m^{2}">); 
- <img src="https://render.githubusercontent.com/render/math?math=\eta"> is the performance of the panel (%);
- <img src="https://render.githubusercontent.com/render/math?math=\phi"> is the solar irradiation reached by the panel (<img src="https://render.githubusercontent.com/render/math?math=W / m^{2}">);
- <img src="https://render.githubusercontent.com/render/math?math=\P_{r}"> is the performance ratio, for which defines the losses due to energy conversion, which usually oscillates between 0.5 and 0.9. 

The variable factor within the expression is the solar irradiation, which depends on both the Martian season of the year and the latitude on which the device is located.

Thanks to the data obtained by the Rover missions through the Rover Environmental Monitoring Station (REMS), within which are the data collected by Curiosity, a table was built in which the energy produced by a <img src="https://render.githubusercontent.com/render/math?math=1 m^{2}"> panel is presented, with <img src="https://render.githubusercontent.com/render/math?math=\eta=0.447"> and <img src="https://render.githubusercontent.com/render/math?math=\P_{r}=0.75">, depending on the Martian season and latitude:

<img src="/Images/Table_energy_production.png" class="center" width="1476" height="140"/>
<caption><center> <u> <font color='black'> Figure 4</u><font color='black'> : Daily solar power (W) production for a 1 m2 panel (\eta=0.447; \phi=0.75) as a function of latitude and season. <br> Source:  <a href="https://www.researchgate.net/publication/298431734_Solar_and_wind_exergy_potentials_for_Mars" title="Solar and wind exergy potentials for Mars">Solar and wind exergy potentials for Mars</a> </center></caption>
 
 <br>
 <br/>

In general, the various Martian exploration missions land on latitudes ranging from -30° to 30°. Based on this important factor, it can be seen in the table that on average the high rates of energy produced are located precisely in this range, regardless of the season of the year. The following shows an interactive image map of the global topography of Mars, visualizing longitude in the X-axis, and latitude in the Y-axis within:

<img src="/Images/Interactive_map.png" class="center" width="1494" height="700"/>
<caption><center> <u> <font color='black'> Figure 5</u><font color='black'> : interactive image map of the global topography of Mars, overlain with locations of Mars landers and rovers <br> Source: <a href="https://en.wikipedia.org/wiki/Mars_landing#Landing_site_locations" title="Landing site locations">Landing site locations</a> </center></caption>
 
 <br>
 <br/>
 
 
 
### Modelo 3D
### Videos de interacción con el modelo 3d
### Posible impacto en la misión de Marte



### Cierre y video

======================================================================================



