# Join Client to Domain Controller

<h3>Change Client-1's DNS settings</h3>

![2](https://github.com/melisa-er/Join-Client-to-Domain-Controller/assets/157723219/cc835ad4-9d71-41e5-a178-f8ab594a4a29)

![33](https://github.com/melisa-er/Join-Client-to-Domain-Controller/assets/157723219/1d41c0df-812b-446d-ab15-356e67394bc2)

On the Azure Portal, change Client-1’s DNS settings so they redirect to DC-1’s private IP address. 

Client-1 → Network Settings → -network interface- → DNS servers → Custom → input DC-1’s private IP address → Save

This will make it so Client-1 uses DC-1 as its DNS server.

#
![34](https://github.com/melisa-er/Join-Client-to-Domain-Controller/assets/157723219/baa35f8f-73d4-4e34-816a-68f0e49417cb)

Restart Client-1

#
<h3>Make the join</h3>

![35](https://github.com/melisa-er/Join-Client-to-Domain-Controller/assets/157723219/5c3a59cd-0bb1-4591-bb61-fd1c04b2e179)

Login to Client-1 with the local administrator account.

Go to System → About → “Rename this PC (advanced) → Change → Domain (input the domain you want to connect the machine to) → OK

You will be prompted for admin credentials with authority to make the join happen.

#
![36](https://github.com/melisa-er/Join-Client-to-Domain-Controller/assets/157723219/c5017e4c-b9ff-4b93-88da-f9858aad3130)

Client-1 is now a part of mydomain.local.

![37](https://github.com/melisa-er/Join-Client-to-Domain-Controller/assets/157723219/4de6fe06-353d-4844-80f4-964ef3547555)

You will be prompted to restart the machine to apply the changes.

#
![38](https://github.com/melisa-er/Join-Client-to-Domain-Controller/assets/157723219/6d230222-03fd-4678-bd4d-12f7149f9d61)

Check DC-1’s ADUC to ensure the join has been made.

“Client-1” should be under Computers within mydomain.local.
