# OCP-4-0-Role-Label-Change
Can we change the role or label of a node to change its purpose? Can I just change a worker node to an infranode? (4)

---
How does it differ between OCP 3 and OCP 4?
--

---
Which ones are on private subnets? 
---

---
Which ones are on public subnets and security groups?
---

---
Do I need to create
---

* operators
* additional security groups to create routers? 
* Based on what security policies?

---
Can I implement different routes in 4?
---

* note:  teach separation of public and private subnets?

Raf: all machines in same subnet.

Eng: Everything defaults to private subnets. NAT gateways for egress and routers are the only things on public networks.

* Note: DO NOT TOUCH your VPC. Changes are not supported.

---
Can we setup VPC peering?
---

---
Do we want Security groups operators later?
---

---
VPN in cluster to database -> Egress IP and internal service -> database
---
