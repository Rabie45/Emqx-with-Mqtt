# Emqx-with-Mqtt
EMQ X (formerly known as EMQTT) is an open-source, highly scalable, distributed MQTT message broker written in Erlang/OTP. It is designed for handling massive amounts of MQTT connections and messages efficiently.
# mqtt with emqx
## Whats is mqtt?
 - MQTT (Message Queuing Telemetry Transport) is a lightweight messaging protocol designed for constrained devices and low-bandwidth, high-latency or unreliable networks. It is commonly used in IoT (Internet of Things) and M2M (Machine-to-Machine) communications due to its simplicity and efficiency.
Key Features of MQTT:

    Lightweight: MQTT is designed to be lightweight both in terms of bandwidth usage and implementation complexity. This makes it suitable for devices with limited resources, such as sensors and embedded systems.

    Publish-Subscribe Architecture: MQTT uses a publish-subscribe messaging pattern where clients (devices or applications) can publish messages to topics. Other clients can subscribe to these topics to receive messages.

    Quality of Service (QoS): MQTT supports different levels of QoS to ensure message delivery reliability:
        QoS 0 (At most once): The message is delivered at most once or not at all.
        QoS 1 (At least once): The message is delivered at least once, ensuring no message loss but may result in duplicates.
        QoS 2 (Exactly once): The message is delivered exactly once by using a handshake mechanism to confirm delivery.
        
        
## install in ubuentu
 -
 ```
 sudo apt update && sudo apt install -y \
apt-transport-https \
ca-certificates \
curl \
gnupg-agent \
software-properties-common
```
 - ```curl -fsSL https://repos.emqx.io/gpg.pub | sudo apt-key add -```
 - ```sudo apt-key fingerprint 3E640D53```
 -
```
sudo add-apt-repository \
"deb [arch=amd64] https://repos.emqx.io/emqx-ce/deb/ubuntu/ \

$(lsb_release -cs) \
stable"
```
 - ``` sudo apt install emqx```
 - ```sudo emqx start```
  
## Install mqtt Client (MQTTX)
  - https://mqttx.app/downloads 
    ![Screenshot from 2024-07-10 11-33-37](https://github.com/Rabie45/Emqx-with-Mqtt/assets/76526170/1fe3d6a0-279f-4707-a145-201379294abe)
  - I used x86-64 | v1.10.0.deb
  - use this command to install the file after download ``` sudo dpkg -i <File_Name> ```
  - Open it with writing ```mqttx``` in terminal
![Screenshot from 2024-07-10 11-36-49](https://github.com/Rabie45/Emqx-with-Mqtt/assets/76526170/fe1c3e70-aebc-44a8-a6c5-fcb10f9d82c1)
    

## mqttx create Topics
 - Press new connection enter the name and the ip of the device that used to lanuch emqx
   ![Screenshot from 2024-07-10 11-37-47](https://github.com/Rabie45/Emqx-with-Mqtt/assets/76526170/61422b07-5767-4424-a6f9-3ca7c05f60dc)

 - Press new Subscription I will make 2 subs Temp  and Numbers as shown
   ![Screenshot from 2024-07-10 11-41-48](https://github.com/Rabie45/Emqx-with-Mqtt/assets/76526170/32dd33b9-df80-42d2-b57b-f7cbe0e6b109)
   ![Screenshot from 2024-07-10 11-42-10](https://github.com/Rabie45/Emqx-with-Mqtt/assets/76526170/3510b956-149a-4ae3-8a97-0af957bbe51b)
  

 
## Create another client with Smart phone 
![53845](https://github.com/Rabie45/Emqx-with-Mqtt/assets/76526170/8a9b56dd-a8d7-4058-973c-91731b7e5a26)
 - Add the broker data
![image](https://github.com/Rabie45/Emqx-with-Mqtt/assets/76526170/658e60c5-0ec2-4163-9724-ff2313d31ac7)
 - Connect
 - Go to publish button
 - Write the Topic and message 
 - Press Publish
   ![image](https://github.com/Rabie45/Emqx-with-Mqtt/assets/76526170/e69d6177-1d39-48c1-920c-c7368476c9de)
 - The data appers in the mqttx client
    ![Screenshot from 2024-07-10 11-48-30](https://github.com/Rabie45/Emqx-with-Mqtt/assets/76526170/c6cff5df-449e-4c05-ab0b-794da5327540)



