# gmxpbsa_dev 2.1.2
MM/PBSA binding free energy calculation dev version
This version GMXPBSA-2.1.2_devel contains some new
features with respect to GMXPBSA-2.1.2:

1. possibility to keep a number of water molecule to be used in the
binding free energy calculation. This in case you want to
exploit this approach:
http://pubs.acs.org/doi/abs/10.1021/ct400045d


2. fix a bug when using pbs queue manager. On the cluster
the OMP threads should be = 1. Normally to fix the issue it is
enough to set:

export OMP_NUM_THREADS=1

before to run the scripts. For some unknown reason on some cluster
this trick does not work.  With this devel version we force mdrun
to use only one tread (-ntomp 1)
