1. Copy war file from jumphost to server

        scp /tmp/ROOT.war steve@stapp02:/tmp

2. SSH into server

        ssh tony@stapp01
        sudo su -

3. Install tomcat


        yum install -y tomcat


4. Copy war file from tmp to tomcat path


        cp /tmp/ROOT.war /usr/share/tomcat/webapps


5. Edit the tomcat configuration file and replace all ConnectorPort port with the required port

        vi /usr/share/tomcat/conf/server.xml


6. Start tomcat server

        systemctl start tomcat

7. Reimplement this for the second time