# Warcry
  Warcry is software project to assess the practical efficacy
 of a implementing affordable commercial off the shelf hardware
 as components in a psuedo-doppler software based direction finding
 system.

# Project Instructions
 1. Acquire the basic Raspberry Pi "Kite" build
  - What will you need to build/participate in this project?
   . Raspberry Pi B+ (Or Raspberry Pi 2)
   . RTL-SDR (Available at www.rtl-sdr.com)
   . A High Gain 802.11/b/g/n WiFi Adapter
    Recommended:
    x Alfa Networks AWUS036NHA
    x TP-Link WN722N

  - Great. I have these, now what?
 
 2. Follow these steps:

   1. Download and install the latest Rasbpian Jessie Lite on a MicroSD card.
 
   2. Insert the MicroSD card into your Raspberry Pi

   3. Setup Raspbian:
     This includes, running "sudo raspi-config" then expanding your filesystem,
     changing your password, and additionally running "sudo apt-get update".

   4. Connect your WiFi adapter and your RTL-SDR to your Raspberry Pi

   5. Run "dmesg" to confirm your devices are connected. Alternatively,
     run "lsusb" to confirm they are connected.

   6. Your first order of business should be setting your regulatory domain.
     This will enable your WiFi adapter to follow your local regulatory radio
     frequency restrictions, if any exist in your jurisdiction.

     You can do this by running "sudo iw reg set CA".

     Alternatively you can use your own two letter country code.
     US, GB, CA are other common examples.

     See ISO 3166-1 Alpha-2 for your two letter country code.
     https://en.wikipedia.org/wiki/ISO_3166-1_alpha-2

     Note: You can set this permanently by openning "/etc/default/crda" and
     appending your country code there.

   7. You are now ready to run the scripts from this GIT repository.
     Note: There are currently no scripts available.
