# EX-04 Single Server with Infinite Capacity (M/M/1):(oo/FIFO)
### Aim :
To find (a) average number of materials in the system (b) average number of materials in the conveyor (c) waiting time of each material in the system (d) waiting time of each material in the conveyor, if the arrival  of materials follow poisson process with the mean interval time 12 seconds, serivice time of lathe machine follows exponential distribution with mean serice time 1 second and average service time of robot is 7seconds.
### Software required :
Visual components and Python.
### Theory:
Queuing are the most frequently encountered problems in everyday life. For example, queue at a cafeteria, library, bank, etc. Common to all of these cases are the arrivals of objects requiring service and the attendant delays when the service mechanism is busy. Waiting lines cannot be eliminated completely, but suitable techniques can be used to reduce the waiting time of an object in the system. A long waiting line may result in loss of customers to an organization. Waiting time can be reduced by providing additional service facilities, but it may result in an increase in the idle time of the service mechanism.
<img src="https://github.com/ROHITJAIND/EX-04-Single-Server-Infinite-Capacity-Markov-Model/assets/118707073/3a1e3acb-5e59-4fa7-8db8-2a7abb8ebb10">
This is a queuing model in which the arrival is Marcovian and departure distribution is also Marcovian,number of server is one and size of the queue is also Marcovian,no.of server is one and size of the queue is infinite and service discipline is 1st come 1st serve(FCFS) and the calling source is also finite.
### Procedure :
<img height=21% width=60% src="https://github.com/ROHITJAIND/EX-04-Single-Server-Infinite-Capacity-Markov-Model/assets/118707073/932ef1af-1768-4a3e-af26-5f8bc07d4b7c">

### Experiment :
<img height=15% width=50% src="https://github.com/ROHITJAIND/EX-04-Single-Server-Infinite-Capacity-Markov-Model/assets/118707073/646d9962-a984-4b3b-9a5c-ade5ae8ed6eb">

### Program :
```
Developed By: SIVAMOHANASUNDARAM. V
Register No: 212222230145
```

```Python
arr_time=float(input("Enter the mean inter arrival time of objects from Feeder (in secs): "))
ser_time=float(input("Enter the mean  inter service time of Lathe Machine (in secs) :  "))
Robot_time=float(input("Enter the Additional time taken for the Robot (in secs) :  "))
lam=1/arr_time
mu=1/(ser_time+Robot_time)
print("--------------------------------------------------------------")
print("Single Server with Infinite Capacity - (M/M/1):(oo/FIFO)")
print("--------------------------------------------------------------")
print("The mean arrival rate per second : %0.2f "%lam)
print("The mean service rate per second : %0.2f "%mu)
if (lam <  mu):
    Ls=lam/(mu-lam)
    Lq=Ls-lam/mu
    Ws=Ls/lam
    Wq=Lq/lam
    print("Average number of objects in the system : %0.2f "%Ls)
    print("Average number of objects in the conveyor :  %0.2f "%Lq)
    print("Average waiting time of an object in the system : %0.2f secs"%Ws)
    print("Average waiting time of an object in the conveyor : %0.2f secs"%Wq)
    print("Probability that the system is busy : %0.2f "%(lam/mu) )
    print("Probability that the system is empty : %0.2f "%(1-lam/mu) )
else:
    print("Warning! Objects Over flow will happen in the conveyor")
print("---------------------------------------------------------------")
```
### Output :
<table border=5>
    <tr>
        <td>
            
```C
Enter the mean inter arrival time of objects from Feeder (in secs): 12
Enter the mean  inter service time of Lathe Machine (in secs) :  1
Enter the Additional time taken for the Robot (in secs) :  7
--------------------------------------------------------------
Single Server with Infinite Capacity - (M/M/1):(oo/FIFO)
--------------------------------------------------------------
The mean arrival rate per second : 0.08 
The mean service rate per second : 0.12 
Average number of objects in the system : 2.00 
Average number of objects in the conveyor :  1.33 
Average waiting time of an object in the system : 24.00 secs
Average waiting time of an object in the conveyor : 16.00 secs
Probability that the system is busy : 0.67 
Probability that the system is empty : 0.33 
---------------------------------------------------------------
```
</td>
</tr>
</table>

### Result :
The average number of material in the sysytem and in the conveyor and waiting time are successfully found.
