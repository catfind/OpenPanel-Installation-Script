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

## OpenPanel Web interface

You should now be able to access the OpenPanel web interface via port 4089 on 
your machine’s IP or hostname.
