Note:
Client usage
1.	First edit the BondsProClient.cfg to input the below configuration, which will be provided by the exchange.
a)	SocketConnectHost
b)	SocketConnectPort
c)	BeginString
d)	SenderCompID
e)	TargetCompID
2.	Run the "run_BondsProClient.bat", a dos application will prompt up, it will connect and log into the server according to the above configuration, then it will read and parse the "MarketDataIncrementalRefresh(X)" messages sent from the server, the market depth of all bonds will be recorded in the memory.
3.	The user can press "1" to write the market depth of all bonds into a file "bonds.com.snapshot.txt" file under the user's home folder, press "2" to quit the application.

I also had implemented a C++ server which will keep sending out the fake "MarketDataIncrementalRefresh(X)" messages periodically (send one out every 3 seconds) to all it's connected sessions. You can run the the server application by "run_bondsProServer.bat" first, then run the client application, you will be able to see how the FIX messages communicate between the two applications.

