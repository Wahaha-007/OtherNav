- Add new remote origin (in this case, GitHub)
git remote add origin git@github.com:Wahaha-007/OtherNav.git

--> After that for the first push (recommend by Git display)
git push --set-upstream origin main

- Changing Git Remote to SSH
git remote set-url origin git@github.com:Wahaha-007/OtherNav.git

- Verify change
git remote -v



Expo On WSL
-----------------------------------
    "start:wsl": "REACT_NATIVE_PACKAGER_HOSTNAME=$(netsh.exe interface ip show address 'Network Bridge' | grep 'IP Address' | sed -r 's/^.*IP Address:\\W*//') expo start",
