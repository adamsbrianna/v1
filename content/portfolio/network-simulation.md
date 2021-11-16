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

Simulation of x attack above and x attack below.

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

Along with two grad students (Eric Campbell and Jonathan DiLorenzo) from Nate Foster's lab, this simulation was designed for a 3-day workshop for high school students on Networking and Security. These students had no to minimal knowledge of computer science, networking, or computer security. To get the students programming the computer labs had them implement a simple learning switch. We exposed an simple, declarative API that exposed some high-level functionality to mimic real networking APIs. We gave the students a graphical playground that they could fully manipluate. We had routers connected by blue lines, and you could send a packet (depicted by an envelope icon) by clicking first on the sender and then on the receiver.
the students were able to finish the learning switch by the end of the hour we had alloted for the lab. 
{{< rawhtml >}} 
<p> &nbsp; </p>
{{< /rawhtml >}}
In the final lab students played with (D)DoS attacks and mitigations, by giving them the ability to speed up Evil Routers, inspect the source of packets, drop incoming packets that have exceeded a certain threshold. The idea here was to provide a bit of experience with the scientific method in computer science. First you come up with an attack model (DoS), then you defend against it (Queue Utilization Thresholds), then you measure the emergent properties of the defense (sometimes valid communications get dropped), so you update your model (Sender-Specific Thresholds), and look for more emergent properties. Then you try and see if your defense is robust to a more general attack model (e.g. DDoS/Spoofing), and come up with more sophisticated defense mechanisms, (e.g. Signing).
{{< rawhtml >}} 
<p> &nbsp; </p>
{{< /rawhtml >}}
By the end of the program, students were able to implement realistic networking programs and derive real-world discovery protocols.