The Nautilus devops team got some requirements related to some Apache config changes. They need to setup some redirects for some URLs. There might be some more changes need to be done. Below you can find more details regarding that:



httpd is already installed on app server 3. Configure Apache to listen on port 6100.

Configure Apache to add some redirects as mentioned below:

a.) Redirect http://stapp03.stratos.xfusioncorp.com:<Port>/ to http://www.stapp03.stratos.xfusioncorp.com:<Port>/ i.e non www to www. This must be a permanent redirect i.e 301

b.) Redirect http://www.stapp03.stratos.xfusioncorp.com:<Port>/blog/ to http://www.stapp03.stratos.xfusioncorp.com:<Port>/news/. This must be a temporary redirect i.e 302.