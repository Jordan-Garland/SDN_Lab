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

<h1>creating custom topology</h1>
<h2>sudo mn --topo single,3</h2>
