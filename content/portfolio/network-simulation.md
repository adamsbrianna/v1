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



develop and lead a 3-day workshop for high school students on Networking and Security, most of them would have 0 programming experience and 0 knowledge of computer science, networking, or computer security. 



 the computer lab to get the students programming by having them implement a simple learning switch. We exposed an simple, declarative API that exposed some high-level functionality to mimic real networking APIs . 
Taking inspiration from Kim Bruce’s textbook Java: An Eventful Approach, we gave the students a graphical playground that they could fully manipluate. We had routers connected by blue lines, and you could send a packet (depicted by an envelope icon) by clicking first on the sender and then on the receiver.
 the students were able to finish the learning switch by the end of the hour we had alloted for the lab. 


In the final lab students played with (D)DoS attacks and mitigations, by giving them the ability to speed up Evil Routers, inspect the source of packets, drop incoming packets that have exceeded a certain threshold.

The idea here was to provide a bit of experience with the scientific method in computer science. First you come up with an attack model (DoS), then you defend against it (Queue Utilization Thresholds), then you measure the emergent properties of the defense (sometimes valid communications get dropped), so you update your model (Sender-Specific Thresholds), and look for more emergent properties. Then you try and see if your defense is robust to a more general attack model (e.g. DDoS/Spoofing), and come up with more sophisticated defense mechanisms, (e.g. Signing).

After having no experience with programming, networking,  our students were able to:

    Implement realistic networking programs with little-to-no prior programming experience
    Derive real-world consensus and discovery protocols by following their noses


From a Networking perspective, I think this really speaks to the need for better networking abstractions. Our 14-18 year olds (with no programming or CS experience) were able to synthesize and implement these simple, but realistic, policies in three days based on a few very high level primitives. I believe that this provides some weak evidence that operating complex networks doesn’t need to be as complicated as it currently is – we just need effective methods for abstracting away the details, interpreting what networks are doing, and predicting how they will behave.

