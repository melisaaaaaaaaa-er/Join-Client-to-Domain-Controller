# Join Client to Domain Controller

<h3>Change Client-1's DNS settings</h3>

<img src="https://raw.githubusercontent.com/melisaaaaaaaaa-er/ADDS-images/main/2.png"/>

<img src="https://raw.githubusercontent.com/melisaaaaaaaaa-er/ADDS-images/main/33.png"/>

On the Azure Portal, change Client-1’s DNS settings so they redirect to DC-1’s private IP address. 

Client-1 → Network Settings → -network interface- → DNS servers → Custom → input DC-1’s private IP address → Save

This will make it so Client-1 uses DC-1 as its DNS server.

#
<img src="https://raw.githubusercontent.com/melisaaaaaaaaa-er/ADDS-images/main/34.png"/>

Restart Client-1

#
<h3>Make the join</h3>

<img src="https://raw.githubusercontent.com/melisaaaaaaaaa-er/ADDS-images/main/35.png"/>

Login to Client-1 with the local administrator account.

Go to System → About → “Rename this PC (advanced) → Change → Domain (input the domain you want to connect the machine to) → OK

You will be prompted for admin credentials with authority to make the join happen.

#
<img src="https://raw.githubusercontent.com/melisaaaaaaaaa-er/ADDS-images/main/36.png"/>

Client-1 is now a part of mydomain.local.

<img src="https://raw.githubusercontent.com/melisaaaaaaaaa-er/ADDS-images/main/37.png"/>

You will be prompted to restart the machine to apply the changes.

#
<img src="https://raw.githubusercontent.com/melisaaaaaaaaa-er/ADDS-images/main/38.png"/>

Check DC-1’s ADUC to ensure the join has been made.

“Client-1” should be under Computers within mydomain.local.
