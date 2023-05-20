After the Splash page, the Login page will be displayed.
I have sent the video of the UI appearance to the Element chat group, you can watch it from there (fix some text styles).

A) If the device supports Biometric authentication:
1) The user will be asked for their fingerprint or face recognition, and if the user uses it, they will go to the Home page.
2) If the user does not want to use Biometric authentication, they can enter a Pin code and sign in from there.
3) If the user accidentally denies Biometric authentication, there is a button for them to use it again.
4) If the user does not want to use fingerprint or face ID, they can sign in with either the device's Pin code or the Encointer Pin code.

B) If the device does not support Biometric authentication:
1) When trying to use Biometric authentication, a Snackbar will be displayed, such as "this device is not supported," and the user can sign in by entering a Pin code.
2) If the password is entered correctly, the Home page will open.
3) If the password is incorrect, the Pin code will be reset, and a Snackbar will be displayed saying "Password is incorrect."

Note: Other banking apps or apps using Pin code use a static 4 to 6 digit Pin code. In the example design in the task description, it is also based on a 4-digit Pin code. However, in our application, the user can use a Pin code of 4 to 20 characters. I wrote it based on that, please check it.

Extra: All `pushAndRemoveUntil` methods changed to  `pushNamedAndRemoveUntil`.

Suggestion: Our `Api` `Webview` and `Stores` all initialize in the splash view, and app takes a bit longer to open. Now, when the app opens, the create or login pages will be visible. Let's only check if the user exists in the splash view, and perform other actions only after create or login. I think this way, the app can open faster. Metamask takes too long to open and that bothers me :)

Please review the text that I used, I need help with this :).  
| Name | English | German | French | Russian |
|----------|-------------|----------|-------------|-------------|
| welcome | Welcome | Willkommen | Bienvenue | Добро пожаловать |
| biometricError | Your device does not support biometric authentication | Ihr Gerät unterstützt keine biometrische Authentifizierung | Votre appareil ne prend pas en charge l'authentification biométrique | Ваше устройство не поддерживает биометрическую проверку подлинности |
| passwordError | Password is incorrect | Das Passwort ist falsch | Le mot de passe est incorrect | Неверный пароль |
| signIn | Sign in  | Anmelden | Se connecter | Войти |
| localizedReason | Login to your account using the security feature on your device. | Melden Sie sich mit der Sicherheitsfunktion Ihres Geräts an Ihrem Konto an. | Connectez-vous à votre compte en utilisant la fonction de sécurité de votre appareil. | Войдите в свой аккаунт, используя безопасную функцию вашего устройства. |
