# How to use the panel\_installer script

Load it onto your server by whatever means you prefer (e.g. scp). 
Make sure it is executable:

	chmod 755 panel_installer

Then run it (as root!):

	./panel_installer

You will be prompted to select what exactly you want to install. After that, 
the installation will start and a detailed log will be created in the file 
panel\_installer.log. It is a good idea to keep this file, so you can debug any 
problems that might arise later on.

## Additional sources

During the installation you will be asked whether you want to add sources to 
your '/etc/apt/sources.lst'. If you are sure that they are already properly 
configured, you can skip this step by selecting 'no' and 'skip'.

## Postfix & Courier

When asked about the configuration for postfix select 'internet site' and 
afterwards answer 'yes' to setting up the configuration directories for courier.

## Cleanup

The cleanup procedure will ask you whether to run 'apt-get autoremove' this will 
remove any unused dependencies from your system (not just the ones used during 
the installation). On a clean system this should be absolutely safe.

This is the last step in our installation script.



## openpanel-admin password setup

The OpenPanel installation guide says that OpenPanel may ask you to specify an openpanel-admin (the default admin user for OpenPanel) password.

In our test runs, it did not, and you should run the following commands as root in your shell:

'openpanel-cli'

    [openpanel]% password user openpanel-admin

    Enter new password:
    Retype new password:

    [openpanel]% exit

(enter your new password twice, followed by enter)


## OpenPanel Web interface

You should now be able to access the OpenPanel web interface via port 4089 on 
your machine’s IP or hostname.


## Questions & Problems

Feel free to fork this script, and improve upon it. We also may be able to help you with smaller problems.