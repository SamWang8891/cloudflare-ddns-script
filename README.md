# cloudflare-ddns-script

### The script to update Cloudflare DNS record

## Introduction

This script updates the DNS A record to Cloudflare. This means that you'll get a DDNS-like function by using this script. All Linux/UNIX based machine are able to run this. If you want to run it reguallary, cronjob is your friend.

## Usage

1. **Install neede package.**
   The needed package are "curl" "jq" and "git".

   1. For Debian/GNU and Ubuntu based
      `sudo apt install -y curl jq git`
   2. For others, please figure out yourself as I'm not familiar with all OS
2. **Make sure to create the DNS A record you want the script to update first**
3. **Clone the repository**
   Change directory as your desire then`git clone https://github.com/SamWang8891/cloudflare-ddns-script.git`, then `cd cloudflare-ddns-script`
4. **Modify the config.sh file**
5. **(Optional) Add execute permission to update-dns.sh file**

   `chmod +x update-dns.sh`
6. **Run the script**

   `./update-dns.sh`  OR  `bash update-dns.sh`
7. If there's error, check ur config.sh again.
8. (Optional) Add to cronjob.

   ``cronjob -e``
