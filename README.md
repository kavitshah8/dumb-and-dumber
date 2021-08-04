# dumb-and-dumber
Most memorable learning experiences

1. Set up alias in my bash environment, which might overwrite some native commands

alias clean=`rm -rf node_modules && rm -rf ~/.inhouse_framework_cache && yarn cache clean && grunt clean && grunt cache:clean && git clean -dfx && yarn install && grunt setup`

Above alias looks innocent but it was cleaning up all the local cache during every xCode build. Hence, my build time increased almost 5-6 times.

Lesson: Add namespace or convention, that aliases do not collide. For example, `alias KsClean = rm -rf node_modules && rm -rf ~/.inhouse_framework_cache && yarn cache clean && grunt clean && grunt cache:clean && git clean -dfx && yarn install && grunt setup` would have avoided the problem. 

Lesson: Sing out and Sign in again in your computer to make sure bash changes take place outside of bash terminal. 
