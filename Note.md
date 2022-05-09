__*GIT*__

# Add new remote origin (in this case, GitHub)
git remote add origin git@github.com:Wahaha-007/OtherNav.git

--> After that for the first push (recommend by Git display)
git push --set-upstream origin main

# Changing Git Remote to SSH
git remote set-url origin git@github.com:Wahaha-007/OtherNav.git

# Verify change
git remote -v

__*EXPO*__

# Expo On WSL
    "start:wsl": "REACT_NATIVE_PACKAGER_HOSTNAME=$(netsh.exe interface ip show address 'Network Bridge' | grep 'IP Address' | sed -r 's/^.*IP Address:\\W*//') expo start",


__*NAVIGATOR*__

# Adding Drawer Navigator
expo install @react-navigation/drawer
expo install react-native-gesture-handler react-native-reanimated
npx expo install react-native-safe-area-context@4.2.4 react-native-screens@~3.11.1   => Follow Expo hint


--XXX npm install react-native-reanimated@1 --save --save-exact => Not work
--XXX npx expo install react-native-reanimated@~2.8.0 => Back to originl, also not work


# Work ! Method
1. Edit babel.config.js
    plugins: ['react-native-reanimated/plugin']

2. use expo r -c instead  // Some kind of clear cache ?
3. Close server and npm run start:wsl => OK