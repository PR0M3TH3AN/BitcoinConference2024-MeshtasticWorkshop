# Meshtastic Workshop Script

### 7/21/2024

---

#### Slide 1

![](http://hedgedoc.malin.onl/uploads/67805f4c-ecf3-477b-b0c9-5099386e92c7.jpg)

Hey everyone, thanks for joining us here at this Meshtastic Workshop at Bitcoin 2024! My name is Adam Malin. By day I am a graphic designer at Oak Ridge National Laboratory, and by night I am a Bitcoiner trying to find the best freedom technology for me and my family.

I believe Bitcoin is crucial for preserving my time and energy. Nostr is crucial for securing my free speech.

But what if internet and cellular networks go down? How will I communicate with my family or those I care about? This is where Meshtastic comes in.

Meshtastic and LoRa create a low-cost, low-power mesh relay network of long-range, encrypted radio devices. This network doesn't need cellular signal or WiFi to send text messages. The more people using Meshtastic and LoRa, the better the network coverage for everyone.

---

#### Slide 2

![](http://hedgedoc.malin.onl/uploads/2a1d6afb-7618-4202-9bcb-4e4c65268ef2.jpg)

Before we keep going, there are two key points to cover:

LoRa is a cost-effective, low-powered mesh radio network designed for text data transmission over long distances without relying on cellular or WiFi signals.

Meshtastic combines radio firmware with an open-source app to enable communication over the LoRa mesh. This allows for seamless and encrypted communication across the network.

---

#### Slide 3

![](http://hedgedoc.malin.onl/uploads/ecfd37b7-3548-4a80-97a6-eb66cacc19a5.jpg)

Always remember to attach your devices antenna before powering on a LoRa device to prevent damage. This is a crucial step for proper device functioning and to prevent damage to the radio.

---

#### Slide 4

![](http://hedgedoc.malin.onl/uploads/633470c4-920a-4be6-93e6-c734b4e30a6d.jpg)

LoRa, which stands for Long Range, is a spectrum modulation technique derived from chirp technology. It operates on unlicensed frequency bands like 868 MHz in Europe and 915 MHz in North America. 

LoRa uses this ‘chirp pattern’ signaling method, which makes the signal robust, allowing it to penetrate through obstacles and cover long distances. Due to its low power consumption, LoRa devices can operate on batteries for weeks, making them ideal for remote or mobile deployments.

---

#### Slide 5

![](http://hedgedoc.malin.onl/uploads/bd1741a2-7cac-406d-ab5c-dcc631d44834.jpg)

LoRa is extensively used in IoT applications such as smart cities, agriculture, and environmental monitoring. Typically sending sensor data to and from remote locations. Its ability to transmit encrypted data over long distances with minimal power makes it ideal for these uses.

---

#### Slide 6

![](http://hedgedoc.malin.onl/uploads/519dc9a0-1c03-41e8-befd-597429e1f373.jpg)
Why Choose LoRa Over Ham Radio’s APRS for Secure Communication? 

Ham radios are limited by FCC regulations on frequencies and power levels, and encoded messages are prohibited. This means that while Ham radio can be useful for many forms of communication, it falls short when it comes to securely transmitting encrypted data.

LoRa, on the other hand, provides an alternative options for encrypted communication. This is particularly important the potential of sending secure eCash transactions in the future. LoRa's ability to transmit encrypted messages over long distances with minimal power consumption makes it an ideal choice for secure and reliable communications.

---

#### Slide 7

![](http://hedgedoc.malin.onl/uploads/bfda2abb-0b27-4351-9827-6a0cc4f6141f.jpg)

Meshtastic is an innovative, open-source chat application that leverages the LoRa Mesh for communication. It offers robust off-grid messaging capabilities, making it a powerful tool for truly decentralized communication.

It’s important to understand that Meshtastic consists of two key components. Firstly, it is an app on your phone that you use to compose and send messages. Secondly, it includes custom firmware that is loaded onto a LoRa-capable radio. These two components work together seamlessly over Bluetooth. Your phone sends the message via Bluetooth to the LoRa radio, which then broadcasts the message to the local area over radio frequencies.

---

#### Slide 8

![](http://hedgedoc.malin.onl/uploads/0149b03c-e1a3-4d80-9c40-3261e2430153.jpg)

To get started with Meshtastic, the first step is to select a suitable LoRa and Meshtastic capable device based on your needs. Examples include Heltec v3, T-Beam, T-Deck, or Wizblock. There are many more. 

It’s crucial to choose the correct LoRa frequency for your region. For instance, the U.S. uses LoRa 915 MHz, while other regions might use 868 MHz or other frequencies. Ensure you have the right hardware for your location to achieve optimal performance.

---

#### Slide 9

![](http://hedgedoc.malin.onl/uploads/5742ec21-f2a0-462b-b434-5a707b5eb82f.jpg)

Because these devices are such low power, there are many ways you can choose to power them.

1. Laptop/USB
2. Small Solar Panel
3. A Coinkite ColdPower
4. A USB battery bank

---

#### Slide 10

![](http://hedgedoc.malin.onl/uploads/000268be-e142-4708-94e0-79c7749c2855.jpg)

Once you have selected the right device and power method, next we will need to flash the Meshtastic firmware.

In this example we will be using the HelTec V3. Make sure to connect your antenna before powering one the radio. Once connected to your computer you should see a screen that looks like this on the LoRa device. 

To  flash your device with the correct firmware we will be using the Meshtastic online device flashing tool and the Chrome web browser. 

Something to note here: If your using a Linux distribution and your Chrome browser is a containerized application like an AppImage or flatpak format you might have connection issues between the browser and the LoRa device. So try using an integrated version of Chrome via APT or another integrated package manager. At the moment this process does usually go more smoothly on a Windows PC.

---

#### Slide 11

![](http://hedgedoc.malin.onl/uploads/d91136cb-8a55-47db-8f3b-11e8c3ac8439.jpg)

Go to flasher.meshtastic.org and select the correct device that you have connected using the first drop down menu. 

Then select the version of the firmware you with to install. I typically use the latest Stable version.

And then select the Flash button on the right.

---

#### Slide 12

![](http://hedgedoc.malin.onl/uploads/8f446ae6-9291-4e24-8833-96428a087b3c.jpg)

You will then be asked if you wish to Erase and Install the new firmware. We want to select Yes.

Then the Chrome browser will ask for permission to connect to the device. If you are unsure which USB device it is then you can just unplug the LoRa device and plug it back in to see which one pops up again. Click “Connect” then click the “Erase Flash and Install” button.

---

#### Slide 13

![](http://hedgedoc.malin.onl/uploads/7d66cc61-f369-4bfb-a299-6f628d1cc3f2.jpg)

Now were done on the LoRa device side of things. You should now see a Meshtastic screen on the device with a connection code under the logo. We will use this to connect our phone with this radio.

---

#### Slide 14

![](http://hedgedoc.malin.onl/uploads/1b646ef5-7b37-447c-8f0e-388954fef2f4.jpg)

To connect your phone to your Meshtastic enabled radio we need to install the Meshtastic app on your Android or iPhone. 

I’ll will start with the iPhone version of the app.

1. Connect your LoRa device to your phone via Bluetooth using the Meshtastic app as well as the code you will find on the screen of your LoRa device.

2. Set the LoRa Region to “United States”.

3. Then you can setup the public and private channels. The default public channel is called “LongFast”. Its key is AQ== and is known to everyone.

I will show how to easily connect to our Bitcoin Conference Channels later in the slides. And this presentation will be available for download.


---

#### Slide 15

![](http://hedgedoc.malin.onl/uploads/9a2166d4-82dc-4866-acd9-1cc693aa80d2.jpg)

Next lets walk through the Android setup since they are slightly different. 

1. With the Meshtastic Device powered on, Click the + button to add the nearby Meshtastic Device using the code on the LoRa devices screen. 

2. Change the Region to “US”.

3. Select the “Channel” tab and click on “Edit” to add your own private channels here.

4. Click on “Add Channel” and enter the Channel Details or Scan the QR code and have it set automatically. If you already have channels setup be sure to save the URL or QR code for restoration later before scanning the new QR code.

---

#### Slide 16

![](http://hedgedoc.malin.onl/uploads/8a5c4009-3cef-4357-8f3a-0346e6f9994d.jpg)

If you already have a Meshtastic Device, you can join our private Bitcoin Conference chat channels. Here is the information you will need to connect. Open the Meshtastic app, go to the Channels tab and scan the code. 

Again, If you already have some custom channels setup make sure to backup your configuration or save your Channel URL somewhere so you can restore them later before scanning this code. 

---

#### Slide 17

![](http://hedgedoc.malin.onl/uploads/4bc92b08-26e3-431a-9a97-77f2067d703a.jpg)

Ok, now we will take a deeper look at how Meshtastic works over LoRa to create a reliable communication network. The Meshtastic mesh broadcast algorithm includes four conceptual layers:

Layer 0: LoRa radio as the base of the network.

Layer 1: Unreliable Zero Hop Messaging

Layer 2: Reliable Zero Hop Messaging

Layer 3: Naive Flooding for Multi-Hop Messaging

Each layer is crucial for ensuring reliable and efficient communication over the mesh network.

---

#### Slide 18

![](http://hedgedoc.malin.onl/uploads/7b67607f-8ac6-4a75-a09c-51853b2f7c4f.jpg)

Layer 0 is the LoRa Radio, which handles the conversion of data into the chirp LoRa symbols. This layer forms the foundation of Meshtastic communication.

---

#### Slide 19

![](http://hedgedoc.malin.onl/uploads/bf56cf34-799e-4236-878d-22809c84cd14.jpg)

Layer 1 handles Unreliable Zero Hop Messaging, which includes conventional LoRa packet transmission from one node to another. Packets are equipped with identification data, followed by encrypted payload data. Nodes perform checks at this stage before transmitting to avoid signal collisions.

---

#### Slide 20

![](http://hedgedoc.malin.onl/uploads/d3b0b0ca-3555-4bd4-aaef-356b597de59c.jpg)

Layer 2 adds reliability to the messaging process by sending what is called a “WantAck” flag. This is a request for the receiver to acknowledge delivery of the message from the sender. Broadcasting Nodes listen for these acknowledgments or “ACKs”. If no “ACK” is received, then the packet is retransmitted up to three times to ensure delivery.

---

#### Slide 21 

![](http://hedgedoc.malin.onl/uploads/84238913-e197-4ace-b8ec-152fd1ff4cc9.jpg)

Layer 3 uses flooding to propagate messages across the network. Nodes reduce the HopLimit and retransmit the message if needed. Nodes further away with lower Signal-to-Noise Ratio (SNR) rebroadcast first to extend the message range.

---

#### Slide 22

![](http://hedgedoc.malin.onl/uploads/0cca0327-76dd-4797-bf1c-69939ec68d83.jpg)

For optimal performance, Meshtastic devices, also known as nodes, should be placed in locations with a clear line of sight to each other. Obstructions such as hills and buildings can reduce the range of these nodes and increase the need for more nodes in the area to maintain reliable communications.

A “node” in this context refers to any device in the network that can send, receive, or relay messages.

---

#### Slide 23

![](http://hedgedoc.malin.onl/uploads/4f02e204-69ba-439e-a0e1-2966d84621b8.jpg)

Here is an example of a well placed node at the top of this hill. This node is able to relay the messages and expand the networks reach. 

---

#### Slide 24

![](http://hedgedoc.malin.onl/uploads/9d2adeef-fdce-48d5-affd-9aaa3e739dd5.jpg)

Let's talk about Meshtastic and encryption one more time. Here we will look at how keep communications secure for yourself and those in your channels.

Meshtastic uses strong AES256 encryption to secure your messages, ensuring they remain private.

Each channel has its own unique key. By default, there’s a simple key everyone knows which is AQ== for the default LongFast channel. For better security on our Bitcoin Conference Channels, we set up the channels with a unique key and have shared it with everyone here outside the mesh. 

Direct Messages over Meshtastic are not as secure as using a dedicated shared and private channel since the encryption key for the DMs is known to everyone of your contact is from the default LongFast Channel. Its best for security to send Channel Keys to new users you would like to communicate with outside the mesh network and not through DMs.

Let's look at some other important security considerations when using Meshtastic.

Always keep your radio device secure. If someone gets access to your device, they could potentially access your communications, since the Channel Key is stored on the LoRa radio device.

Be careful with sharing your channel QR code or URL with others. Only share it with trusted people to keep your messages and the messages of others in your channels private.

Remember, encryption can be turned off if needed like for “Ham Radio mode”, but it's best to keep it on for privacy.

---

#### Slide 25

![](http://hedgedoc.malin.onl/uploads/42b6e56c-e5e3-4412-8e36-0a5508b67120.jpg)

Here are some practical use cases for Meshtastic and LoRa, showing how these technologies can be effectively utilized in various scenarios.

Rural Area Connectivity: LoRa/Meshtastic can provide reliable communication in rural areas where traditional infrastructure is lacking or nonexistent.

Outdoor Adventures: For hikers, campers, and kayakers, LoRa/Meshtastic offers a dependable way to stay in touch with your group in remote locations where cell service is unavailable, enhancing safety and coordination.

Disaster Response: During natural disasters or other emergency situations, when traditional communication networks fail or are overloaded with traffic, LoRa/Meshtastic can be used as an alternative communication network, ensuring that vital information is quickly relayed throughout the community.

---

#### Slide 26

![](http://hedgedoc.malin.onl/uploads/33dfe890-0086-477d-98de-8e311f36231e.jpg)

I want to also shout out ‘The Comms Channel’ (TC2) on YouTube. He has some of the most informative and comprehensive Meshtastic content available. He’s working on some really cool Meshtastic related projects, like his Meshtastic BBS server as well as various Solar Meshtastic node designs. So, if you're interested in building out your area with Meshtastic nodes, whether that be for solar, mobile, or a home base stations, check out his content. I’m sure you will find it helpful.

---

#### Slide 27

![](http://hedgedoc.malin.onl/uploads/6f0a9843-d267-4cdd-9ac1-b7480a5479de.jpg)

Feel free to reach out to me on Nostr at thePR0M3TH3AN if you have any other questions that we don't cover today!

---

#### Slide 28

![](http://hedgedoc.malin.onl/uploads/fe106867-1b0c-4a57-87f6-0c4ca4178799.jpg)

Before we move into the Q&A segment, let’s recap the key takeaways from today’s workshop:

Meshtastic is open-source software that uses the LoRa mesh for decentralized, off-grid communication. It consists of a phone application and custom firmware on a LoRa radio devices, working together over Bluetooth.

Meshtastic uses strong encryption to ensure the confidentiality and security of your messages. Understanding how the channel keys work is crucial for maintaining that security.

For optimal mesh network performance, place nodes in locations with clear lines of sight. For more strategic placements, consider landscape topology and obstructions as well as the locations of other nodes in your area. This will enhances the networks reliability.

Meshtastic can be used for rural connectivity, emergency communication, and mobile mesh networks.

Now, I’d be happy to answer any questions you may have.

---

#### Slide 29

![](http://hedgedoc.malin.onl/uploads/31826703-ce25-493d-91db-40ea05ac262a.jpg)

Here are some links to Meshtastic resources as well as a download link for this entire presentation. 

The large QR code here are the Bitcoin Conference Meshtastic Private Channels. Scan them and join in on the conversation over the radio waves.

Thanks for joining us for this Meshtastic workshop, I hope it was informative and enjoy the rest of the conference!