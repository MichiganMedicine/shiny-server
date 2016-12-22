# R Shiny Server Pro Configs for the University of Michigan IT Environment
This is the directory R Shiny uses for its configuration.  It is located in /etc/shiny-server.  
## Environment  
### HITS Silver Cloud  
#### Operating System and Configuration  
* HITS Standard RHEL 7 Template  
* Level 2 Shell Auth  
* Login Group umms-shiny-login managed by Service Desk and HITS Research  
* Addition of Tripwire  
* Cron configured to run once daily at midnight  
* Configured to mail to root on local machine  
* Addition of ShinyApps directory to /etc/skel  
### Application Configuration  
#### R Studio  
* [Packages](https://shiny.med.umich.edu/packages/packages.html)    
#### R Shiny Pro  
* ssl certificate and key in /home/shiny/  
* shiny-server.conf
#### Custom HTML Templates  
* /etc/shiny-server/templates  
* /srv/shiny-server/index.html 
#### Custom Publisher Directory  
* /srv/shiny-server  
* cron job created to call /etc/shiny-server/directory.sh to build every 4 hours
