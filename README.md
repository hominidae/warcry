# Project Description
  Warcry is a software project to assess the practical efficacy
 of implementing an affordably portable Direction Finding system
 using commercial off-the-shelf equipment.
 
 Major design goals:
  - Mobile Ad-hoc Networking between hand-held units
  - Passively Networked Pseudo-doppler Radio Direction Finding

# Project Instructions
 1. Acquire the basic Raspberry Pi "Kite" build

  - What will you need to build/participate in this project?
   . Raspberry Pi 2 (or Raspbery Pi 3)
   . RTL-SDR (Available at www.rtl-sdr.com)
   . A High Gain 802.11/b/g/n WiFi Adapter
     Recommended:
      x Alfa Networks AWUS036NHA
      x TP-Link WN722N

 2. Great. I have these, now what? Simple, follow these steps:

   1. Download and install the latest Rasbpian Jessie Lite on a MicroSD card. 
   2. Insert the MicroSD card into your Raspberry Pi
   3. Setup Raspbian:
     This includes, running "sudo raspi-config" then expanding your filesystem,
     changing your password, and additionally running "sudo apt-get update".

   4. Connect your WiFi adapter and your RTL-SDR to your Raspberry Pi
     You may need a USB hub to safely power the wireless adapter without
    causing the Raspberry Pi to hang or run improperly.
   5. Run "dmesg" to confirm your devices are connected and functional. Alternatively,
     run "lsusb" to confirm they are connected. You should see both your RTL-SDR
     and your WiFi adapter.

   6. Your first order of business should be setting your Wireless regulatory
     domain. This will restrict your WiFi adapter to follow your local regulatory
     radio frequency restrictions, if any exist in your jurisdiction. This is
     important because microwaves are very dangerous and you could hurt yourself
     with mis-information. If you don't wear tinfoil on your head, you could get
     yourself seriously hurt.

     You can set this by running "sudo iw reg set CA". Alternatively, you can use
     your own two letter country code. US, GB, CA are other common examples.

     See ISO 3166-1 Alpha-2 for your two letter country code.
     https://en.wikipedia.org/wiki/ISO_3166-1_alpha-2

     Note: You can set this permanently by opening "/etc/default/crda" and
     appending your country code there. You'll need to use sudo to do this.

   7. You are now ready to run the scripts from this GIT repository.

     Note: There are currently no scripts available.
