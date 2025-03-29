**The following is an unedited log of the testing that Marc performed on various servos over the course of a few months. All I've done is copy every post he made about servos, along with the the images he posted. I also added some of the questions we asked him during testing, for context.**



i whipped up a test setup and tortured a random MG90 today, will repeat the test with savox, guo hua and metal gear mg90 tomorrow evening

![Servo Test Rig](https://github.com/Enraged-Rabbit-Community/ERCF_v2/blob/master/Documentation/assets/servo_testing/PXL_20240421_232803876.jpg)

after ~45 "hard push" actions in short succession (100ms delay between each try) the MG90 is basically about to fail and already started to degrade push performance after 25 pushes

![MG90s Servo with Plastic Gears Results](https://github.com/Enraged-Rabbit-Community/ERCF_v2/blob/master/Documentation/assets/servo_testing/CleanShot_2024-04-22_at_01.27.232x.png)

![AZ-Delivery MG90 Results](https://github.com/Enraged-Rabbit-Community/ERCF_v2/blob/master/Documentation/assets/servo_testing/AZ-Delivery_SG90_-_0.35ah.png)
![Guo Hua A0090 Results](https://github.com/Enraged-Rabbit-Community/ERCF_v2/blob/master/Documentation/assets/servo_testing/Guo_Hua_A0090_-_0.4a.png)
![MG90 Metal Gear Results](https://github.com/Enraged-Rabbit-Community/ERCF_v2/blob/master/Documentation/assets/servo_testing/MG90_Metal_Gear_-_0.6ah.png)
![Savox Force vs Temperature](https://github.com/Enraged-Rabbit-Community/ERCF_v2/blob/master/Documentation/assets/servo_testing/Savox_SH-0255MG_-_0.6ah.png)

and here's a comparison, solid lines are the force and dashed the temperature lines, same color same servo

![Comparison](https://github.com/Enraged-Rabbit-Community/ERCF_v2/blob/master/Documentation/assets/servo_testing/CleanShot_2024-04-23_at_01.28.052x.png)

so, the Savox beats all others easily, the plastic gear one is really unreliable, the metal gear MG90 is kinda ok and holing on, the Guo Hua seems also pretty solid and stable, but far away form the push power of the savox.
all force and temperature values should be considered rough estimates, because i simply threw together a load cell and ntc temperature probe, but for comparing this is still valid data to see the difference
also, the Savox and Guo Hua stay quite cool, both MG90 variants get hot quick and can lead to permant failure easily when stressed a lot


Guo hua a0090 would be also an option, seems stable and reliable, but not ad strong as the mg90s

here's the gist of the Data i gather so far:

![Results Data Table](https://github.com/Enraged-Rabbit-Community/ERCF_v2/blob/master/Documentation/assets/servo_testing/CleanShot_2024-04-24_at_01.30.372x.png)

the SG90/MG90 basically disqualify due to quick heat buildup, A0090 and SH-0225MG keep pretty cool, A0090 does have more push power than the MG90/SG90 but is far behing the SH-0255MG

i just ordered these for Servos for additional tests, give me a shout, if you know of any more i should/could include in these tests, i also ordered an original TowerPro MG90S, since i only got a random clone tested so far

GDW DS041MG (https://gdwservo.com/product/gdw-ds041mg-5kg-torque-metal-gear-micro-mini-digital-servo-for-450-helicopter-fix-wing-rc-auto-robot-arm/)

DSPower DS-S006M (https://www.dspowerservo.com/ds-s006m-metal-gear-9g-servo-micro-servo-product/)

JX Servo PDI-1109MG (http://www.jx-servo.com/en/Product/micro/MD/566.html)

Original TowerPro MG90S (https://www.towerpro.com.tw/product/mg90s-3/)

![Servo Tuesday 1](https://github.com/Enraged-Rabbit-Community/ERCF_v2/blob/master/Documentation/assets/servo_testing/PXL_20240430_135639891.jpg)
![Servo Tuesday 2](https://github.com/Enraged-Rabbit-Community/ERCF_v2/blob/master/Documentation/assets/servo_testing/PXL_20240430_135426634.jpg)

Seems to be a Servo Tuesday 

Will start testing tonight

TowerPro MG90S being stressed on the bench, maxes out at 740g so far and already quickly rose to 51.2°C, so far not looking better than the clones, will run through 3000 cycles with 1s pause in between 

well, already started to degrade when it rose to 55°C, so i canceled that run and put on the GDW DS041MG instead, lets see how it'll hold up, change to 5s instead of 1s pause in betrween cycles

GDW DS041MG (~7.5€ on AliExpress) put up a solid performance over night, stable ~800g of push force, quickly rose to ~30°C but didn't rise above 35°C which should be quite fine, this was 3000 attempts at 5s pause 

![GDW DS041MG Results](https://github.com/Enraged-Rabbit-Community/ERCF_v2/blob/master/Documentation/assets/servo_testing/CleanShot_2024-05-01_at_11.42.392x.png)

some nerdy stuff, i completely redid the electronics for the test rig and switched form rp2040 to an esp32, so instead of logging to a serial console the data now flows directly into my influxDB which i have running on my HomeAssistant Server anyway. Usually that's a time based logging, but i programmed the esp32 so that the test run always starts at start of epoch and goes from there, so the data is comparable to each other over real timeframes

using that data i can use Grafana to dig in and plot it into graphs, and even publish snapshots to share online: https://snapshots.raintank.io/dashboard/snapshot/K923gpDqSMlkNJxxM6egWdj5cI3GKi1t

so, now i've got the JX PDI-1109MG on the Test bench, temperature looks good so far, similar to the GDW around 30-35°C, but push force seems to be almost 100g less than the GDW at mean:

JX PDI-1109MG (~6€ on AliExpress) kept going stable at the force and temperature over all 3000 attempts, so not as strong as GDW, but it seems to be stable for longer use 

![JX PDI-1109MG Results](https://github.com/Enraged-Rabbit-Community/ERCF_v2/blob/master/Documentation/assets/servo_testing/CleanShot_2024-05-01_at_16.35.282x.png)

comparison in one graph of those 2

![GDW DS041MG and JX PDI-1109MG Results](https://github.com/Enraged-Rabbit-Community/ERCF_v2/blob/master/Documentation/assets/servo_testing/CleanShot_2024-05-01_at_16.37.002x.png)

next up: CSPower 12G Digital Servo (~4€ on AliExpress)

CSPower 12G Digital Servo (~4€ on AliExpress) is off to a good start:

![CSPower 12G Beginning](https://github.com/Enraged-Rabbit-Community/ERCF_v2/blob/master/Documentation/assets/servo_testing/CleanShot_2024-05-01_at_17.12.312x.png)


![Servo Size Comparison](https://github.com/Enraged-Rabbit-Community/ERCF_v2/blob/master/Documentation/assets/servo_testing/AP1GczN3xuk0uwnqtSj0e75c4FxmamNfbL2QsegaGktWaHRYZGLtNWS67bxC4ww3378-h2544-s-no-gm.png)

second from the right, right next to the original mg90s, a tiny bit smaller

![CSPower 12G](https://github.com/Enraged-Rabbit-Community/ERCF_v2/blob/master/Documentation/assets/servo_testing/Sefde0918c7e6474fa499eed3128397e82.png)

i'll do another run with the original towerpro mg90 after this run, but at 1s pause it quickly heated up as well

will give it another chance at 5s like the others right now

yes, Guo Hua and Savöx standing above

will redo both on the latest rig and test firmware as well to have a fair comparison with 3000 tries 5s pause

takes about 5h for one test run 😅

which is also kind of a fair "test" for real world usage imho

i'm running these in a ~20°C room right now sandwiched between 2 aluminium blocks (vise), that should already enable some heat dissapation, now how would they handle in hotter climate?

especially in such cases MG90 might go bad quicker

ProModeler was difficult to source, right?

US only?

44$ and no shipping option to me, so, yea no thanks 😄

CSPower 12G is happily chopping on without signs of degradation:

![CSPower 12G preliminary results](https://github.com/Enraged-Rabbit-Community/ERCF_v2/blob/master/Documentation/assets/servo_testing/CleanShot_2024-05-01_at_20.22.582x.png)

so, yea very solid performance for the price for the CSPower 12G Servo:

![CSPower 12G results comparison](https://github.com/Enraged-Rabbit-Community/ERCF_v2/blob/master/Documentation/assets/servo_testing/CleanShot_2024-05-01_at_22.12.082x.png)

next i'm rerunning the Savöx as a comparison, already feels like they're playing in different leaques...

Savöx basically "shifts" that whole graph into a new perspective:

![Savox results comparison](https://github.com/Enraged-Rabbit-Community/ERCF_v2/blob/master/Documentation/assets/servo_testing/CleanShot_2024-05-01_at_22.13.462x.png)

savöx is the green dot top left

1.53kg average currently

i mean, what really sets the savöx above from the others, is, that it basically doubles the push force of the others while also being the coolest to operate, really suprising considering how similar the others perform: 

would be curious to add ProModeler to the list, though i don't think it'll end up as the recommodation for most people, it'll be difficult to beat Guo Hua performance/price wise and the CSPower seems to be very good for that low price

Guo Hua is available for 6-7€ currently on AliExpress

ea, i'll slap on the guo hua again tomorrow morning, savöx will run for another ~4h

I'd currently group the servos into: 

discouraged: MG90 (Clones and Original)

budget options: CSPower, GDW, JX

default recommodation: Guo Hua

high peformance: Savöx (, maybe ProModeler)

so, Savöx performed very stable, 1560g push force mean and did't exceed 20.5°C, pretty impressive.

Guo Hua is running since this morning, kinda expected a bit more push force, but 776g is still a solid performance so far, pretty happy about the temperature, it's even below the savöx

![Guo Hua Results Comparsion](https://github.com/Enraged-Rabbit-Community/ERCF_v2/blob/master/Documentation/assets/servo_testing/CleanShot_2024-05-02_at_11.36.07.png)

actually you're right the temp of guo huo does not make sense, need to investigate, because this is the temp in the room for the last 24h:

![Room Temp](https://github.com/Enraged-Rabbit-Community/ERCF_v2/blob/master/Documentation/assets/servo_testing/CleanShot_2024-05-02_at_15.25.42.png)

i'd put out basically this: 

discouraged: MG90 (Clones and Original) [tests have shown degrading push power and thermal problems in stress tests]

budget options: CSPower 12g, GDW DS041MG, JX PDI-1109MG

default recommodation: Guo Hua A0090

high peformance: Savöx 0255MG (, maybe ProModeler)

will do, i'll investigate the guo huo temperature later tonight and add a final run of the original tower pro which is missing right now, then i'll announce that in the vendor chat with some data, prices, etc.

to be honest, i'm a bit confused right now, doing another test with another random XTVTX MG90 looks like this so far:

![XTVTX MG90 preliminary results](https://github.com/Enraged-Rabbit-Community/ERCF_v2/blob/master/Documentation/assets/servo_testing/CleanShot_2024-05-02_at_18.48.562x.png)
![XTVTX MG90 results comparison](https://github.com/Enraged-Rabbit-Community/ERCF_v2/blob/master/Documentation/assets/servo_testing/CleanShot_2024-05-02_at_19.02.302x.png)

will do at least one other XTVTX to compare

i am collecting voltage and current, but the sensors i have seem to be shit, so not really usable data

i can read about 0.254A on my lab power supply on this run currently

additionally connected to usb though, so probably not the full picture

the other XTVTX MG90 i tested did degrade after 1000-2000 tries:

![XTVTX MG90 degradation](https://github.com/Enraged-Rabbit-Community/ERCF_v2/blob/master/Documentation/assets/servo_testing/CleanShot_2024-04-25_at_09.png)

Maybe the other one was bad

Will try ~100 attempts with every clone i have to get a "range"

well, just came back from outside...

good impression didn't last:

![XTVTX MG90 failure](https://github.com/Enraged-Rabbit-Community/ERCF_v2/blob/master/Documentation/assets/servo_testing/CleanShot_2024-05-02_at_20.59.352x.png)

![VIDEO](https://github.com/Enraged-Rabbit-Community/ERCF_v2/blob/master/Documentation/assets/servo_testing/PXL_20240502_185900545.LS.mp4)

Houston, we've got a failed MG90S clone

Yes, it was probably still "fresh" but went bad quick

![Broken plastic gears](https://github.com/Enraged-Rabbit-Community/ERCF_v2/blob/master/Documentation/assets/servo_testing/PXL_20240502_190529853.jpg)

1 gear failed completely and one lost one tooth

should i try to destroy another? 😄

i put on the original TowerPro MG90s instead, let's see if it also shares that same fate

well, i'd say there's already kind of a trend visible:

![TowerPro MG90S Trend Beginning](https://github.com/Enraged-Rabbit-Community/ERCF_v2/blob/master/Documentation/assets/servo_testing/CleanShot_2024-05-02_at_21.38.082x.png)

These are the original TowerPro MG90s.

`What good are these motors if they fail so badly. Must be for the very lightest toys.`

yea, especially because these 2 variants are basically the "only" servos you get when searching amazon for small servos:

can't get Guo Hua A0090, GDW DS041MG, JX PDI-1109MG or CSPower 12g on amazon here in germany

i need to source all of them from ali

trend does seem to continue:

![TowerPro MG90S Trend continuing](https://github.com/Enraged-Rabbit-Community/ERCF_v2/blob/master/Documentation/assets/servo_testing/CleanShot_2024-05-02_at_22.49.552x.png)

seems to stabilize so far:

![TowerPro MG90S stablized](https://github.com/Enraged-Rabbit-Community/ERCF_v2/blob/master/Documentation/assets/servo_testing/CleanShot_2024-05-02_at_22.49.552x.png)

i had to restart that test, the servo arm startet slipping/stripping out on that test (bottom graph), the new test was stable over 3000 attempts:

![TowerPro MG90S stable?](https://github.com/Enraged-Rabbit-Community/ERCF_v2/blob/master/Documentation/assets/servo_testing/CleanShot_2024-05-03_at_10.05.432x.png)

so, overall the TowerPro Original did similar to the other good servos:

![TowerPro MG90S Comparison](https://github.com/Enraged-Rabbit-Community/ERCF_v2/blob/master/Documentation/assets/servo_testing/CleanShot_2024-05-03_at_10.07.122x.png)

will slap a final clone on the bench to see if it also fails

still doing more tests on the MG90 clones, 2 did quite ok so far, one failed with brokes gears and the on on it right now quickly dipped in performance but is stable so far, but it does make a struggling sound, so might fail during this test :

![XTVTX MG90 prolonged testing](https://github.com/Enraged-Rabbit-Community/ERCF_v2/blob/master/Documentation/assets/servo_testing/CleanShot_2024-05-05_at_14.15.322x.png)

short status quo, still testing, so far 5 XTVTX Servos, suprisingly most are putting up a good performance aside from the one that failed with broken gears and one (Number 4) which did not work at all, so it's missing in the graph:

![XTVTX MG90 mixed bag](https://github.com/Enraged-Rabbit-Community/ERCF_v2/blob/master/Documentation/assets/servo_testing/CleanShot_2024-05-06_at_16.40.30.png)

there is quite a bit variation in push force though

`The manufactured consistency sounds like a big issue to me despite the performance`

yea, currently i'd still recommend one of the others, kinda expected number 3 to fail as well, it was very noisy, almost crying to be released from it's misery, while pushing

`yeah in my opinion 2 out of 5 being defective is horrible even before performance testing. In my opinion if it is any worse than 1% of 100 samples, that's hugely iffy.`

I'll do additional tests with the others as well to see how they stack up

`have you tested the GDW DS041MG as of yet?`

yes, worked pretty good:

![GDW DS041MG results](https://github.com/Enraged-Rabbit-Community/ERCF_v2/blob/master/Documentation/assets/servo_testing/CleanShot_2024-05-07_at_21.42.192x.png)

the #7 of XTVTX MG90 did some funky stuff at the, will do another round for that one:

![XTVTX MG90 #7 mixed bag](https://github.com/Enraged-Rabbit-Community/ERCF_v2/blob/master/Documentation/assets/servo_testing/CleanShot_2024-05-08_at_09.38.462x.png)

so, yea this #7 of the XTVTX MG90s really does some wonky stuff, (blue round 1, red round 2)

![XTVTX MG90 #7 mixed bag](https://github.com/Enraged-Rabbit-Community/ERCF_v2/blob/master/Documentation/assets/servo_testing/CleanShot_2024-05-08_at_11.24.582x.png)

BTW, i've collected almost 50 000 force measurments by now 

`There are more GDW issues showing up on Facebook now too.`

i'll put on one of the other GDW after this MG90 testrun in ~1h

i got 4 GDX here i can test

#7 is really a weird one, expected it to completely fail, but seems like it'll go out with decent values, still the weird spikes  and variance of performance would disqualify it for me

![XTVTX MG90 mixed bag](https://github.com/Enraged-Rabbit-Community/ERCF_v2/blob/master/Documentation/assets/servo_testing/CleanShot_2024-05-08_at_14.50.242x.png)

started testrun on GDW #2

![GDW DS041MG #2 results](https://github.com/Enraged-Rabbit-Community/ERCF_v2/blob/master/Documentation/assets/servo_testing/CleanShot_2024-05-08_at_23.27.302x.png)

second GDW performt quite consistend, i think i've got the lever arm a bit further out which explains the differnt push force

#3 GDW is also performing similar to the #2 so far

`bad batch then, or is it bad software configuration I wonder?`

this only tests force + temperature currently

not speed

i'm waiting 100ms after initializing the move to measure

so, let's print a "batch" test jig 😅

![Batch Test Jig 1](https://github.com/Enraged-Rabbit-Community/ERCF_v2/blob/master/Documentation/assets/servo_testing/CleanShot_2024-05-09_at_02.01.382x.png)
![Batch Test Jig 1](https://github.com/Enraged-Rabbit-Community/ERCF_v2/blob/master/Documentation/assets/servo_testing/CleanShot_2024-05-09_at_02.01.312x.png)
![Batch Test Jig 1](https://github.com/Enraged-Rabbit-Community/ERCF_v2/blob/master/Documentation/assets/servo_testing/CleanShot_2024-05-09_at_02.03.212x.png)

the "bump" on the load cell ensures that the push point is 1cm from the center of the servo

![GDW DS041MG #3 results](https://github.com/Enraged-Rabbit-Community/ERCF_v2/blob/master/Documentation/assets/servo_testing/CleanShot_2024-05-09_at_02.12.012x.png)

GDW #3 seems very "stable" so far as well

will cancel that run and put in #4 before going to sleep

lets see how #4 holds up

#4 starts of in the same range as #2 and #3,

![GDW DS041MG #4 preliminary results](https://github.com/Enraged-Rabbit-Community/ERCF_v2/blob/master/Documentation/assets/servo_testing/CleanShot_2024-05-09_at_02.21.082x.png)

signing off for today, good night! 🙂

![GDW DS041MG #2 results](https://github.com/Enraged-Rabbit-Community/ERCF_v2/blob/master/Documentation/assets/servo_testing/CleanShot_2024-05-09_at_07.57.062x.png)

so, all 4 GDW Servos performed similar and stable without any degradation, spikes or failures

3000 push attemps with 5s pause like all the other runs, over ~5h time total per run, the temperature was also stying within reasonable limits

To be fair, my calibration isn't perfect for the load cell and pivot distance, i'm printing a new batch test jig right now to ensure almost exactly 1cm distance for the push measurement

`You da man! I am impressed with your ingenuity. This is all good info.`

Thanks, to be honest this really is kinda fun, but loads of things to consider/keep in mind, also bummed out a bit that i don't get good voltage/current readings

So don't exactly quote me on those values, but it does give quite some insight into the stability and differences

Will do a short retest of every Servo i have on the new jig for exact force comparison

new test jig gave me some headaches, somehow i can't read more than one load cell, so sadly no parallel tests, but i'm testing #1 of my guo hua now, the jig is now also quite a bit more consistant and freshly calibrated with a 1000g weight, so it should also give more accurate forces and comparison

![multi-servo test bed](https://github.com/Enraged-Rabbit-Community/ERCF_v2/blob/master/Documentation/assets/servo_testing/PXL_20240512_202447671.jpg)


Silverback_Attack_The_Dad_Ninja said:
I want to jump in here. The Promodeler servo is NOT a DS041MG. It's a totally different servo. I don't recommend making it part of the ERCF team's recommendation since it is expensive (relative to the chinese budget servos, but cheap compared to other high quality servos). Also, it is made in the US and shipped from the guy that makes them. He will do international shipping, but it will likely be more than the price of a kit from Ali by the time all is said and done. Here's a direct link: https://www.promodeler.com/DS105CLHV

Many people complain about the cost of shipping, but the servo comes in a substantial cardboard box, and will likely have a small gift in it as well (a beer can coozie most of the time, however I have received a ball cap as well). So, like Nebraska, the ProModeler option isn't for everyone. It's the option for people who don't want to worry about servo issues...ever.

I think the best option would be to just point users to my Github page for it from the ERCF github and let them know that it is a high quality option for those in the US.

As for the GDW DS014MG, I believe @moggieuk handled the issues with an update to Happy Hare that keeps the servo signal on. You just have to select it during the install script for HH. I have one and it has been good. More power than the MG90S, but it isn't a fast servo, so the dwell time needs to be higher, and the pause after command needs to be longer since it doesn't "snap" into position, but "floats" there.