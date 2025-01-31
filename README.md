# Switch-Configuration

### Objective
  
Basic VLANs access points

### Skills Learned

- Basic VLANs access points commands and verification
- Learned how to configure switches through CLI command to get to configuration mode
- Learned how to assign different VLANs and Ports to the switch through CLI command

### Tools Used

- CISCO Packet Tracer

### Steps

*Ref 1: Example of a simple network example where a switch is connected to two computers with two simple static IP addresses as labeled on the image*

![image](https://github.com/user-attachments/assets/41790293-53f2-45de-9259-dd1a17f8e84b)


*Ref 2: Using the command prompt on the first computer (PC0) to ping the second computer (PC1) to see if they're connected and they are because they're connected to the same switch*

![image](https://github.com/user-attachments/assets/1e1b3c1e-8496-4c2c-b6f0-7cff1825fffe)

*Ref 3: Setting up some basic switch configuration, VLAN. For example we label PC0 as "User" and PC1 as "Accounting". We do not want them to communicate to each other.*

![image](https://github.com/user-attachments/assets/9a00bbc5-74eb-4cb9-9a34-27d254cd1ab9)

*Ref 4: We can put the User (PC0) on VLAN 2 and Accounting (PC1) on VLAN 3 so that they're on two different logical network*

![image](https://github.com/user-attachments/assets/44a38a56-f718-4c3c-beed-9b5c537d6fe8)

*Ref 5: Configuring the switch by going to the CLI prompt and entering "enable" to enable privilaged exec mode "Switch#"*

![image](https://github.com/user-attachments/assets/4c4b310f-72c6-46e8-8d81-f3e1a352043e)

*Ref 6: From "Switch#" enter command config t (configure terminal) to get "Switch(config)#, which is the configuration mode*

![image](https://github.com/user-attachments/assets/4567837f-3b1b-458f-b22f-f2daf3346a4f)

*Ref 7: Before we configure a switch we want to make sure there's no pre-existing VLAN on it. To do that type in "exit" from the terminal (Switch(config)#exit), then "Switch#show vlan" to see if there's any pre-existing VLAN*

![image](https://github.com/user-attachments/assets/57e6010f-90ee-458a-a6fb-de271dae38a5)

*Ref 8: Configuring VLAN on the switches by using the command "Switch(config-vlan)#name User-VLAN2", then exit out of that command and do it again for the second computer. Same command "Switch(config-vlan)# name Accounting-VLAN3"*

![image](https://github.com/user-attachments/assets/828d6b0e-dd2f-4fe2-b593-3e3f1786627b)

*Ref 9: To verify if the VLANs were configured correctly use command "Switch(config-vlan)#do show vlan" and there should be two additional VLANs including the default. "do" forces the command in CLI.*

![image](https://github.com/user-attachments/assets/4aa5555e-c611-4811-b8df-bb5277dd327c)

*Ref 10: To assign a port to VLAN2, hover over the green arrow by the switch to find the port, which is Fa0/1 in this example. So from there enter the command "Switch(config)#int Fa0/1

![image](https://github.com/user-attachments/assets/9680163c-9f1b-45b0-8982-ba165d7d6956)

*Ref 11: Configuring this port "Fa0/1" into an access port*

![image](https://github.com/user-attachments/assets/1c13d549-3a6c-4280-8995-826e7bea4c5b)

*TIP 1: If you don't remember the next command prompt then press "?" and it'll provide you a list*

![image](https://github.com/user-attachments/assets/30650e7f-0ed9-4f9b-80ef-c3ff952029f0)

*Ref 12: Applying Fa/0/1 to access port vlan 2. As you can see the orange circle means that the switch is resetting to the new configuration*

![image](https://github.com/user-attachments/assets/ed10f578-856c-4ea6-b14a-e6d2da38a6f2)

*TIP 2: Always remember to save your configurations incase the switch turns off. Use the command "exit" to go back to "Switch#" and from there type in "Switch#copy running-config startup-config, press enter two times to confirm. If you see [OK] it means your configuration was saved correctly - Though this is what the exam wants, in the real world use the short cut "Switch#wr" and it'll do the same thing.*

![image](https://github.com/user-attachments/assets/59c51390-6075-48b7-b81a-567d40e0def9)


