# 🚀 Subdomain Enumeration Cheat Sheet  
### *By IndiHackers*

---

## 🧠 Why Subdomain Enumeration Matters

Subdomains are often **forgotten entry points**.

Hackers don’t attack the main website…  
They target:
- Dev environments  
- Staging servers  
- Old APIs  
- Misconfigured assets  

👉 This is where real vulnerabilities live.

---

## ⚔️ Types of Subdomain Recon

### 1. Passive Recon
- No direct interaction with target  
- Safe & stealthy  
- Uses public data sources  

### 2. Active Recon
- Direct probing (DNS brute-force)  
- More results, but detectable  

---

## 🛠️ Top Subdomain Enumeration Tools

| Tool | Type | Best For | Command |
|------|------|----------|---------|
| **Subfinder** | Passive | Fast & clean recon | `subfinder -d domain.com -all -silent` |
| **Amass** | Passive + Active | Deep attack surface mapping | `amass enum -passive -d domain.com` |
| **Sublist3r** | Passive | Beginner-friendly tool | `python3 sublist3r.py -d domain.com` |
| **Chaos** | Passive | Bug bounty datasets | `chaos -d domain.com -silent` |
| **Assetfinder** | Passive | Quick subdomain discovery | `assetfinder --subs-only domain.com` |
| **GAU** | Passive | URL + historical data | `gau --subs domain.com` |
| **GitHub Subdomains** | Passive | Finds leaks on GitHub | `github-subdomains -d domain.com` |
| **Findomain** | Passive | Fast + automation features | `findomain -t domain.com` |
| **OneForAll** | Passive | All-in-one enumeration | `python3 oneforall.py --target domain.com run` |
| **PureDNS** | Active | Bruteforce + filtering | `puredns bruteforce wordlist.txt domain.com` |
| **Gobuster** | Active | DNS brute-force | `gobuster dns -d domain.com -w wordlist.txt` |
| **ShuffleDNS** | Active | Mass brute-force + resolving | `shuffledns -d domain.com -w wordlist.txt -r resolvers.txt` |

---

## 🔥 Beginner Recon Workflow

Follow this exact flow 👇

### 1️⃣ Passive Enumeration
- Subfinder  
- Assetfinder  
- Amass  

### 2️⃣ Combine Results
```bash
cat *.txt | sort -u > final.txt
```

### 3️⃣ Active Bruteforce
- ShuffleDNS  
- GoBuster

### 4️⃣ Validate Live Subdomains
```bash
httpx -l final.txt
```


Visit https://indihackers.in/courses/full-ethical-hacking and checkout our course!!!
