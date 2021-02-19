.. _Upgrade XDM:

Upgrade XDM
===========

#. Install the new ISO:
   
   .. code::
      
      curl -u '$CREDS' https://eve.devsca.com/github/scality/zenko/artifacts/builds/github:scality:zenko:staging-2.0.0.r210210230152.7c4bbdc.pre-merge.00015938/zenko-2.0.0-beta.3.iso -o zenko-2.0.0-beta.3.3.iso

#. Import the ISO:

   .. code::
      
      /srv/scality/metalk8s-2.6.0/solutions.sh import --archive /home/centos/zenko-2.0.0-beta.3.3.iso

#. Activate the ISO:

   .. code::
      
      /srv/scality/metalk8s-2.6.0/solutions.sh activate --name zenko --version 2.0.0-beta.3

#. Add the ISO into the namespace:

   .. code::
      
      /srv/scality/metalk8s-2.6.0/solutions.sh add-solution --name zenko --solution zenko --version 2.0.0-beta.3
