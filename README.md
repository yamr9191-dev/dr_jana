# DR:Jana 🌱

A mobile-first student PWA for planning, studying and growing.

## Included
- Tasks with completion percentage
- Agriculture college schedule
- Five daily prayers
- Notes and search
- Daily history
- Garden mini-game
- Private wellness/cycle section
- Local offline storage
- Firebase Authentication + Realtime Database sync
- Installable as an Android home-screen app

## Firebase setup
1. Open Firebase Console.
2. Enable Authentication -> Sign-in method -> Email/Password.
3. Create Realtime Database.
4. Put rules similar to:

```json
{
  "rules": {
    "users": {
      "$uid": {
        ".read": "auth != null && auth.uid === $uid",
        ".write": "auth != null && auth.uid === $uid"
      }
    }
  }
}
```

The Firebase web configuration is already inserted in `index.html`.

## GitHub Pages
Upload the contents of this folder to a GitHub repository, then:
Settings -> Pages -> Deploy from branch -> main -> /(root).

The app will be available at:
https://YOUR-USERNAME.github.io/YOUR-REPOSITORY/

Open it on Android -> browser menu -> Add to Home screen / Install app.

## Important
The Firebase web config is not a password. Database rules and Authentication protect the actual user data.
