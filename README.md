Encrypted DNS Performance Evaluation under Adverse Network Conditions

This project evaluates the performance of encrypted DNS protocols under different network impairments from a client-side perspective. The study experimentally compares:

Traditional DNS
DNS-over-TLS (DoT)
DNS-over-HTTPS (DoH)

The objective is to analyze how encryption overhead and transport mechanisms affect DNS query latency under realistic adverse network conditions such as delay and packet loss.

Experimental Setup

Experiments were conducted on Ubuntu Linux in a virtual machine environment using:

kdig for DNS query execution
/usr/bin/time for latency measurement
tc netem for network emulation

The test dataset consists of the top 100 domains from the Tranco list.

For each domain, DNS queries were executed using DNS, DoT, and DoH protocols, and latency measurements were collected under multiple network scenarios.

Network Conditions Tested

The following network conditions were simulated:

Baseline network
Static delay (50 ms)
Static delay (100 ms)
Packet loss (1%)
Packet loss (5%)
Dynamic delay (20–150 ms variation)

A total of:

18 datasets
1800 latency measurements

were generated and analyzed.

Analysis Performed

The project includes Python scripts for:

Parsing latency measurements
Computing statistical metrics:
Mean latency
Median latency
Standard deviation
95th percentile
Generating visualization graphs:
Boxplots
CDF curves
Mean latency comparison charts
Generated Outputs

The analysis pipeline produces:

Per-condition boxplots
CDF latency distributions
Baseline combined CDF comparison
Mean latency comparison graphs
Statistical summary tables

All generated figures are suitable for research-style reports and presentations.

Technologies Used
Ubuntu Linux
Python
NumPy
Pandas
Matplotlib
tc netem
kdig
Research Focus

This project studies how encrypted DNS protocols behave under adverse network conditions and highlights the trade-offs between:

Security and privacy
Latency overhead
Protocol stability under network impairments

The work is intended as part of an MTech Computer Networks semester project.
