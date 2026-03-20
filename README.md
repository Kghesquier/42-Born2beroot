*This project has been created as part
of the 42 curriculum by kghesqui.*

Description : This project allows us to discover the fabulous world of Virtual Machines. VM can be really usefull for some of our next project in 42 and can often be used in companies so it's important to know how it works. For Born2beroot we will create our first VM using the features asked by the subject.

Instructions : Really simple for this project. Just start the VM clone called Born2beroot clone on Oracle and that's it. For the execution of the commands I will guide you during the defense.

Resources : I hadn't used AI for this project cause there was a lot of tutorials and documentation online. You can find some usefull websites I used for this project just bellow:
Debian :
https://www.peerspot.com/products/comparisons/debian_vs_rocky-linux
SSH :
https://phoenixnap.com/kb/how-to-enable-ssh-on-debian
UFW :
https://www.cyberciti.biz/faq/set-up-a-firewall-with-ufw-on-debian-12-linux/
VM :
https://www.informatiweb.net/tutoriels/informatique/virtualisation/virtualbox-virtualiser-rapidement-sa-1ere-machine-sous-virtualbox-7.html
LVM :
https://linuxhandbook.com/lvm-guide/
B2BR :
https://github.com/alx-sch/born2beroot
https://noreply.gitbook.io/born2beroot/correction-preparation/evaluation-answer

Project description :
I used Debian for the project because the subject and my peers told me to use it. And more seriously because it's the easiest one for beginners and the most documented one.

Debian pros: Easy to use, great for learning, huge community support, APT package manager is straightforward.
Debian cons: Packages are sometimes older versions, less commonly used in enterprise servers.
Rocky pros: Better for enterprise environments, SELinux is more powerful for security, closer to what companies actually use.
Rocky cons: Harder learning curve, fewer beginner-friendly tutorials, more complex to configure.

Partitioning: I used LVM with encryption to make the system flexible and secure. Created separate partitions for /, /home, /var, and /tmp to isolate different parts of the system.
Security policies: Set up strong password rules and configured sudo with strict logging to track all administrative commands.
User management: Created regular users with limited permissions and used groups to control access. Root login via SSH is disabled for security.
Services installed: SSH for remote access, UFW firewall to block unwanted connections, and a monitoring script that runs every 10 minutes.

Debian vs Rocky Linux:
Debian uses APT package manager and is community-driven, making it simpler and more beginner-friendly. Rocky uses DNF/YUM and follows RedHat standards, making it better for professional server environments but harder to learn.
AppArmor vs SELinux:
AppArmor (Debian's default) is easier to understand and uses simple file paths for security rules. SELinux (Rocky's default) is more powerful and secure but much more complex, using labels and contexts that are harder to configure.
UFW vs firewalld:
UFW is super simple with easy commands like "ufw allow 4242" - perfect for basic firewall needs. Firewalld is more powerful with zones and rich rules but requires more knowledge to use properly.
VirtualBox vs UTM:
VirtualBox works on Windows, Mac, and Linux with the same interface everywhere - it's free and has tons of tutorials. UTM is made specifically for Mac (especially M1/M2 chips) and runs faster on Apple Silicon but only works on macOS.
