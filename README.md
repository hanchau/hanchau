# Hello there 👋

```python
#!/usr/bin/python
# -*- coding: utf-8 -*-

from BigData import Data
from job import tasks
from UPSC.CSE import study_tasks
import asyncio


class DataEngineer(Data):
    pass

class DataScientist(Data):
    pass

class DataScienceEngineer(DataEngineer, DataScientist):

    def __init__(self, name = "", role = ""):
        self.name = name
        self.role = role
        self.languages = ["Python3", "Java"]
        self.hobbies = ["music", "road_trips", "maths"]

    @classmethod
    def reborn(cls, name, role):
        return cls(name, role)

    def say_hi(self):
        print("Thanks for dropping by, hope you find something useful.")

    async def do_work(self):
        for i in range(0, len(tasks)):
            if i % 20 == 0:
                print("Hey, Can't you see I'm working")
                print("bc code fat gaya! told you to test regorously!!")
        return 0

    async def study(self):
        for i in range(0, len(study_tasks)):
            if i % 10 == 0:
                print("History, geography, current affairs.. zzz..")
                print("Fir sae sogaya.. kal karunga baaki.. zzz..")
        return 0

    async def here_and_there(self):
        f1 = loop.create_task(self.do_work())
        f2 = loop.create_task(self.study())
        await asyncio.wait([f1, f2])

    def get_back(self):
        struggle = asyncio.get_event_loop()
        struggle.run_until_complete(here_and_there())
        struggle.close()


if __name__ == "main":
    me = DataScienceEngineer()
    # oops, no name, time to reborn
    me = DataScienceEngineer.reborn("Anuj Chauhan", "Data Science Engineer")
    me.say_hi()
    me.get_back()
```

## To sum it up
![](https://github.com/hanchau/hanchau/blob/main/debug.gif)