To create AD account
https://confluence.rakuten-it.com/confluence/display/RSQS/SymLab_IDM+User+Onboarding+Request+Form



- vpn-symlab.symphony.rakuten-it.com
- tunnel creation(SOCKS PROXY with dynamic port forwarding):  ssh jaya.thakur@192.168.50.3 -D1444
-  nc -zv localhost 1444
-  git config --list
-  git config user.name jaya-thakur
- git config --local https.proxy socks5://localhost:1444
- git config --local http.proxy socks5://localhost:1444
- git config --local http.https://github.rsym-cicd.blr.rsicdcdns.lab.sslVerify false
- git clone https://token@github.rsym-cicd.blr.rsicdcdns.lab/OSS/maven-repo.git -c http.proxy=192.168.50.3:3128 -c http.https://github.rsym-cicd.blr.rsicdcdns.lab.sslverify=false
- nslookup github.rsym-cicd.blr.rsicdcdns.lab


--
Github conflicts resulve
---
1. switched to new branch so no need to add new commit.
2. we are in staging area, when we have conflicts.
3. then again we need to rebase once the conflicts resolved, then only to generate the pr.


--
Github naming conventions
--
1. feature branch - feature/{ticket-id}-{short-description}
2. bugfix branch - bugfix/{ticket-id}-{short-description}
3. hotfix/{ticket-id}-{short-description}
4. experiment/{short-description} or spike/{short-description}
5. chore/{short-description}


--
Git checkout and switch
--
git checkout main                # Switch to the 'main' branch
git checkout -b new-branch       # Create and switch to 'new-branch'
git checkout <commit-id> <file>  # Restore a specific file from a commit

git switch main                  # Switch to the 'main' branch
git switch -c new-branch         # Create and switch to 'new-branch'

