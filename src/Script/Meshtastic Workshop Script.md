# Meshtastic Workshop Script

### 7/21/2024

---

#### Slide 1

![](http://hedgedoc.malin.onl/uploads/d7a54fa2-1e32-4e5d-a4da-d0bae09d37dc.jpg)

Hey everyone, thanks for joining us here at this Meshtastic Workshop at Bitcoin 2024! My name is Adam Malin. By day I am a graphic designer at Oak Ridge National Laboratory, and by night I am a Bitcoiner trying to find the best freedom technology for me and my family.

I believe Bitcoin is crucial for preserving my time and energy. Nostr is crucial for securing my freedom of speech online.

But happens when we have another Cloud Strike event, and critical internet and cellular services go down? How would you communicate with friends and family? This is where Meshtastic comes in.

Meshtastic and LoRa together can create a mesh relay network of encrypted radio devices. Because this network is its own infrastructure, it doesn't need cellular or WiFi signal to send text messages. The more people using Meshtastic and LoRa, the better the network coverage for everyone. Another way to think about this is to imagine LoRa is the Interstate System and Meshtastic is the car.

---

#### Slide 2

![](http://hedgedoc.malin.onl/uploads/6e428874-85f6-45ba-ba5a-24f01619c9eb.jpg)

Here are some of the topics we will try to cover today. 

---

#### Slide 3

![](http://hedgedoc.malin.onl/uploads/a00f8c33-2b69-4d8a-8a34-87ccaca12238.jpg)

Before we keep going, there are two key terms to cover: LoRa and Meshtastic.

LoRa is a cost-effective, low-powered mesh radio network designed for text data transmission over long distances without relying on cellular or WiFi signals.

Meshtastic combines open-source radio firmware that is loaded onto these LoRa devices with an open-source app to enable communication over the LoRa mesh network. This allows for seamless and encrypted communication across the network.

---

#### Slide 4

![](http://hedgedoc.malin.onl/uploads/645e9c3c-2db0-4583-ac65-b0a93c19455f.jpg)

LoRa, which stands for Long Range, is a spectrum modulation technique. It operates on unlicensed frequencies like 868 MHz in Europe and 915 MHz in North America. 

LoRa uses a ‘chirp pattern’ signaling method, which allows the signal to better penetrate through obstacles and also cover long distances. Due to its low power consumption, LoRa devices can operate on batteries for weeks at a time, making them ideal for remote or mobile deployments.

---

#### Slide 5

![](http://hedgedoc.malin.onl/uploads/30f50664-575f-4205-820b-7424cdc49f2b.jpg)

LoRa has been extensively used in Internet of Things (IoT) applications such as smart cities, agriculture, and environmental monitoring. Typically sending sensor data to and from remote locations. LoRa’s ability to transmit encrypted data over long distances with minimal power makes it ideal for these situations.

---

#### Slide 6

![](http://hedgedoc.malin.onl/uploads/b66615ff-5602-4c34-8a8e-bfca7ee4d936.jpg)

Why did Meshtastic choose LoRa Over Ham Radio’s APRS for Secure Communication?

Ham radios are limited by FCC regulations on frequencies and power levels, and encoded messages are prohibited. This means that while Ham radio can be useful for many forms of communication, it falls short when it comes to securely transmitting encrypted data.

LoRa, on the other hand, provides an alternative options for encrypted communication. This is particularly important for the potential of sending secure eCash transactions in the future. LoRa's ability to transmit encrypted messages over long distances while using minimal power makes it an ideal choice for secure and reliable communications.

---

#### Slide 7

![](http://hedgedoc.malin.onl/uploads/9c934219-67a5-44ba-81c8-394934220d84.jpg)

So now that we have discussed LoRa, lets move on to Meshtastic.

Meshtastic is an innovative, open-source chat application that leverages the LoRa Mesh for communication. It enables off-grid messaging capabilities, making it a powerful tool for a truly decentralized communication network.

It’s important to understand that Meshtastic consists of two key components. Firstly, it is an app on your phone that you use to write and send messages. Secondly, it includes custom firmware that is loaded onto a LoRa-capable radio. These two components work together seamlessly over Bluetooth. Your phone sends the message via Bluetooth to the LoRa radio, which then broadcasts the message to the local area over the radio frequencies.

---

#### Slide 8

![](http://hedgedoc.malin.onl/uploads/8c5a980d-81d5-40fa-bab2-50fa3fdf00ec.jpg)

How do you get started with Meshtastic? The first step is to select a suitable LoRa and Meshtastic capable device based on your needs. Examples might include Heltecs, T-Beams, T-Decks, or Wizblocks and many more.

It’s crucial to choose the correct LoRa frequency for your region. For instance, the U.S. uses LoRa 915 MHz, while other regions might use 868 MHz or other frequencies. Ensure that you have the right hardware for your location.

---

#### Slide 9

![](http://hedgedoc.malin.onl/uploads/5f0b940a-498f-4032-b142-1634f37c283e.jpg)

Next we will talk about setting up a Meshtastic device. Because these devices are such low power, there are many ways you can choose to power them.

From Laptops and USB ports to solar panels, battery banks and even Bitcoin hardware like a ColdPower could be used.

---

#### Slide 10

![](http://hedgedoc.malin.onl/uploads/71fd4584-313c-4b02-9b8f-67ce40c3e405.jpg)

Once you have selected the right device and power method, next we will need to flash the Meshtastic firmware onto the radio.

In this example we will be using the HelTec V3. Make sure to connect your antenna before powering one the radio. Once connected to your computer you should see a screen that looks like this on the LoRa device.

To  flash your device with the correct firmware we will be using the Meshtastic online device flashing tool and the Chrome web browser.

Something to note here, If your using a Linux distribution and your Chrome browser is a containerized application like an AppImage or flatpak format you might have connection issues between the browser and the LoRa device. So try using an integrated version of Chrome via APT or another integrated package manager. At the moment this process does usually go more smoothly on a Windows PC.

---

#### Slide 11

![](http://hedgedoc.malin.onl/uploads/dbf7ed5d-d90f-4c40-b4a4-5d3f46c1ef26.jpg)

Once connected, go to flasher.meshtastic.org and select the correct device that you have connected using the first drop down menu on the left.

Then select the version of the firmware you with to install. I typically use the latest Stable version.

And then select the Flash button on the right.

---

#### Slide 12

![](http://hedgedoc.malin.onl/uploads/9d50ebd6-c905-49b1-88e0-66a10c8e6477.jpg)

You will then be asked if you wish to “Erase and Install” the new firmware. We want to select Yes.

Then the Chrome browser will ask for permission to connect to the device. If you are unsure which USB device it is then you can just unplug the LoRa device and plug it back in to see which one pops up again. Click “Connect” then click the “Erase Flash and Install” button.

---

#### Slide 13

![](http://hedgedoc.malin.onl/uploads/293c10f8-debd-4a8a-8cf8-5c56bfc37569.jpg)

Now were done on the LoRa device side of things. You should now see a Meshtastic screen on the device with a connection code under the logo. We will use this one-time code to connect the phone to this radio.

---

#### Slide 14

![](http://hedgedoc.malin.onl/uploads/e0364743-475c-408b-af00-ce3532bfe5aa.jpg)

To connect your phone to your Meshtastic enabled radio we need to install the Meshtastic app on your Android or iPhone.

I’ll will start with the iPhone version of the app.

1. Connect your LoRa device to your phone via Bluetooth using the Meshtastic app as well as the code you will find on the screen of your LoRa device.

2. Set the LoRa Region to “United States”.

3. Then you can setup the public and private channels. The default public channel is called “LongFast”. Its encryption key is AQ==. This key is known to everyone.

Later in the slides I will show how to connect to the Bitcoin Conference Channels we have setup. Also this presentation will be available to download for reference.

---

#### Slide 15

![](http://hedgedoc.malin.onl/uploads/be73d811-6c10-4e2e-9945-3becd08fa62a.jpg)

Next lets walk through the Android setup since they are slightly different.

1. After installing the Meshtastic App, power on the device and then Click the + button to add the nearby device. Then put in the one-time code from the LoRa devices screen. 

2. Change the Region to “US”.

3. Select the “Channel” tab and click on “Edit” to add your own private channels here.

4. Click on “Add Channel” and enter the Channel Details or Scan the QR code and have it set automatically. If you already have channels setup be sure to save the URL or QR code for restoration later before scanning this new QR code.

---

#### Slide 16

![](http://hedgedoc.malin.onl/uploads/a1c07825-f577-4e66-911b-d590ad720d32.jpg)

If you already have a Meshtastic Device, you can join our private Bitcoin Conference chat channels that we have setup. Here is the information you will need to connect. Open the Meshtastic app, go to the Channels tab and scan the code. 

Again, If you already have some custom channels setup make sure to backup your configuration or save your Channel URL somewhere so you can restore them later before scanning this code.

---

#### Slide 17

![](http://hedgedoc.malin.onl/uploads/07c4c24c-db62-4261-adbe-d5217c0f559f.jpg)

Ok, now we will take a deeper look at how Meshtastic works over LoRa to create a reliable communication network. The mesh broadcast algorithm includes four conceptual layers:

The base layer is the LoRa Radio. On top of that we have “Unreliable Zero Hop Messaging” then “Reliable Zero Hop Messaging” and finally on the top we have “Naive Flood Routing” for multi-hop messaging.

Each layer is crucial for ensuring reliable and efficient communication over this network.

---

#### Slide 18

![](http://hedgedoc.malin.onl/uploads/a1248cf5-7960-4808-a5ec-3e69367a260e.jpg)

Layer 0 is the LoRa Radio. This handles the conversion of data into the chirp LoRa symbols. This layer forms the foundation of all Meshtastic communication.

---

#### Slide 19

![](http://hedgedoc.malin.onl/uploads/730ef9d7-8b78-4ebe-a09f-0194ddfd2349.jpg)

Layer 1 handles Unreliable Zero Hop Messaging. This includes conventional LoRa packet transmission from one node to another. These packets are equipped with identification data, followed by encrypted payload data. At this stage, the nodes perform checks before transmitting to avoid signal collisions.

---

#### Slide 20

![](http://hedgedoc.malin.onl/uploads/ccba7397-5c51-4851-a767-397e8d14c1fc.jpg)

Layer 2 adds reliability to the messaging process by sending what is called a “WantAck” flag. This is a request for the receiver to acknowledge delivery of the message from the sender. Broadcasting nodes listen for these acknowledgments or “ACKs”. If no “ACK” is received, then the packet is retransmitted up to three times to ensure successful delivery.

---

#### Slide 21

![](http://hedgedoc.malin.onl/uploads/08337476-7aaa-4514-8fb5-b71dad9f6ca0.jpg)

Layer 3 uses flood routing to propagate messages across the network. Nodes reduce the HopLimit and retransmit the message they received if needed. Nodes further away with lower Signal-to-Noise Ratio (SNR) rebroadcast first to extend the message range.

---

#### Slide 22

![](http://hedgedoc.malin.onl/uploads/e17bb1e4-fb33-46e2-b755-8a909e75b033.jpg)

Now that we understand how Meshtastic works, lets look at how we can optimize this network for sending our messages.

Devices, also known as “nodes”, should be placed in locations with a clear line of sight to each other. Obstructions such as hills and buildings can reduce the range of these nodes and increase the need for more nodes in the area to maintain reliable communications.

A “node” in this context refers to any device in the network that can send, receive, or relay messages.

---

#### Slide 23

![](http://hedgedoc.malin.onl/uploads/566321b9-2ea6-4ddb-871d-61f061c9d48c.jpg)

Here is an example of a well placed node at the top of this hill. This node is able to relay the messages and expand the networks reach.

---

#### Slide 24

![](http://hedgedoc.malin.onl/uploads/66017579-20da-4f7c-b1a9-5c90b57ea3cf.jpg)

Let's talk about how Meshtastic uses encryption so we can better understand how keep our messages secure.

Meshtastic does use strong AES256 encryption to secure its channels, ensuring that messages sent within these channels remain private.

Each channel in has a unique key used for encryption. This key is used to encrypt messages sent within that channel, including direct messages between users on the same channel. The default LongFast channel has a publicly known key (AQ==). This means that anyone can join this default channel, and messages sent over this channel are not secure since the key is publicly available. For better security, it is recommended to create private channels with unique keys. These keys should be shared securely (using a secure communication method like Signal) with those you want to communicate with. This ensures that only intended participants can access the channel.

Direct messages in Meshtastic are not as secure if the initial contact was made on the default LongFast channel because the encryption key for DMs would be the same publicly known key. Therefore, it is better to use private channels with unique keys for more secure communications. Sharing the channel keys outside the mesh network and not through DMs on the default channel adds an extra layer of security.

---

#### Slide 25

![](http://hedgedoc.malin.onl/uploads/f6789f03-af3f-4a34-91ea-e2f6e618e649.jpg)

Next we will look at when you might use Meshtastic. Here are some practical examples showing how these technologies can be effectively utilized in various scenarios.

Rural Area Connectivity: LoRa/Meshtastic can provide reliable communication in rural areas where traditional infrastructure is lacking or nonexistent.

Outdoor Adventures: For hikers, campers, and kayakers, LoRa/Meshtastic offers a dependable way to stay in touch with your group in remote locations where cell service is unavailable, enhancing safety and coordination.

Disaster Response: During natural disasters or other emergency situations, when traditional communication networks fail or are overloaded with traffic, LoRa/Meshtastic can be used as an alternative communication network, ensuring that vital information is quickly relayed throughout the community.

---

#### Slide 26

![](http://hedgedoc.malin.onl/uploads/d11408bf-b22b-49d8-b81b-ee31d6fa0622.jpg)

That wraps up my content. I want to also shout out ‘The Comms Channel’ (TC2) on YouTube. He has some of the most informative and comprehensive Meshtastic content available. He’s working on some really cool Meshtastic related projects, like his new BBS server as well as various Solar node designs. So, if you're interested in building out your area with nodes, whether that be for solar, mobile, or a home base stations, check out his content. I’m sure you will find it helpful.

---

#### Slide 27

![](http://hedgedoc.malin.onl/uploads/a84ffb2c-63d1-4dc7-9b7a-b5688776332d.jpg)

Feel free to reach out to me on Nostr at thePR0M3TH3AN if you have any other questions that I don't cover today!

---

#### Slide 28

![](http://hedgedoc.malin.onl/uploads/6b7f071f-6549-4b49-828a-d7bee4c7603e.jpg)

Before we move into the Q&A segment, let’s recap the key takeaways from today’s workshop:

Meshtastic is open-source software that uses the LoRa mesh for decentralized, off-grid communication. It consists of a phone application and custom firmware on a LoRa radio devices, working together over Bluetooth.

Meshtastic uses strong encryption to ensure the confidentiality and security of your messages. Understanding how the channel keys work is crucial for maintaining that security.

For optimal mesh network performance, place nodes in locations with clear lines of sight. For more strategic placements, consider landscape topology and obstructions as well as the locations of other nodes in your area. This will enhances the networks reliability.

Meshtastic can be used for rural connectivity, emergency communication, and mobile mesh networks.

Now, I’d be happy to answer any questions you may have.

---

#### Slide 29

![](http://hedgedoc.malin.onl/uploads/c5cfceaa-5ea8-4bb3-b95f-244e9e673d80.jpg)

Here are some links to Meshtastic resources as well as a download link for this entire presentation. 

The large QR code is the Bitcoin Conference Private Channels. Scan to join in on the conversations.

Thanks for joining us for this Meshtastic workshop, I hope it was informative and enjoy the rest of the conference!