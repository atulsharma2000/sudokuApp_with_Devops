# sudokuApp_with_Devops
here i used jenkins to automate updatation of my web app.
just by a commit it can test merge and publish my website globally 
i launched 2 docker containers of httpd 
and website launched using ngrok tunnels
In Jenkins following Jobs are created :-
Job1: connected to test_branch it will keep on checking and any commit made it will be copied to test-server using docker.
Job2: connected to master branch , same checking if any commit is made it will copy changes to production server using docker & it is also exposed to external world using pating for which I have used ngrok here.
Job3: It will be run by quality assurance team manually after checking test server working fine, this job will merger both branches at github n automatically trigger job2 .
