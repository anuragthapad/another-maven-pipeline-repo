If you just set Poll Scm with cron expression H H/2 * * *, it will trigger the 
build for every 2 hours but the build will also be triggered if a git commit 
happens and it is not 2 hours yet.

If you check option "Ignore post-commit hooks" along with the above cron expression 
in Poll SCM, this will Ignore changes notified by SCM post-commit hooks and now the 
build will be triggered only if there is a commit and it has been 2 hours..
