SDN Lab 

<h1>Step 1: Install mininet VM</h1>
<h2>sudo apt install mininet</h2>
<img width="265" height="61" alt="image" src="https://github.com/user-attachments/assets/5fdd154a-e862-4da0-bda2-8b05ede190de" />

<h1>Step 2: verify mininet is working</h1>
<h2>sudo mn --test pingall</h2>
<img width="258" height="274" alt="image" src="https://github.com/user-attachments/assets/c25dd079-f8ce-4424-8a15-cd541ad5e517" />

<h1>Step 3: launch default topology</h1>
<h2>sudo mn</h2>
<img width="134" height="130" alt="image" src="https://github.com/user-attachments/assets/b5289b1a-6ad7-42d7-8137-b9300ef6d611" />

<h1>Step 4: test connectivity</h1>
<h2>h1 ping h2</h2>
<img width="287" height="174" alt="image" src="https://github.com/user-attachments/assets/fd4516c6-eb23-4b4d-900c-8de9bf84cd7e" />

<h1>Step 5: creating custom topology</h1>
<h2>sudo mn --topo single,3</h2>
<img width="304" height="150" alt="image" src="https://github.com/user-attachments/assets/6a5e32bc-e6db-46bf-859e-dc6969cb7875" />

<h1>Step 6: measure bandwith</h1>
<h2>'h1 iperf -s &' and "h2 iperf -c h1"</h2>
<img width="285" height="108" alt="image" src="https://github.com/user-attachments/assets/f860dacb-a6a9-4aed-94ed-44d9233b1e2e" />

<h1>Step 7: programming the SDN controller with Ryu</h1>
<h2>sudo apt install python3-ryu and verify installation with ryu-manager --version</h2>
we had to use sudo apt install -y python3-ryu since the original sudo apt install python3-ryu command was throwing 404 errors when prompted if we'd like to continue the install. Once command was updated we were able to run ryu-manager --version properly 
<img width="620" height="779" alt="image" src="https://github.com/user-attachments/assets/469346a3-e5e4-460d-8335-66e2677efe67" />

<h1>Step 8: Connect mininet to controller</h1>
<h2>sudo mn --controller=remote,ip=127.0.0.1,port=6653 --topo single,3</h2>
<img width="417" height="135" alt="image" src="https://github.com/user-attachments/assets/a8ecfc70-7619-48fa-952d-410959156e37" />

<h1>Step 9: Create custom ryu app that impliments a simple learning switch controller<h1>
<h2>Opened a nano file and added these import modules: from ryu.base import app_manager, from ryu.controller import ofp_event, from ryu.controller.handler import MAIN_DISPATCHER,set_ev_cls, from ryu.ofproto import ofproto_v1_3, from ryu.lib.packet import packet, ethernet</h2>
<img width="264" height="74" alt="image" src="https://github.com/user-attachments/assets/e4104f89-70f3-4994-b7d6-e3a46dcd5117" />

<h1>Step 10: observe flow tables</h1>
<h2>use: sh ovs-ofctl dump-flows s1</h2>

<h1>Step 11: Impliment traffic blocking policy</h1>
<h2>sh ovs-ofctl -O OpenFlow13 add-flow s1 "priority=100,ip,nw_src=10.0.0.1,nw_dst=10.0.0.3,actions=drop" than run sh ovs-ofctl -O OpenFlow13 dump-flows s1</h2>
<img width="461" height="423" alt="image" src="https://github.com/user-attachments/assets/22f9e767-8121-40ab-b009-e45eca4c0c4d" />
<img width="214" height="426" alt="image" src="https://github.com/user-attachments/assets/08d38636-a4b9-413a-b991-5c286469df95" />

<h1>Verify traffic between h1 and h3 have been blocked</h1>
<h2>h1 ping h2</h2>


<h1>Verify h2 and h3 can still communicate between eachother</h1>
<h2>h2 ping h3</h2>
<img width="489" height="570" alt="image" src="https://github.com/user-attachments/assets/b00d0cc4-eda9-451b-b312-7ccde54a15a9" />
<img width="445" height="425" alt="image" src="https://github.com/user-attachments/assets/6f7576e2-8607-4349-80eb-e3e67f4ac79f" />
<img width="334" height="61" alt="image" src="https://github.com/user-attachments/assets/9252644b-9307-4382-96c7-ec6c9b58f02b" />
<img width="337" height="61" alt="image" src="https://github.com/user-attachments/assets/9dd671a0-4cdb-4cff-9c44-0675e3a5f033" />









