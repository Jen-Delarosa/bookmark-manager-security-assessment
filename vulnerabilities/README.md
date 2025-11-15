For each PoC I share how to run it and what to expect when they are ran. All scripts print out the auhtenticaion code, I manually typed in the auth code into the url. For example if the auth code were 123456 I typed into the browser 'http://127.0.0.1:8888/123456/' to see the results of running my scripts. EXCEPT for vulnerability4 you can have bcbmc open in a browser already. 


1. To run PoC 1 which is titled Vulnerability1.py:
  First you need to have a bcbmc account that has atleast one bookamrk valid url saved.
  Now before the user loads their bookmark manager again into a web browser you need to load bcbmc in a VM temrinal, by just runing bcbmc.
  Then in a different VM temrinal run the command 'python3 vulnerability1.py' this should print out the authentication code, and
  a message that says "bookmark deleted" to confirm each possible bookmark has been deleted. Now when the user opens their web browser with the same authentication code all of     their valid bookmarks should be deleted.

2. To run PoC 2 which is titled Vulnerability2.py:
   First I ran bcbmc in a VM terminal and then in a different VM terminal
   I ran 'python3 vulnerability2.py' this will print out the authentication code and
   a print statement saying "injected evil website". Now when the user loads the
   website with the same auth code they should see a new bookmark titled 'Health Care'.
   When the user clicks on Health Care they are redirected to mr.superevilguy.com, which is
   assumed to be a malicious website. This PoC shows how easy it is for an outsider to inject
   any website they want into a users bcbmc with just the authentication code.
   
3. To run PoC 3 which is titled Vulnerability3.py:
   First I ran bcbmc in a VM terminal and then in a different VM terminal
   I ran 'python3 vulnerability3.py'. The authentication code is printed out and a message saying that a a website was added wiht fav rank as 11. Then when you access the local host with that auth code that was printed out, and click on top ten favorites the server crashes. This is supposed to simulate a mindless user adding a non valid rank to their fav bookmarks.

4. To run PoC 4 which is titled Vulnerabilit4.py:
   Before runing the script it's assumed that there is an account setup on bcbms
   that has the email 'student3@localhost' and its own password. To run the scirpt First I ran bcbmc in a VM terminal and then in a different VM terminal
   I ran 'sudo python3 vulnerbility4.py'. It has to run with sudo becuase it reads the bcbms logs that reveal tokens being sent to      emails. After running the script the attacker can now login to student3@localhost account with the passowrd haha.
   So to see that this worked I went to the sync to cloud page and input the email as 'student3@localhost' and the pasword as 'haha' (no quotes for either fields). Then the login was successfull. 
   
