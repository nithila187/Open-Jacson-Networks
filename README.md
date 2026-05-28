# Series Queues with infinite capacity - Open Jackson Network

## Aim :
To find (a) average number of materials in the system (b) average number of materials in the each conveyor of (c) waiting time of each material in the system (d) waiting time of each material in each conveyor, if the arrival  of materials follow Poisson process with the mean interval time 12 seconds, service time of  lathe machine in series follow exponential distribution  with service time  1 second, 1.5 seconds and 1.3 seconds respectively and average service time of robot is 7 seconds.

## Software required :
Visual components and Python

## Theory

![image](https://user-images.githubusercontent.com/103921593/203239736-7b81f599-71a8-4ae7-b63e-5d98acd9ea54.png)


## Procedure :

![image](https://user-images.githubusercontent.com/103921593/203239789-bc870dce-6727-487b-a0e2-4fc3f5114889.png)

## Experiment:
<img width="890" height="550" alt="image" src="https://github.com/user-attachments/assets/63af15ca-f0b6-43f9-8b2e-31f594e964c3" />

## Program:
```
arr_time=float(input("Enterthe meaninterarrival timeof objects fromFeeder(insecs):"))
ser_time1=float(input("Enterthe mean inter servicetimeof Lathe Machine1(in secs): "))
ser_time2=float(input("Enterthe mean inter servicetimeof Lathe Machine2(in secs): "))
ser_time3=float(input("Enterthe mean inter servicetimeof Lathe Machine3(in secs): "))
Robot_time=float(input("EntertheAdditional timetakenfor theRobot(insecs): "))
lam=1/arr_time
mu1=1/(ser_time1+Robot_time)
mu2=1/(ser_time2+Robot_time)
mu3=1/(ser_time3+Robot_time)
print("-----------------------------------------------------------------------")
print("SeriesQueueswithinfinitecapacity-OpenJacksonNetwork")
print("-----------------------------------------------------------------------")
if(lam< mu1)and(lam< mu2) and(lam< mu3):
Ls1=lam/(mu1-lam)
Ls2=lam/(mu2-lam)
Ls3=lam/(mu3-lam)
Ls=Ls1+Ls2+Ls3
Lq1=Ls1-lam/mu1
Lq2=Ls2-lam/mu2
Lq3=Ls3-lam/mu3
Wq1=Lq1/lam
Wq2=Lq2/lam
Wq3=Lq3/lam
Ws=Ls/(3*lam)
print("Averagenumberofobjects inthe system S1:%0.2f"%Ls1)
print("Averagenumberofobjects inthe system S2:%0.2f"%Ls2)
print("Averagenumberofobjects inthe system S3:%0.2f"%Ls3)
print("Averagenumberofobjects inthe overallsystem : %0.2f"%Ls)
print("Averagenumberofobjects inthe conveyorS1 : %0.2f"%Lq1)
print("Averagenumberofobjects inthe conveyorS2 : %0.2f"%Lq2)
print("Averagenumberofobjects inthe conveyorS3 : %0.2f"%Lq3)
print("Averagewaiting timeofan object intheconveyor S1: %0.2fsecs"%Wq1)
print("Averagewaiting timeofan object intheconveyor S2: %0.2fsecs"%Wq2)
print("Averagewaiting timeofan object intheconveyor S3: %0.2fsecs"%Wq3)
else:
print("Warning!ObjectsOver flowwillhappenintheconveyor")
print("----------------------------------------------------------------------")
```

## Output:
<img width="768" height="451" alt="image" src="https://github.com/user-attachments/assets/d1e63390-464e-4cc3-9bdc-c7fd7014fdba" />

## Result:
Thus, the program has been executed successfully and the required parameters have been calculated as per the given
conditions
