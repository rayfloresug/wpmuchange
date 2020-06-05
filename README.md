##In case you want to pass a multisite of subfolders to subdomains, the process is exactly the same, but in reverse:

1) For security copies of the database and the wp-config.php and .htaccess files
2) Set the >SUBDOMAIN_INSTALL to true in wp-config.php  
3) Change the rules in the htaccess by the subdomains (more info here)
4) Change the domain column of the wp_blogs table in all sites, establishing the subdomains of each site. Simply leave the pathfield with the bar /
5) Through the Search & Replace or WP-CLI script, replace all URLs of the type mydomain.com/site1 with site1.mydomain.com
6) Check to see that everything is working correctly.