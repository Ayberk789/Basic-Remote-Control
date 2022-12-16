import random
import time
class Remote_Controller():
    def __init__(self,tv_status = "Tv is OFF",tv_volume = 0,channel_list = ["FOX"],channel = "FOX"):
        self.tv_status = tv_status
        self.tv_volume = tv_volume
        self.channel_list = channel_list
        self.channel = channel
    def tv_on (self):
        if self.tv_status == "Tv is ON":
            print("TV is already ON")
        else:
            print("Tv is ON")
            self.tv_status = "Tv is ON"
    def tv_off (self):
        if self.tv_status == "Tv is OFF":
            print("Tv is already OFF")
        else:
            print("Tv is OFF")
            self.tv_status = "Tv is OFF"
    def volumesettings (self):
        while True:
            answer = input("Turn down: '<'\nTurn up: '>'\nExit: q")
            if answer == "<":
                if self.tv_volume != 0:
                    self.tv_volume -= 4
                print("Volume:",self.tv_volume)
            elif answer == ">":
                if self.tv_volume != 100:
                    self.tv_volume += 4
                print("Volume:",self.tv_volume)
            else:
                print("Volume level has been updated:",self.tv_volume)
                break
    def add_channel(self,channel_name):
        print("New channel has been added...",channel_name)

        self.channel_list.append(channel_name)

    def random_channel(self):
        rand = random.randint(0,len(self.channel_list)-1)
        self.channel = self.channel_list[rand]
        print("Channel: ",self.channel)
    def __len__(self):
        return len(self.channel_list)
    def __str__(self):
        return "Tv Status: {}\nVolume Level: {}\nChannel List: {}\nCurrently Channel: {}".format(self.tv_status,self.tv_volume,self.channel_list,self.channel)
Rcontroller = Remote_Controller()
print("""
    
    Remote Controller Application...
    
    1- Turn on TV
    2- Turn Off TV
    3- Volume Settings
    4- Add New Channel
    5- Surfing on Random Channels
    6- Channel List
    7- Info
    
    For exit please press "q"...
    """)

while True:
    Operations = input("Select Prosses:")
    if Operations == "q":
        break
    elif Operations == "1":
        Rcontroller.tv_on()
    elif Operations == "2":
        Rcontroller.tv_off()
    elif Operations == "3":
        Rcontroller.volumesettings()
    elif Operations == "4":
        channel_names = input("Please add ',' symbol between channel names ")
        channel_list = channel_names.split(",")
        for adding in channel_list:
            Rcontroller.add_channel(adding)
    elif Operations == "6":
        print("Channel List: ",len(Rcontroller))
    elif Operations == "5":
        Rcontroller.random_channel()
    elif Operations == "7":
        print(Rcontroller)
    else:
        print("Error...")
