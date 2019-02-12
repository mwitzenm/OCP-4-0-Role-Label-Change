# OCP-4-0-Role-Label-Change
Can we change the role or label of a node to change its purpose? Can I just change a worker node to an infranode? (4)

---
How does it differ between OCP 3 and OCP 4?
---
The ability to change the labels is trivial but I would suggest that editing a resource such as an existing machineset that was create by default should be avoided.  Just becasue you can do it does not mean you want too.  The basic primatives in how and why to create a machineset is well documented in `https://github.com/openshift/training/blob/master/docs/05-infrastructure-nodes.md` how to add a machineset and modify the appropriate labels that will then create a series of nodes to the labels to be applied and thus workloads to be applied to those nodes via the label.

---
Which ones are on private subnets? Which ones are on public subnets and security groups?
---
Private subnets are used by default and are part of the larger subnet carved up via security groups.


---
Do I need to create
---

* operators - *no* you need to create a machine set
* additional security groups to create routers? - Not required a per the way the ELB is deployed with a Custom Resource so K8s handles the commmunication / configuration
* Based on what security policies? - No security policies needed or need to be modified

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
