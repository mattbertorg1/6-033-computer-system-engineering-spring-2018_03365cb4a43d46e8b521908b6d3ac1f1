---
course_id: 6-033-computer-system-engineering-spring-2018
layout: course_section
menu:
  leftnav:
    identifier: 72f0d675cb14ba194c5d7a81051af829
    name: DCTCP Assignment
    parent: 0abfab7fcd019a6a159d1afa3fd61f99
    weight: 340
parent_title: 'Week 7: Networking Part III'
title: DCTCP Assignment
type: course
uid: 72f0d675cb14ba194c5d7a81051af829

---

*   Read ![This resource may not render correctly in a screen reader.](/images/inacessible.gif)"[Data Center TCP (DCTCP) (PDF - 2.98MB)](https://people.csail.mit.edu/alizadeh/papers/dctcp-sigcomm10.pdf)" by Mohammad Alizadeh, Albert Greenberg, et al.
*   Skip section 3.3 except for the final paragraph, which gives an estimate for the parameter _K_.
*   Skim section 4 (Results)
*   Closely observe figures 15 and 19, which show the queue occupancy as a function of time, and number of sources.

DCTCP customizes the TCP congestion control algorithm for datacenters. It leverages the Explicit Congestion Notification (ECN) to obtain an early congestion feedback from routers/switches, before the queue drops packets. Further, DCTCP provides a smooth reaction to congestion, i.e., when congestion is limited, it reduces its congestion window by a small amount. In contrast, when congestion is severe, it reduces its congestion window by a large amount.

To help you as you read:

*   Section 1 introduces the paper. Section 2 describes communication in datacenter networks. After this section, you should understand how datacenter traffic differs from "normal" Internet traffic.
*   Section 3 describes the DCTCP algorithm. After this section, you should understand how DCTCP compares to TCP. Does it react sooner or later to congestion than TCP does? What does a DCTCP sender do when it infers that there is congestion on the network as compared to a TCP center? What are queues in a datacenter running DCTCP like (empty? full? etc.)?
*   Section 4—which you should skim—gives the results of the authors' experiments. Check that the empirical results match your expectations.

As you read, think about:

*   Would DCTCP work on the Internet?
*   Is there a trade-off between the generality of a protocol and its performance?

Questions for Recitation
------------------------

**Before you come to this recitation**, write up (on paper) a _brief_ answer to the following (really—we don't need more than a couple sentences for each question). 

Your answers to these questions should be **in your own words**, not direct quotations from the paper.

*   What is the goal of DCTCP?
*   How does DCTCP differ from TCP?
*   Why does DCTCP differ from TCP?

As always, there are multiple correct answers for each of these questions.