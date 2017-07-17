![logo](/polycircle.png?raw=true "Optional Title")
##### Circle-based Edge Network #####
 
Decentralized apps & CDN with signaling for webbt from any improvised storage. Should mitigate or obsolesce hosting & cloud infrastructure requirements entirely for the bravest users.

*Is it truly serverless?* Well, its more like bootstraping metadata for a P2P-based global delivery cluster. 
Among the cluster will also be our seeding supernodes where network metadata is shared with clients. 

##### Registration #####
Each new account is mapped to <br>
&lt; app | user &gt;.polycircle.net.
<br>Use your own signaling domain as circle instance on polycircle.net via manual CNAME map.

##### Requirements & Flow #####

Requires<br>
1. Registering your circle app namespace ("CAN") and optionally map your (sub)domain as a CNAME.<br>
2. Manually inserting signal.js to your site's index file if mapped as a CNAME.<br>

Flow<br>
1. Client requests signaling script -> <br>&lt;script src=http://polycircle.net/signal?api_key&gt;<br>
2. Script accesses signaling data through arbitrary browser-based storage api<br>
3. Data is gz web component package of js, html, and css.<br>
4. Content referenced in gz retrieved from LLS or IDBWrapper injection.<br>

Component contents: <br>
1. circles.js:  list of circles<br>
2. signal.js:  signal web component bootstrap<br>

Signal web component defines & performs:<br>
1. CID - Circleid is 64bit OTP( CAN )<br>
2. SIG - Signalid is 256bit OTP( REMOTE_ADDR + CID )<br>
3. MID - Mediaid is 16bit OTP( SIG + path ), path is media file or folder<br>
4. CAN - Namespace module loading per circleid<br>
5. URL circle resolver - Get circleid signals roster<br>
6. Circle mirror - Route circle content to client response<br>
(entropyd seeds one-time pad (OTP))
##### Peering Tools #####
- Polymer
- RTMFP + WebBT 
- Webtorrent.io - torrent CDN
- NSQ - Distributed message queue 
- LargeLocalStorage

##### Core Signaling Providers #####
- Openshift
- Bluemix
- Backand
- Peerserver Cloud
