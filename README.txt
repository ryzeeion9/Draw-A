Atelier — Private Art Studio + Firestore Rules

File:
- atelier_private_art_studio.html: app with Firebase Auth and Firestore workspace sync code.
- firestore.rules: rules matching the app's cloud path users/{uid}/workspace/atelier.

IMPORTANT:
1. Publish firestore.rules in Firebase Console > Firestore Database > Rules.
2. Enable the sign-in providers used by the app in Firebase Authentication.
3. Make sure the Firebase configuration inside the HTML points to your Firebase project.
4. Cloud sync is not independently verified from this package. The app's current cloud save covers the main workspace state; some separately stored items (such as the pose/anatomy gallery) may remain local-only.
