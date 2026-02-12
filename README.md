[![ReadMeSupportPalestine](https://raw.githubusercontent.com/Safouene1/support-palestine-banner/master/banner-project.svg)](https://s.id/standwithpalestine)

# PHPNuxBill - PHP Mikrotik Billing

![PHPNuxBill](install/img/logo.png)

## Feature

- Voucher Generator and Print
- [Freeradius](https://github.com/hotspotbilling/phpnuxbill/wiki/FreeRadius)
- Self registration
- User Balance
- Auto Renewal Package using Balance
- Multi Router Mikrotik
- Hotspot & PPPOE
- Easy Installation
- Multi Language
- Payment Gateway
- SMS validation for login
- Whatsapp Notification to Consumer
- Telegram Notification for Admin

See [How it Works / Cara Kerja](https://github.com/hotspotbilling/phpnuxbill/wiki/How-It-Works---Cara-kerja)

## Payment Gateway And Plugin

- [Payment Gateway List](https://github.com/orgs/hotspotbilling/repositories?q=payment+gateway)
- [Plugin List](https://github.com/orgs/hotspotbilling/repositories?q=plugin)

You can download payment gateway and Plugin from Plugin Manager

## System Requirements

Most current web servers with PHP & MySQL installed will be capable of running PHPNuxBill

Minimum Requirements

- Linux or Windows OS
- Minimum PHP Version 8.2
- Both PDO & MySQLi Support
- PHP-GD2 Image Library
- PHP-CURL
- PHP-ZIP
- PHP-Mbstring
- MySQL Version 4.1.x and above

can be Installed in Raspberry Pi Device.

The problem with windows is hard to set cronjob, better Linux

## Changelog

[CHANGELOG.md](CHANGELOG.md)

## Installation

[Installation instructions](https://github.com/hotspotbilling/phpnuxbill/wiki)

## Freeradius

Support [Freeradius with Database](https://github.com/hotspotbilling/phpnuxbill/wiki/FreeRadius)

## Community Support

- [Github Discussion](https://github.com/hotspotbilling/phpnuxbill/discussions)
- [Telegram Group](https://t.me/phpmixbill)

## Technical Support

This Software is Free and Open Source, Without any Warranty.

Even if the software is free, but Technical Support is not,
Technical Support Start from Rp 500.000 or $50

If you chat me for any technical support,
you need to pay,

ask anything for free in the [discussion](/hotspotbilling/phpnuxbill/discussions) page or [Telegram Group](https://t.me/phpnuxbill)

Contact me at [Telegram](https://t.me/ibnux)

## License

GNU General Public License version 2 or later

see [LICENSE](LICENSE) file


## Donate to ibnux

[![Donate](https://img.shields.io/badge/Donate-PayPal-green.svg)](https://paypal.me/ibnux)

BCA: 5410454825

Mandiri: 163-000-1855-793

a.n Ibnu Maksum

## SPONSORS

- [mixradius.com](https://mixradius.com/) Paid Services Billing Radius
- [mlink.id](https://mlink.id)
- [https://github.com/sonyinside](https://github.com/sonyinside)

## Thanks
We appreciate all people who are participating in this project.

<a href="https://github.com/hotspotbilling/phpnuxbill/graphs/contributors">
  <img src="https://contrib.rocks/image?repo=hotspotbilling/phpnuxbill" />
</a>


Step 1: Install Docker Desktop
Download Docker Desktop for Windows
Install it and restart your computer
Verify installation in PowerShell:

docker --version

Step 2: Configure Docker Compose
The docker-compose.example.yml is already in your project. You can use it as-is, or create a docker-compose.yml copy for your local setup:

Step 3: Start Docker Containers
Open PowerShell and navigate to your project:

cd c:\Users\Administrator\Documents\isp_billing\phpnuxbill

Start the containers:

docker-compose up -d

This downloads MySQL 8.0, builds the PHP/Apache image, and starts both services.

Verify containers are running:

docker-compose ps

You should see both nuxbill and mysql containers with status "Up"

Step 4: Access the Installation Wizard
Open your browser and go to: http://localhost/install/

Follow the installer steps:

Step 1: Accept terms & continue
Step 2: System requirements check
Step 3: Database configuration:
Host: mysql
User: nuxbill
Password: 12345678
Database: nuxbill
Step 4: Admin account creation
Step 5: Finish installation
After installation, access the app at: http://localhost

Step 5: Database Access (Optional)
If you need to directly access MySQL:

docker exec -it mysql mysql -u nuxbill -p12345678 nuxbill

Or use MySQL Workbench/phpMyAdmin:

Host: localhost
Port: 3306
User: nuxbill
Password: 12345678
Useful Docker Commands

# View logs
docker-compose logs -f nuxbill

# Restart container
docker-compose restart nuxbill

# Stop all containers
docker-compose down

# Stop and remove volumes (clean reset)
docker-compose down -v

# Access PHP container shell
docker exec -it nuxbill bash
docker --version
That's it! Your PHPNuxBill application should be running on Windows via Docker. Let me know if you encounter any issues!