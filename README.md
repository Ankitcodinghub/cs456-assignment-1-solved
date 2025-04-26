# cs456-assignment-1-solved
**TO GET THIS SOLUTION VISIT:** [CS456 Assignment 1 Solved](https://www.ankitcodinghub.com/product/cs456-assignment-1-solved/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;126800&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;3&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;5&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;5\/5 - (3 votes)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;CS456  Assignment 1 Solved&quot;,&quot;width&quot;:&quot;138&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 138px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            5/5 - (3 votes)    </div>
    </div>
&nbsp;

1 Assignment ObjecOve

The goal of this assignment is to gain experience with both TCP and UDP socket programming in a client-server environment (Figure 1). You will use Python or any other programming language to design and implement a client program (client) and a server program (server) to communicate between themselves.

2 Assignment SpecificaOons

2.1 Summary

In this assignment, the client will send requests to the server to reverse strings (taken as a command line input) over the network using sockets.

This assignment uses a two-stage communicaOon process. In the negoOaOon stage, the client and the server negoOate on a random port (&lt;r_port&gt;) for later use through a fixed negoOaOon port (&lt;n_port&gt;) of the server. Later in the transacOon stage, the client connects to the server through the selected random port for actual data transfer.

2.2 Signaling

The signaling in this project is done in two stages as shown in Figure 2.

Stage 1. Nego+a+on using TCP sockets: In this stage, the client creates a TCP connecOon with the server using &lt;server_address&gt; as the server address and &lt;n_port&gt; as the negoOaOon port on the server (where the server is listening). The client sends a request to get the random port number from the server where it will send the actual request (i.e., the string to be reversed). To iniOate this negoOaOon, the client sends a request code (&lt;req_code&gt;), an integer (e.g., 13), a]er creaOng the TCP connecOon. If the client fails to send the intended &lt;req_code&gt;, the server closes the TCP connecOon and conOnues listening on &lt;n_port&gt; for subsequent client requests. Once the server verifies the &lt;req_code&gt;, it replies back with a random port number &lt;r_port&gt; where it will be listening for the actual request. A]er receiving this &lt;r_port&gt;, the client closes the TCP connecOon with the server.

Stage 2. Transac+on using UDP sockets: In this stage, the client creates a UDP socket to the server in &lt;r_port&gt; and sends the &lt;msg&gt; containing a string. On the other side, the server receives the string and sends the reversed string back to the client. Once received, the client prints out the reversed string and exits. Note that the server should conOnue listening on its &lt;n_port&gt; for subsequent client requests. For simplicity, we assume, there will be only one client in the system at a Ome. So, the server does not need to handle simultaneous client connecOons.

2.3 Client Program (client)

You should implement a client program, named client. It will take four command line inputs:

&lt;server_address&gt;, &lt;n_port&gt;, &lt;req_code&gt;, and &lt;msg&gt; in the given order.

2.4 Server Program (server)

You should also implement a server program, named server. The server will take &lt;req_code&gt; as a command line parameter. The server must print out the &lt;n_port&gt; value in the following format as the first line in the stdout:

SERVER_PORT=&lt;n_port&gt;

For example, if the negoOaOon port of the server is 52500, then the server should print: SERVER_PORT=52500

2.5 Example ExecuOon

Two shell scripts named server.sh and client.sh are provided. Modify them according to your choice of programming language. You should execute these shell scripts which will then call your client and server programs.

• Run server: ./server.sh &lt;req_code&gt;

• Run client: ./client.sh &lt;server address&gt; &lt;n_port&gt; &lt;req_code&gt; ‘A man, a plan, a canal— Panama!’

3 Hints

Below are some points to remember while coding/debugging to avoid trivial problems.

• You can use and adapt the sample codes of TCP/UDP socket programming in Python slides (last few slides Chapter 2).

• Use port id greater than 1024, since ports 0-1023 are already reserved for different purposes (e.g., HTTP @ 80, SMTP @ 25)

• If there are problems establishing connecOons, check whether any of the computers running the server and the client is behind a firewall or not. If yes, allow your programs to communicate by configuring your firewall so]ware.

• Make sure that the server is running before you run the client.

• Also remember to print the &lt;n_port&gt; where the server will be listening and make sure that the client is trying to connect to that same port for negoOaOon.

• If both the server and the client are running in the same system, 127.0.0.1 or localhost can be used as the desOnaOon host address.

• You can use help on network programming from any book or from the Internet, if you properly refer to the source in your programs. But remember, you cannot share your program or work with any other student.

4 Procedures

4.2 Hand in InstrucOons

Submit all your files in a single compressed file (.zip, .tar etc.) using LEARN in dedicated Dropbox. The filename should include your username and/or student ID. You must hand in the following files / documents:

• Source code files.

• Makefile: your code must compile and link cleanly by typing “make” or “gmake” (when applicable).

• README file: this file must contain instrucOons on how to run your program, which undergrad machines your program was built and tested on, and what version of make and compilers you are using.

• Modified server.sh and client.sh scripts.

Your implementaOon will be tested on the machines available in the undergrad environment linux.student.cs which includes the following hosts:

4.3 DocumentaOon

4.4 EvaluaOon

Work on this assignment is to be completed individually.

5 AddiOonal Notes:

• You have to ensure that both &lt;n_port&gt; and &lt;r_port&gt; are available. Just selecOng a random port does not ensure that the port is not being used by another program.

• All codes must be tested in the linux.student.cs environment prior to submission.

• Run client and server in two different student.cs machines

• Run both client and server in a single student.cs machine

• Make sure that no addiOonal (manual) input is required to run any of the server or client.
