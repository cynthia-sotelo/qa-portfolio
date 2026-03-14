flowchart TD
A[Start Test] --&gt; B[Send GET request to /simple/price<br>ids=ethereum<br>vs_currencies=usd]
B --&gt; C{HTTP Status Code}
C --&gt;|200 OK| D[Validate Response Body]
D --&gt; E{Field ethereum.usd exists?}
E --&gt;|Yes| F[Validate Data Type: Float]
F --&gt; G[Validate Latency &lt; SLA threshold]
G --&gt; H[Test Passed]
E --&gt;|No| I[Test Failed - Missing Field]
C --&gt;|400 Bad Request| J[Invalid Parameter Handling]
J --&gt; K[Verify Error Structure<br>status + message]
K --&gt; L[Test Passed - Error handled]
C --&gt;|429 Too Many Requests| M[Rate Limit Triggered]
M --&gt; N[Validate Rate Limit Response<br>Retry-After header]
N --&gt; O[Test Passed - Rate limiting handled]
