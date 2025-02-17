# cloudflare-ddns-script

### The script to update Cloudflare DNS record

## Introduction

This script updates the DNS A record to Cloudflare. This means that you'll get a DDNS-like function by using this script.

## Usage

### 1. Install the needed packages.

The needed package are "curl", "jq" and "git". 
- For Debian/GNU and Ubuntu-based:
```bash
sudo apt install -y curl jq git
```
- For others, please figure out yourself as I'm not familiar with all OS

<br />

### 2. Create DNS record
Create a DNS A record you want the script to update in the Cloudflare web dashboard.

<br />

### 3. Clone the repository
   Change the directory to your desired location then
```bash
git clone https://github.com/SamWang8891/cloudflare-ddns-script.git && \
cd cloudflare-ddns-script
```

<br />

### 4. Modify the config.sh file
Inset the needed information to the config.sh file.

<br />

### 7. Add execute permission to update-dns.sh file.
```bash
chmod +x update-dns.sh
```

<br />

### 8. Run the script

```bash
./update-dns.sh
```

<br />


### 9. (Optional) Add to cronjob.

   Run `cronjob -e` and add `* * * * * bash /path/to/update-dns.sh` to the file. Change the time as desired.
