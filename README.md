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
<img width="620" height="779" alt="image" src="https://github.com/user-attachments/assets/469346a3-e5e4-460d-8335-66e2677efe67" />

<h1>Step 8: </h1>
