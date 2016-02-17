#Celix Alpine
A Small docker image based on alpine containing Apache Celix

#Work in Progress
This image does not work (yet), still work in progress

#Known issues

- The thread pool in linux cannot be build. It uses pthread_setname_np. I seems that this should not really be needed (just changes the name of a thread)
- Remote shell does not work. Can be disabled by -DBUILD_REMOTE_SHELL=OFF 
