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
<caption><center> <u> <font color='black'> Figure 1 </u><font color='black'> : Scientifc Objective of Mars Exploration Program <br> Recovered from: https://mars.nasa.gov/mars2020/mission/overview/ </center></caption>

These include those related to the search for biosignatures and caching samples, as they are those that come into action when linking them with engineering applications that facilitate such processes, like the implementation of a device or artifact capable of complying with these challenges.

In order to make our autonomous system essentially useful for the mission, we identified all the instruments mounted on the Rover Perseverance, each with unique functions (which can even include several transducers and among other maneuverability devices, as is the case of the turret or robotic arm), in order to determine which of these could be distributed throughout the area in various autonomous units, in a way that allows to collect more valuable information in the shortest possible time, while allowing to increase the range of possibilities in which some data of great impact for the scientific community can be observed and captured. []

To choose this instrument, we are based on some criteria related to the importance that this instrument brings within the objectives, weight and energy consumption. This categorization is based on the need to have a reduced body volume of each autonomous unit, which brings with it a low energy consumption inherent to the reduced load capacity. The following table contains specific information from the various instruments regarding the criteria mentioned above:

<img src="/Images/Instruments_Table.png" class="center" width="608" height="599"/>
<caption><center> <u> <font color='black'> Figure 2</u><font color='black'> : List of instruments mounted on Rover Perseverance <br> Recovered from: https://mars.nasa.gov/mars2020/spacecraft/rover/ </center></caption>

When choosing the instrument, it is important to compare the various factors grouped in the table above. Regarding the **Power consumption** factor, it is observed that those related to the analysis of rocks and capture of graphic information (SHERLOC / WATSON, Mastcam-Z, SuperCam and PIXL) have a high energy consumption, and by far there is the chemical conversion instrument, which consumes the most (300 W). The MEDA and RIMFAX are among the least energy consumption, therefore, within this factor, they are possible candidates to choose from.

The **Mass** factor is important when selecting an instrument, based on the maneuverability that the autonomous unit will have during its routine, in turn with the power that the actuators will have to exert to move the system. All the instruments, with the exception of the MOXIE, have masses that vary between 1.6 kg (SHERLOC / WATSON) up to 6 kg (MEDA). Although these are considerable masses, the weight of a body on Mars is only a third of what it has on Earth, so this may be within a good degree of acceptance.

Finally, taking into account the **Measured variables or main objective** factor, it is important to note the homogeneity of the information captured and the position from which the information is captured. The first 4 instruments listed in the table will not increase their efficiency in capturing information if they are distributed throughout the area, since it is enough to take the samples from the Rover directly, in addition to the issue about the amount of energy each one consumes, especially the MOXIE.

This leaves us with the last two candidates: MEDA and RIMFAX. A large part of the variables obtained by MEDA are uniform, at least within a large spatial range on the Mars surface, and the variations that would be obtained when positioning several of these sensors in autonomous units whose maximum distance radius with respect to the ROVER does not would exceed 500 m (for communication issues) are minimal or imperceptible. This indicates that, similar to the factor previously addressed, the efficiency in information capture would not increase.

On the other hand, the information captured by the RIMFAX depends on the place where the mobile is placed, so that the information ratio obtained increases depending on the amount that is spread out, finally causing the efficiency of information capture to increase. One of the main objective is to find water and ice signs (if not liquid water itself) under the martian surface, and this device is the first of its category inserted onto a Rover capable of capture many geological features with no need to put a drill on the ground. []

## Project overview

As soon as we set this selection, we began to brainstorm possible solutions involving the RIMFAX module to find water on Mars. From this process we conclude that this task must be carried out efficiently and quickly, since finding water on Mars would exponentially accelerate the colonization of that planet. By priority, we propose a swarm of autonomous collaborative robots, capable of exploring the entire surface of Mars.

These robots would have the following elements for Martian exploration:

-	The robot body will be made of rugged materials to protect the electronics inside and will have heaters to keep all electronic components in proper operation. Similar components can be found into the Rovers missions and the recent Ingenuity (from Perseverance mission). []
-	Central processing unit where all decisions will be made.
-	Temperature sensor to transmit its value to the CPU and this control the heaters.
-	Battery level sensor
-	Inertial Measurement Unit (IMU) to identify and control the robot's imbalance and prevent the robot from overturning.
-	For navigation we will implement a LIDAR device.
-	For power generation we will implement solar panels. It is proved that this power resource is adequate for this devices. As an example, the Ingenuity works with solar power, which energy is contained later in a battery pack. []
-	Its traction system will be using mechanum wheels with electric motors directly connected to these wheels, thus avoiding a steering system.
-	Antennas to communicate with satellites to report their status, and their location in case of finding groundwater.

These robots would reach the Martian surface through a similar capsule in which astronauts from the Apollo 11 mission arrived. When you opened the gate, they would go out in different directions in search of water sources.


### Modelo 3D
### Videos de interacción con el modelo 3d
### Posible impacto en la misión de Marte
### Cierre y video

======================================================================================

### Markdown

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text
 
[Link](url) and ![Image](src)
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Documentation

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/atlasthehero/handsonviii/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Thanks for reading us!

Having trouble with Pages? Check out our [documentation](https://docs.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.
