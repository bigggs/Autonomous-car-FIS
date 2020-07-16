<h1> How to install </h1>
<h2>Method one</h2><br>
1: Download the FIS file<br>
2: Right click on it - open with<br>
3: Select MATLAB<br>

<h2>Method two</h2><br>
1:Open MATLAB<br>
2:File > Open <br>
3:Locate the FIS file

<br><br>

This fuzzy system offers insight into the future of autonomous cars. A fuzzy system has been developed that performs calculations to determine the safest distance at each speed from the object in front of the car running the system. Research has been done to ensure that the fuzzy system has been set up and programmed according to legislation and laws regarding road safety. The mathematical formulas responsible for indicating the acceleration rates and conversions are also accurate to real-world experiences of driving a car.
The British Highway code (Stopping distances, 2020) suggests that you should leave approximately 1 meter for every one mile per hour you are driving at, so if you are driving at 30mph you should be 30 meters away from the vehicle in front and behind you, Figure 1 demonstrates a diagram depicting this. 
<h2> 
Figure 1 A diagram depicting a car travelling at 30mph and is 30 meters away</h2>
<img src="https://i.imgur.com/uJINCxE.png">



<br><br>
Stopping distances take into consideration thinking time and braking time, according to the British Highway authority at 30mph it would take 23 meters to come to a stop – 9m for thinking distance and 23m for braking distance. Figure 2 indicates the stopping distances for cars travelling at different speeds.  (A safe separation distance, 2020)

<h2> 
Figure 2 Thinking and braking distances for vehicles travelling at different speeds (Stopping distances, 2020)
</h2>
<img src="https://i.imgur.com/WNpxBCo.png">
These factors were considered while developing this fuzzy logic autonomous vehicle. An autonomous vehicle may have shorter thinking time, however, there are other factors to take into consideration such as processing time or time until an object is detected. 
This fuzzy logic system has been developed to mathematically ensure that the autonomous vehicle will always be at a maintained distance matching meters away and miles per hour, in other words, this fuzzy system will control acceleration/deceleration rates to ensure that mph will match meters away from the vehicle ahead of the vehicle with the system installed.


<br><br>
<h1>Introduction </h1>
This system aims to allow autonomous cars to stay within a ‘safe range’ of the vehicle ahead of them, matching miles per hour with meters away. 
With these two inputs, the system calculates and provides an output of the acceleration level or deceleration level required to achieve optimum distance from the vehicle in the most efficient time.
The fuzzy logic system will be implemented in an environment that simulates autonomous cars to accelerate or decelerate to avoid a collision, drive at the legal distance, and increase general safety on the road.
Besides, this system could even be implemented by car manufacturers, even if it is not autonomously controlling the acceleration or deceleration of the car, alerting the driver if they are within an ‘unsafe distance’ from the vehicle in front of them could increase general road safety in the United Kingdom.
The developers believe this system could be potentially beneficial to new drivers as they do not have the experience to verify a reliable judgement or cannot yet predict how far away they are from an object and how much acceleration is necessary before reaching the object.
Moreover, elderly people will benefit as they have their vision and perception reduced. 
<Br><br>
<h1>Design and Development</h1>
The developers that worked in the construction of this fuzzy system, developed a two-input, and one output system. The two inputs are distance and speed. The one output is acceleration, as demonstrated in Figure 3.
 
<h2>Figure 3 Autonomous car, the fuzzy inference system</h2>
<img src="https://i.imgur.com/VLYWw8k.png">
Figure 3 illustrates a fuzzy system developed in MATLAB called ‘Autonomous Car 2.3’, this is the second increment of the software and the third software update that has been developed to date. 
This system contains three membership functions: Distance, Speed and Acceleration. The fuzzy system will calculate the difference between distance and speed and provide an output of acceleration to decide the optimum acceleration or deceleration rate to achieve the optimum distance or speed away from the vehicle ahead. 
The Membership Function Editor as demonstrated in Figures 4, 5 and 6, allowed developers to display and edit all the membership functions that are associated with the two inputs and one output for the entire fuzzy system. This editor was used when initially setting up the fuzzy system, the developers used the GUI to add three membership functions and inputted their ranges, and parameters manually through the GUI.
 <br><br.
<h1>Speed Variable</h1>
The speed variable, as revealed in Figure 4 displays the current speed of the vehicle. Its range is from 0 to 100, and it measures in miles per hour. Although the road speed limit in the United Kingdom is 70mph, the developers took into consideration that in some situation’s drivers exceed the speed limit and cutting off functionality past the speed limit would cause more harm than good. 
This 30mph increase offers a safety net to drivers as the risk of danger is increased at faster speeds, warnings will be given to drivers to slow down in future iterations. 
 <br><br>
<h2>Figure 4 FIS Variable - Speed</h2>
<img src="https://i.imgur.com/8H6G4jc.png">

This variable contains five membership function plots:
1.	The slow plot has four parameters [0 0 10 20].
2.	The slow medium plot has three parameters [10 30 40].
3.	The medium plot has three parameters [30, 50, 60].
4.	The medium-high plot has three parameters [50 70 80].
5.	The high plot has four parameters [70 90 100 100].
These plots are measurements in miles per hour.
These membership functions, parameters and ranges were inputted through using the MATLAB GUI.
These parameters overlap so the fuzzy system can determine which membership function the input belongs in, this also considers the time of processing and regions where speed is increasing and decreasing very steady, so a driver going at 33mph would be on the threshold of being in the medium although being slow. This delivers time for the processor to process the data to provide the output of slowing down if a car is within the same distance in meters.
<br><br>
<h1>Distance Variable</h1>
The distance variable as shown in Figure 5, has five membership function plots and its range is 0 to 100. The distance is measured in meters away from the object. While developing the distance variable, the developers considered road size legislation, and the UK government indicates that there are different rules for different types of roads. (How wide are roads?, 2020)

Road Classification	Size
Standard road widths	3.65m
Single carriageway with two lanes	5.5m – 7.7m

Single carriageway with a cycle lane	8.8m (principal roads), 10.3m (highways) 9m - 10.3m (classified roads)

Dual carriageway with three lanes	2 x 11m
Motorway with two lanes	2 x 7.3m + (hard shoulder)
Motorway with three lanes	2 x 11m + (hard shoulder)

The width of an entire cross-section of a motorway is approximately 56m (12 lanes, 2 hard shoulders, median dividing barrier) – M25, North of Junction 14 was used for this example.
The distance variable range allows for all types of roads in the UK to be viable for the fuzzy system – in a future iteration steering automation may be a possibility, having distance large enough to fit in all road types allows the fuzzy system to have incremental updates providing minimum data redundancy and re-optimisation.
Distance and Speed have matching membership functions with parameters and ranges essentially being paired together between each FIS variable, this is because meters away should always try to match the mph that the vehicle is travelling at.
 
<h2>Figure 5 FIS Variable  - Distance</h2>
<img src="https://i.imgur.com/6Y6SUue.png">
The five membership function plots for this variable are the following:
1.	The very short plot has four parameters [0 0 10 20].
2.	The short-medium plot has three parameters [10 30 40].
3.	The medium plot has three parameters [30 50 60].
4.	The medium-large plot has three parameters [50 70 80].
5.	The large plot has four parameters [70 90 100 100].

These parameters are measured in meters away from the object ahead.
These membership functions, parameters and ranges were inputted through using the MATLAB GUI.





<br><br>
<h1>Acceleration Variable</h1>
Figure 6 demonstrates the output, which is acceleration. The fuzzy inference system calculates the distance and speed and determines the necessary acceleration or deceleration for the car to reach its optimum distance away from the car ahead, considering the speed and distance.
The research was undertaken to specify the acceleration and deceleration parameters (Bokarea & Mauryab, 2017). Figure 7 highlights a table of different vehicle types and their max and mean acceleration values in meters per second squared, this table was used when deciding the parameters for the acceleration.
The parameters inputted allow for the maximum acceleration/deceleration rates for all vehicle types apart from a motorised two-wheeler, this is because the developers considered that this system would not be fit for purpose on a motorised bike and a different system would have to be developed for that specific category of vehicle.  
 
<h2>Figure 6 FIS variable - Acceleration</h2>
<img src="https://i.imgur.com/u4RWKIf.png">

The three membership function plots for this variable are the following:
1.	The reduced plot has three parameters [-4 -2 -0.1333].
2.	The maintained plot has three parameters [-0.6667 0.6667].
3.	The increased plot has three parameters [0.1333 2 4].

These parameters are measured in meters per second squared.
These membership functions, parameters and ranges were inputted through using the MATLAB GUI.

 <br><br>
<h2>Figure 7 Table showing acceleration values for different types of vehicles</h2>
<img src="https://i.imgur.com/FzzU4se.png">
 <br>
 <br>
<h1>Surface Viewer</h1>
 <br>
<h2>Figure 8 Surface viewer of FIS</h2>
<img src="https://i.imgur.com/D8yyqbW.png">
The diagram in Figure 8 visually outlines the symbiosis between speed and distance, speed and distance will always try to meet, acceleration as the output will ensure this. 
<br><br> 
<h1>Rules</h1>
The fuzzy inference system has a total of twenty-six rules. These rules have different levels of priority to provide a level of privilege to rules that are somewhat more important. The highest priority rules are ones that keep the vehicle at the optimum safe distance. If the optimum safe distance is always the highest priority, there will be a lower risk of collision. 
Rules were inputted manually by using the Rule Editor on MATLAB, Figure 9 shows a list of all rules.
 <br>
<h2>Figure 9 Rules for Autonomous Car</h2>
<img src="https://i.imgur.com/saCFK4V.png">
The rules are optimised and specified to try and match the distance and speed variables, the priority helps define this. The speed and distance are always trying to match to be the same value, which in turn controls the acceleration to meet it. This way the vehicle is always prioritising being at a safe distance.
 

<h1>Limitations of the fuzzy inference system</h1>
The developers are concerned about how the system would react if an object were suddenly thrown in front of the car, for instance, a person running from behind a corner into the road. The system may not have enough time to react and calculate the speed and distance to the emergency brake.
At the current stage that the system is at, it may not be able to operate correctly if there are many vehicles in front of it, for instance on a three-lane motorway where there are three cars ahead of it at varying distances. Testing of this cannot be accomplished at the current iteration as the fuzzy inference system only allows for one input of distance.
Another limitation is that cameras and sensors will be needed for a real-life application of this system, these cameras need to be able to detect objects and may become damaged or be unreliable in different climates or weather situations, testing of this situation is not feasible at the current iteration due to financial constraints.
This fuzzy logic system may not be applicable in some regions of the world due to legislation, also the risk of a software defect causing an error could lead to loss of life, damage to property and potential lawsuits. In 2017 Tesla was taken to court under a wrongful death lawsuit (Tesla Lawsuit, 2020) for having a defect in their autopilot system that caused it to hit a highway barrier in California, due to this tedious and rigorous testing needs to be done to the system before it is implemented on public roads.
<br><br>
<h1>Conclusions</h1>
The aim of building a fuzzy inference system to simulate a car being automated has successfully been accomplished. During development two iterations and several software updates have been done to improve the quality of life, accuracy, and efficiency of the system. 
The developers successfully worked efficiently in a team of two to design, develop, test, and implement the system producing a high-quality fuzzy inference system in MATLAB.

 
<h1>Proposal to integrate into society</h1>
<br>
Autonomous Car 2.3 has the potential to be a very useful application once it has reached a level where it is appropriate to integrate into society. In its current iteration, not enough testing with real-life situations and scenarios has been done to ensure its feasibility and functionality, this is mainly due to financial constraints.
In its current iteration, the system could be implemented into a car as a warning system, alerting drivers if they are within the legal distance from the vehicle ahead of them. To implement these cameras and sensors, software like Google's deep learning ANN - Vision API (Cloud Vision API, 2020) would need to be implemented in the vehicle to provide recognition to the software to indicate what objects are.
Communication between the car and system needs to be programmed in to provide the system with the required input of speed, an alternative is adding a speed sensor onto the software as a third party that is not connected to the car. 
Autonomous vehicles have several benefits when compared to their counterparts, for instance, the fuzzy logic systems autonomous capabilities such as consistency driving speeds and ensuring a consistent and measured distance between other vehicles can help reduce unnecessary braking and re-acceleration. This has the benefit of saving fuel costs for the driver and reducing emissions from the vehicle. 
Another benefit that the autonomous vehicles offer is an increase in road safety. Worldwide, there 20-50 million injuries occurring due to road traffic accidents, at its current rate, this is indicating that it will be the fifth-highest cause of death. (Road Safety Facts, 2020)
Research indicates that 90% of traffic accidents are due to human error (Crash Stats, 2019) if every car on the road had an autonomous system/autopilot this would potentially reduce traffic accidents by up to 90%.
Autonomous vehicles could potentially lead to less traffic on roads in the United Kingdom, this can be visualised as how train systems work; every departure and stopping is mathematically calculated to ensure efficiency and minimum delays – this is only possible due to communication between different stations. If cars had the same technology traffic, it would flow in a more orderly fashion, with the immense decrease in car accidents and more orderly traffic every driver on the road would be able to mathematically calculate the time to reach their destination very accurately.
Although there are many benefits to implementing the developed fuzzy logic system into society, it is also important to consider the arguments against autonomous vehicles on the road. 
One argument against having autonomous vehicles is that it could lead to a loss of jobs. The subject of Artificial intelligence greatly considers delegating human responsibilities to machines. The industrial revolution has been argued that it made man into a machine, which is what many people now rely on for general livelihood. 
With the development of intelligent agents, many people could lose their jobs, taxi drivers and workers in the transportation industry could find that their trade no longer requires them as it is more efficient and more economical to have an autonomous vehicle to transport goods or people.
Intelligent agents also have a lack of morals; a good argument of this is the theory of instrumental convergence by Oxford philosopher, Nick Bostrom (Instrumental convergence, 2020) which simply put dictates to get from point A – B humans have evolved and developed specific psychology taking into consideration of ethics and wickedness. 
The thought experiment of building an intelligent agent as a “paper-clip maximiser” (Frankenstein’s paperclips, 2020) helps visualise this as an intelligent agent will not consider somewhat ‘invisible’ inputs that humans consider without even noticing.
Regarding this fuzzy system, there is no algorithm that it can compute to determine if it is worth emergency braking on the road to stop a collision with a person running ahead of it from a blind spot while there is a car very close behind it. For this reason, a manual overdrive must be available to the human driver to make these decisions if necessary. 
Another potentially dangerous drawback to this fuzzy logic system is the potential of cyber criminals hacking the vehicles and manually inputting incorrect distances or speeds to cause a collision. Nowadays thieves break into cars using physical objects to unlock doors, however, in the future with the implementation of autonomous vehicles, hackers could do the same, but the outcomes could be far more dangerous.
In conclusion, in the software’s current state, it is not appropriate to be implemented into a real-world scenario due to reasons such as financial and time constraints which limited testing and implementation into real vehicles, but in the testing environment of MATLAB all test cases passed. 
This fuzzy inference system, that has been developed, could help offer insight into the formulas of implanting the technology into a real-world scenario. In future, if this project continued development through the iterations a fully functioning automated car could be produced. 
 
<h1>References</h1>

Arbital.com. 2020. Instrumental Convergence. [online] Available at: <https://arbital.com/p/instrumental_convergence/> [Accessed 5 June 2020].

Association for Safe International Road Travel. 2020. Road Safety Facts. [online] Available at: <https://www.asirt.org/safe-travel/road-safety-facts/> [Accessed 5 June 2020].

Bokarea, P. and Mauryab, A., 2017. Acceleration-Deceleration Behaviour of Various Vehicle Types. ScienceDirect,.

Crash stats. 2019. [online] Available at: <https://crashstats.nhtsa.dot.gov/Api/Public/ViewPublication/812115> [Accessed 5 June 2020].

Driving Test Success. 2020. A Safe Separation Distance. [online] Available at: <https://www.drivingtestsuccess.com/blog/safe-separation-distance> [Accessed 5 June 2020].

Driving Test Success. 2020. Stopping Distances. [online] Available at: <https://www.drivingtestsuccess.com/blog/stopping-distances-and-theory-test> [Accessed 5 June 2020].

Google Cloud. 2020. Cloud Vision API. [online] Available at: <https://cloud.google.com/vision/docs/object-localizer> [Accessed 5 June 2020].

Mocktheorytest.com. 2020. How Wide Are Roads?. [online] Available at: <https://mocktheorytest.com/resources/how-wide-are-roads/):> [Accessed 5 June 2020].

Techcrunch.com. 2020. Tesla Lawsuit. [online] Available at: <https://techcrunch.com/2019/05/01/tesla-sued-in-wrongful-death-lawsuit-that-alleges-autopilot-caused-crash/?guccounter=1&guce_referrer=aHR0cHM6Ly93d3cuZ29vZ2xlLmNvbS8&guce_referrer_sig=AQAAANqsBw_0kfnR6Wc1Iy05_KT02f2kflRWD5UlmXo-d9FVhzfSmqVR0E7s6ryml5TTRIhVwgLgSRQAm3tCaxf-KCMHC44gu1Tzkr0t0RywM5pVSxxuNHSK0yJlAywJYCknaruNNR3HOErPAj5WK-6LqB2zIVah7f9SOasgPNtf5iNe> [Accessed 5 June 2020].

The Economist. 2020. Frankenstein’S Paperclips. [online] Available at: <https://www.economist.com/special-report/2016/06/23/frankensteins-paperclips> [Accessed 5 June 2020].
