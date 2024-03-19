<h1>ExpNo 1 :Developing AI Agent with PEAS Description</h1>
<h3>Name: Saravanan N</h3>
<h3>Register Number/Staff Id: TSML006</h3>



## AIM:

To develop a PEAS description for the given AI problem and implement an AI agent for a vacuum cleaner.

## Theory:
### Vacuum Cleaner Agent:
This agent operates within a confined environment consisting of multiple rooms (four rooms in this case). The objective of the agent is to navigate through these rooms, detect and clean any dirt present. The agent's performance is determined by the efficiency with which it cleans the rooms. Each movement and cleaning action affects its performance. The environment comprises rooms with potential dirt spots, and the agent must use sensors to detect dirt and actuators to perform cleaning actions.

### PEAS DESCRIPTION:

|AgentType|	Performance	|Environment|	Actuators|	Sensors|
|--------|--------|	----------	|----------|	-----|	
|Vacuum Cleaner Agent	|Cleaning efficiency|	Rooms with potential dirt spots	|Vacuuming	|Cleaning sensors|



## ALGORITHM:

#### STEP 1: Identifying the input:
Detection of dirt spots in each room.

#### STEP 2: Identifying the output:
Perform cleaning actions in detected dirt spots.

#### STEP 3: Developing the PEAS description:
PEAS description is constructed based on the performance, environment, actuators, and sensors of the agent.

#### STEP 4: Implementing the AI agent:
Clean dirt spots in each room using vacuuming actions.

#### STEP 5: Measure the performance parameters:
Performance is determined by the percentage of cleaned spots in the rooms. Each cleaning action contributes positively to performance, while movement may affect performance negatively.

## CODE:
``` PYTHON
# Developed By : NAVEEN S
# Reg No : 212222110030
import random

class VacuumCleaner:
    def __init__(self):
        self.room = [
            [1, 1, 1, 1],
            [1, 1, 1, 1],
            [1, 1, 1, 1],
            [1, 1, 1, 1],
        ]

    def display_room(self):
        print("Room Status:")
        for row in self.room:
            print(row)

    def dirty_room(self):
        print("All the rooms are dirty")

    def random_dirt(self):
        for x in range(4):
            for y in range(4):
                self.room[x][y] = random.choice([0, 1])

    def clean_room(self):
        print("Before cleaning the room, detecting random dirt...")
        self.random_dirt()
        self.display_room()
        dirt_count = 0
        for x in range(4):
            for y in range(4):
                if self.room[x][y] == 1:
                    print("Vacuuming at location:", x, y)
                    self.room[x][y] = 0
                    print("Cleaned at location:", x, y)
                    dirt_count += 1
        print("Room is clean now.")
        self.display_room()
        performance = self.calculate_performance(dirt_count)
        print("Performance:", performance, "%")

    def calculate_performance(self, cleaned_count):
        total_spots = 16
        performance = (1 - (cleaned_count / total_spots)) * 100
        return performance

if __name__ == "__main__":
    vacuum = VacuumCleaner()
    vacuum.dirty_room()
    vacuum.clean_room()

```
## OUTPUT:
![image](https://github.com/MukeshVelmurugan/19AI405ExpNo1/assets/118707363/10548efe-b9d8-4e92-b8b2-ac2cf2354882)

### RESULT:
Thus the Developing AI Agent with PEAS Description was implemented using python programming.






