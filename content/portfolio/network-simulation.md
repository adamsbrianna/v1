+++
showonlyimage = false
draft = false
image = "img/portfolio/packet-switching.png"
date = "2021-11-05T18:25:22+05:30"
title = "Network Simulation"
weight = 0
+++

Teaching DoS attacks, DDos attacks, simple DoS mitigation, and spoofing.
<!--more-->


{{< rawhtml >}} 

<video controls width=100%>
    <source src="/videos/simulation1.mp4"
            type="video/mp4">
    Sorry, your browser doesn't support embedded videos.
</video>

{{< /rawhtml >}}

{{< rawhtml >}} 
<p> &nbsp; </p>
{{< /rawhtml >}}

[comment]: <> (Simulation of x attack above and x attack below.)

{{< rawhtml >}} 
<p> &nbsp; </p>
{{< /rawhtml >}}

{{< rawhtml >}} 

<video controls width=100%>
    <source src="/videos/simulation2.mp4"
            type="video/mp4">
    Sorry, your browser doesn't support embedded videos.
</video>

{{< /rawhtml >}}

{{< rawhtml >}} 
<p> &nbsp; </p>
{{< /rawhtml >}}

Along with two grad students (Eric Campbell and Jonathan DiLorenzo) from Nate Foster's lab, this simulation was designed for a 3-day workshop for high school students on networking and security. These students had minimal knowledge of computer science and networking. To get the students programming, the computer labs we designed had them implement a simple learning switch. We provided a simple API that exposed some high-level functionality to mimic real networking APIs, and gave the students a graphical playground that they could fully manipluate. We had routers connected by blue lines, and you could send a packet (depicted by an envelope icon) by clicking first on the sender and then on the receiver. All of the students were able to finish the learning switch by the time we had alloted for the lab. 

In the final lab students played with (D)DoS attacks with the ability to speed up specific, "Evil" Routers, inspect the source of packets, and drop incoming packets that exceeded a certain threshold. The idea here was to provide a bit of experience with the scientific method in computer science. First you come up with an attack model (DoS), then you defend against it (Queue Utilization Thresholds), then you measure the emergent properties of the defense (sometimes valid communications get dropped), so you update your model (Sender-Specific Thresholds), and look for more emergent properties. Then you try and see if your defense is robust to a more general attack model (e.g. DDoS/Spoofing), and come up with more sophisticated defense mechanisms, (e.g. Signing).

By the end of the program, the students were able to implement realistic networking programs and derive real-world discovery protocols.