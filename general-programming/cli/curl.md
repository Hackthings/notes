# curl

It's most powerful, I think, because it allows a developer to test an API or endpoint while SSH'd into any server. 

I wanted to get the fastest possible response times from Microsoft Spell-Check \(cognitive\) API. So, I spawned a bunch of servers all over the USA + Canada. It turns out that Microsoft does not do geo-routing. They only served from one location - in NYC. That's it. So, I decided to host my server there. Works well. Unfortunately, when I upgrade my API architecture to include geo-routing, all locations except for NYC will have bad latency, of up to 0.5 added seconds! To be fair to Microsoft, their spell-check API is the best publicly available. Just their infrastructure is lacking. But maybe geo-routing is not as common in enterprise as I expected. Anyway, you can find out by using curl.

{% embed url="https://stackoverflow.com/questions/18215389/how-do-i-measure-request-and-response-times-at-once-using-curl" caption="\(and other good tips\)" %}



