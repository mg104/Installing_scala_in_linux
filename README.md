# Installing_scala_in_linux

1. Run the following commands:
   - curl -fLo cs https://git.io/coursier-cli-"$(uname | tr LD ld)"
   - chmod +x cs
   - ./cs install cs
   - rm cs

2. Run the command to open ~/.bashrc file and add the second line at the end of it:
   - sudo nano ~/.bashrc
   - export PATH=$PATH:/home/madhur/.local/share/coursier/bin

3. Run:
   - cs update cs
   - ./cs setup

4. Install Java by running the following command:
   - sudo apt install openjdk-16-jre-headless

5. Run the following command to find the path of the Java binary (bin) files:
   - sudo update-alternatives --config java

6. Copy the path that you get from above (usually /usr/lib/jvm/java-16-openjdk-amd64/bin/java) without "/bin/java" and add it to the /etc/environment file by running the following command:
   - sudo nano /etc/environment

7. Add the following line to the end of the above file:
   - JAVA_HOME="/usr/lib/jvm/java-16-openjdk-amd64"

8. Run the following command:
   - source /etc/environment
