# Royal SRC Tutorial ⬇️

Thank you for choosing Royal SRC; you won't regret it! 👑

**Current Royal SRC version**: `1.8.7.2`

Setup video tutorial: https://discord.com/channels/1358053746420219995/1358060457138852020

---

# Suggested minimum server specifications:

**Operating System**: `Ubuntu 22.04` or `Ubuntu 24.04`
**RAM**: `1 GB`
**CPU**: `1 Core` @ `1 GHz`
**Storage**: `5 GB` recommended

---

## Check this for any support:
- https://discord.com/channels/1358053746420219995/1358060457138852020
- https://discord.com/channels/1358053746420219995/1358060485089562729
- https://royalprojets.com

---

*Step #1*
# Download Royal SRC files to your server in the `/root/` directory

*Step #2*
# Configure the configuration files:
	Open `assets/config/config.json` and replace line 4 with your Royal SRC license key.
	Check the rest of `assets/config/config.json` for custom settings.
	Open `assets/attacks/attacks.json` and update relevant lines.
	Open `assets/config/presets.json` and replace your presets as needed.
	Open `assets/config/bots.json` and configure your bots (Discord & Telegram) - ROYAL SRC AIO EXCLUSIVE!!
	Open `assets/config/funnel.json` and link your APIS/SERVER/BOTS - ROYAL SRC AIO EXCLUSIVE!!

*Step #3*
# Run the following 3 commands (DISABLE IPV6):

```bash
sudo sysctl -w net.ipv6.conf.all.disable_ipv6=1
sudo sysctl -w net.ipv6.conf.default.disable_ipv6=1
sudo sysctl -w net.ipv6.conf.lo.disable_ipv6=1
```

## What it should look like: Commands execute without error

*Step #4*
# Update the server:
```bash
sudo apt-get update -y && sudo apt-get upgrade -y
```

## What it should look like: System updates successfully

*Step #5*
# Install required dependencies:
```bash
sudo apt-get install gnupg
```

## What it should look like: gnupg installs correctly

*Step #6*
# Install MongoDB - Add key and repository:
```bash
curl -fsSL https://www.mongodb.org/static/pgp/server-4.4.asc | sudo apt-key add -
apt-key list
echo "deb [ arch=amd64,arm64 ] https://repo.mongodb.org/apt/ubuntu focal/mongodb-org/4.4 multiverse" | sudo tee /etc/apt/sources.list.d/mongodb-org-4.4.list
```

## What it should look like: MongoDB key is added successfully

*Step #7*
# Install OpenSSL dependency:
```bash
sudo -i wget http://archive.ubuntu.com/ubuntu/pool/main/o/openssl/libssl1.1_1.1.1f-1ubuntu2_amd64.deb
sudo dpkg -i libssl1.1_1.1.1f-1ubuntu2_amd64.deb
```

## What it should look like: OpenSSL downloads and installs

*Step #8*
# Finalize MongoDB installation:
```bash
sudo apt update
sudo apt install mongodb-org
sudo systemctl start mongod
sudo systemctl enable mongod
```

## What it should look like: MongoDB installs and starts

*Step #9*
# Secure MongoDB with authentication:
```bash
mongo
```

In the MongoDB console, run the following commands:
```javascript
use Royal
```

Create a MongoDB user (replace "your_password" with a strong password):
**Important**: Go to "https://passwordsgenerator.net/", select 35 characters (NO SYMBOLS!!!)
**Example**: "HsncgKtUYdXCRB9WhTeQ75PL6pAxDJ8y2bZ"

```javascript
db.createUser({
  user: "root",
  pwd: "you_secret_passwd_here",
  roles: [{ role: "readWrite", db: "Royal" }]
})
```

```javascript
exit;
```

## What it should look like: User is created successfully

*Step #10*
# Enable authentication in MongoDB:
```bash
sudo nano /etc/mongod.conf
```

Add under the security section:
```yaml
security:
  authorization: "enabled"
```

**Instructions**: Save and close the file (Ctrl + O then ENTER / Ctrl + X to quit nano)

## What it should look like: Configuration file is modified

*Step #11*
# Restart MongoDB:
```bash
sudo systemctl restart mongod
sudo systemctl status mongod
```

If everything is fine (no error), press **Ctrl + C** to quit the logs

In your `config.json` file, line 102, update the MongoDB URL:
```json
"Database": {
  "MongoURL": "mongodb://root:your_password@localhost:27017/Royal"
}
```

## What it should look like: MongoDB restarts without error

*Step #12*
# Verify MongoDB authentication:
```bash
mongo -u root -p your_password --authenticationDatabase Royal
```

## What it should look like: You connect to MongoDB successfully

*Step #13*
# Install NVM and Node.js:
```bash
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.4/install.sh | bash
source ~/.bashrc
nvm install 22.9.0
nvm use 22.9.0
```

## What it should look like: Node.js version 22.9.0 installs

*Step #14*
# Install PM2:
```bash
npm install n -g
n latest
npm i pm2 -g
```

## What it should look like: PM2 installs globally

*Step #15*
# Navigate to Royal SRC directory and configure permissions:
```bash
cd RoyalSRC
chmod 777 *
```

## What it should look like: Permissions are set

*Step #16*
# Test Royal SRC:
```bash
./RoyalSRC
```

If Royal SRC starts correctly, press **Ctrl + C**

## What it should look like: Royal SRC starts without error

*Step #17*
# Start Royal SRC with PM2:
```bash
pm2 start "./RoyalSRC" --name RoyalSRC
```

## What it should look like: PM2 starts Royal SRC in background

---

*You have completed Royal SRC setup!*

---

# Managing Royal SRC with PM2

**View logs**: `pm2 log RoyalSRC`
**Stop Royal SRC**: `pm2 stop RoyalSRC`
**Restart Royal SRC**: `pm2 restart RoyalSRC`
**List processes**: `pm2 list`

---

# How to connect to Royal SRC

1. **Connect using SSH** (Use https://putty.org it's better)
   - **Host**: `Your server IP`
   - **Port**: `1339` or as specified in config.json line 7
   - **Type**: `SSH`

2. **First account saved in**: `/RoyalSRC/assets/config/login.json`

3. **Bonus - How to connect on your phone**: Open Google Chrome or Safari and go to https://ssheasy.com

---

# Launching attacks

1. Connect to Royal SRC
2. Run the command with the format: `<method> <target> <port> <duration>`
3. **Bonus DEBUG mode**: `<method> <target> <port> <duration> -d` (Owner user only)

---

# Troubleshooting

### If MongoDB doesn't start:
```bash
sudo systemctl status mongod
sudo journalctl -u mongod
```

### If Royal SRC doesn't connect to MongoDB:
- Check that MongoDB is running: `sudo systemctl status mongod`
- Check your credentials in `config.json`
- Test connection: `mongo -u root -p your_password --authenticationDatabase Royal`

### If PM2 doesn't start Royal SRC:
```bash
pm2 log RoyalSRC
```

---

# If you still need assistance, please contact:
- **Discord**: https://discord.com/channels/1358053746420219995/1358060457138852020
- **Telegram Support**: https://discord.com/channels/1358053746420219995/1358060485089562729
- **Website**: https://royalprojets.com

---

👑 **Created by royalprojets.com**

**Important note**: Always replace "your_password" with your actual password generated on https://passwordsgenerator.net/ (35 characters, no symbols).