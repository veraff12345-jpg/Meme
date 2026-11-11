# MEME — Android personal assistant (starter project)

A beginner-friendly Kotlin Android starter for a tap-to-talk Hindi/English assistant.

## Features in this starter
- Tap microphone to start recognition; it does not listen continuously.
- Android SpeechRecognizer for speech input (the phone's recognition provider may require internet).
- Android TextToSpeech for spoken replies.
- Basic local commands: greeting, time, date, assistant name, help.
- Local notes using SharedPreferences (`remember ...` and recall).
- Optional OpenAI-compatible HTTPS chat-completions endpoint. Online AI is OFF by default.
- No API key is included. A provider may charge or have usage limits; only use a provider whose free access you have verified.

## Build an APK using only your phone
1. Create a GitHub account if you do not already have one.
2. Create a new repository named `MEME-Android`.
3. Upload the contents of this folder to the repository (not the outer folder itself).
4. Open the repository's **Actions** tab.
5. Select **Build MEME Android APK**, then **Run workflow**. A push to `main` also starts a build.
6. When it finishes, open the workflow run, scroll to **Artifacts**, and download `MEME-debug-apk`.
7. Extract the ZIP on your phone and install `app-debug.apk`. Android may ask you to allow installation from your browser/file manager.

## Online AI configuration
Online AI is optional and disabled by default. To use it, you need an HTTPS chat-completions endpoint, a model name, and an API key from a provider. The app stores these in private app preferences on the phone. Do not put API keys in GitHub, source code, screenshots, or chat messages. Requests send the spoken text to that provider.

## Female voice
The app asks Android TextToSpeech to prefer an installed voice whose name contains "female". Many Android TTS engines do not label voices by gender, so a female voice is not guaranteed. Change the voice in Android Settings > Text-to-speech output and install a preferred Hindi/English voice if available.

## Limitations and privacy
- Microphone permission is requested only when you tap the mic.
- This starter does not run in the background, use a wake word, send texts, make calls, or control other apps.
- Speech recognition may be handled by Google or another installed speech service. Check that service's privacy settings.
- Local notes stay in app-private storage until app data is cleared/uninstalled.
- Online AI sends your recognized text to the endpoint you configure.
- Treat assistant responses as suggestions; confirm important actions yourself.

## Requirements
- Android Studio/Gradle build environment in GitHub Actions; Android device for installation.
- compileSdk 35, minSdk 26, Java 17, Gradle 8.9, Android Gradle Plugin 8.7.3.
