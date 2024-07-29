# DNS
DNS Records and Local Cache Lab: A, CNAME, and Local DNS Cache

A-Record Exercise
Connect/log into DC-1 as your domain admin account (mydomain.com\jane_admin)
Connect/log into Client-1 as an admin (mydomain\jane_admin)
From Client-1 try to ping “mainframe” notice that it fails

<img width="993" alt="Screenshot 2024-07-28 at 11 27 33 PM" src="https://github.com/user-attachments/assets/6d244b58-b858-4fc3-97d1-b242c22fc650">

Nslookup “mainframe” notice that it fails (no DNS record)
Create a DNS A-record on DC-1 for “mainframe” and have it point to DC-1’s Private IP address
Go back to Client-1 and try to ping it. Observe that it works

Local DNS Cache Exercise
Go back to DC-1 and change mainframe’s record address to 8.8.8.8
Go back to Client-1 and ping “mainframe” again. Observe that it still pings the old address
Observe the local dns cache (ipconfig /displaydns)
Flush the DNS cache (ipconfig /flushdns). Observe that the cache is empty
Attempt to ping “mainframe” again. Observe the address of the new record is showing up

<img width="521" alt="Screenshot 2024-07-29 at 12 02 16 AM" src="https://github.com/user-attachments/assets/570ebc05-3917-447d-bbaa-decb826edab2">

CNAME Record Exercise
Go back to DC-1 and create a CNAME record that points the host “search” to “www.google.com”
Go back to Client-1 and attempt to ping “search”, observe the results of the CNAME record
On Client-1, nslookup “search”, observe the results of the CNAME record

<img width="789" alt="Screenshot 2024-07-29 at 12 07 38 AM" src="https://github.com/user-attachments/assets/1718091c-54f7-4690-870a-2b45025371a0">

<img width="625" alt="Screenshot 2024-07-28 at 11 44 49 PM" src="https://github.com/user-attachments/assets/b3543a03-3e02-4b3d-bcf9-5559edcf790b">

Root hints, are the starting points in this system. They are a list of servers, known as root servers, that your computer contacts first to begin the
process of finding the exact location of a website. These root servers then direct your computer to more specific servers until it finds the exact 
address of the website you're looking for.

<img width="426" alt="Screenshot 2024-07-28 at 11 50 24 PM" src="https://github.com/user-attachments/assets/f28c7a98-a4b0-46dc-9a73-5cf72c821637">





