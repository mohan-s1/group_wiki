To date (January 5, 2026), UVA has two supercomputing clusters, `Rivanna` and `Afton` with Afton being the newer one. A cluster is merely a group of machines where every `node` can be thought of as an inidvidual computer. Within each node, there are multiple cores akin to a laptop (node) having multiple cores. Rivanna nodes have only 40 cores while Afton nodes go up to 96 cores.

# Accessing the Cluster

There are three ways to access the supercomputing cluster: [https://www.rc.virginia.edu/userinfo/hpc/login/](https://www.rc.virginia.edu/userinfo/hpc/login/)

1. [FastX](https://fastx.hpc.virginia.edu) is a completely virtual desktop.
2. [Open OnDemand](https://ood.hpc.virginia.edu/pun/sys/dashboard) which is beteween a completely virtual desktop (i.e. FastX) and an all-terminal approach (i.e. ssh).
3. `ssh` which is the "secure shell" (a shell meaning way to access the terminal). If you are using MacOS or Linux, you can `ssh` into the cluster by typing `ssh -Y computing_id@login.hpc.virginia.edu` into your terminal. If on a Windows machine, RC recommends installing MobaXTerm.

# Notes on Using the Cluster

## File Structure

Everyone that can access the UVA cluster (controlled by having a PI with access) will have at least two "spaces" they can use:

1. `/home/computing_id` which offers permanent but small (20 GB) storage. It is recommended you use this directory to house essential files.

2. `/scratch/computing_id` has temporary (90 days) and large (10 TB = 10000 GB) storage. It is recommended you use this directory to run jobs in and move essential files elsewhere upon completion.

There is a third space we can use, referred to as "project space"

3. `/project/paolucci` is a shared space on the cluster for all members of the Paolucci group. It has 10 TB of permanent storage, but it costs money so be courteous when storing files here. Feel free to make a directory like `/project/paolucci/your_name` for you to use.

## Job Submission

When you log onto the cluster -- whether it be through FastX, Open OnDemand, or ssh -- you are on what is called a "login node." The login node is only meant for you to navigate around the cluster. When it comes time to run jobs, you will submit a `slurm` script for the job at hand. Throughout the subdirectories here, there will be slurm scripts provided. Please ask questions about any and every aspect of them as you need/want.

The reason not to submit jobs on login nodes is that it will slow things down for everyone. The analogy is asking a waiter to cook: if the waiter has to take orders and cook the meals, it will be very difficult for everyone else to place their orders. Moreover, the waiter probably hasn't trained to cook, so the food will be slowly (and likely improperly) prepared. In this analogy, the waiter is a login node while a slurm script is an order to goes to a chef (a `compute node`) that can appropriately handle the request.

# UVA RC Services
The UVA Research Computing (RC) staff are generally great, and there are a couple things they do of note.

* The most important one is they [answer support tickets](https://www.rc.virginia.edu/form/support-request/). You can submit a ticket to receive help with the caveat that the issue may be outside of what they can or have to assist you with.
  * Note. If you are not on Grounds, you must use a VPN to access the ticket submission page. If the link above does not work, use [this one](https://www.rc.virginia.edu/support/) and choose `Open a Support Ticket`.

* The UVA RC staff hold office hours where you can go an directly ask questions to the staff: scroll down [here](https://www.rc.virginia.edu/support/) to the `Office Hours` section.

* The UVA RC staff hold workhops including a weekly Intro to HPC session: [https://www.rc.virginia.edu/education/workshops/](https://www.rc.virginia.edu/education/workshops/)
