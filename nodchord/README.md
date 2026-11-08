# Nodchord

**Shape a chord with your hands. Nod to play it.**

A webcam instrument that runs entirely in your browser. No app to install, no account, no MIDI gear.

**▶ Play it: https://YOUR-USERNAME.github.io/nodchord/**

![Nodchord demo](preview.png)

## How it works

- **Your thumb is the root.** Each other finger plays the key as far from the thumb as you spread it: upward for the right hand, downward for the left.
- **Curl a finger to leave it out.** Three fingers up is a triad, five is a big voicing, and you can play inversions, sevenths and clusters just by changing your hand.
- **Nod to play.** Both hands sound together on the nod, with a neon shockwave and the note names flying off your fingertips.
- **The note above each fingertip** shows what the next nod will play, so you can adjust before you commit.

Wrong notes are part of it. There is no scale lock.

## Play

1. Open the link above in Chrome or Edge on a laptop or desktop and press **Start camera and sound**.
2. Sit so your whole face is near the top of the frame. Palms face the camera, right hand on the right half of the screen, left hand on the left.
3. Go to **Play**, shape a chord, and nod.

**Calibrate** is optional but worth doing once. It learns the size and direction of your nod, then how far apart your fingers sit in two piano shapes (C D E F G and C E G C). It is saved in your browser.

### Sounds

Classic piano, electric piano and guitar (the guitar strums low to high). All three are synthesized live in the browser.

### Avatar and recording

Switch to **Avatar** and an original neon character stands in for your camera image. It follows your head, blinks when you blink, opens its mouth when you do, and its antenna flares on every nod.

**Record video** saves the stage, the effects and the instrument's sound as an `.mp4` where supported, otherwise `.webm`. Tick **Include my microphone** to sing or talk over it; your voice goes only into the recording, never to the speakers. Wear headphones so the mic does not also pick up the instrument. Go fullscreen first so the video uses the whole frame. The nod meter is hidden while recording.

### Keys

| Key | Does |
|---|---|
| `1` `2` `3` | Classic piano / electric piano / guitar |
| `V` | Camera / avatar |
| `R` | Start / stop recording |
| `F` | Fullscreen |
| `←` `→` | Move the right-hand root by a white key (`Shift` for a semitone) |
| `↑` `↓` | Right-hand root up / down an octave |
| `A` `D` · `W` `S` | The same for the left hand |
| Click / right-click a key | Set the right / left root |

## Run it on your own computer

The camera only works over `https://` or on `localhost`, so double-clicking `index.html` may not work. Start a tiny local server in this folder instead, then open `http://localhost:8000` in Chrome.

**Mac.** Open Terminal, type `cd ` and drag this folder onto the window, press Return, then run:

```
python3 -m http.server 8000 --bind 127.0.0.1
```

If macOS offers to install the command line developer tools, accept and run the line again. If the camera stays black, turn Chrome on under **System Settings → Privacy & Security → Camera** and restart Chrome.

**Windows.** In Command Prompt, in this folder:

```
py -m http.server 8000 --bind 127.0.0.1
```

## Privacy

Your video never leaves your computer. Hand and face tracking run locally in the browser with Google's MediaPipe. The page downloads only the tracking models (from `cdn.jsdelivr.net` and `storage.googleapis.com`) and fonts. Calibration lives in your browser's local storage, and recordings are saved straight to your machine.

## Good to know

- Works on macOS and Windows in Chrome or Edge, on a desktop or laptop with decent, even lighting. Phones and tablets are not supported.
- Hands are told apart by which side of the screen they are on, so crossing them swaps them.
- If nods stop registering, watch the meter at the top: it says **FACE NOT FOUND** when your face is out of frame.
- Expect about 0.15 s between starting a nod and hearing the chord, so nod slightly ahead of the beat.

## Built with

- [MediaPipe Tasks Vision](https://developers.google.com/mediapipe) 0.10.14 for hand and face landmarks (Apache 2.0)
- Web Audio API for every sound; no samples
- One HTML file, no build step

## License

MIT. See [LICENSE](LICENSE).

---

## 한국어

**손으로 코드 모양을 만들고, 고개를 끄덕이면 연주됩니다.** 설치 없이 브라우저에서 바로 돌아가는 웹캠 악기예요.

- 엄지가 근음이고, 나머지 손가락은 엄지에서 벌린 만큼 위(오른손)나 아래(왼손) 건반을 칩니다.
- 손가락을 접으면 그 음은 빠집니다. 자리바꿈, 7화음, 클러스터도 손 모양만으로 만들 수 있어요.
- 끄덕이면 양손 코드가 함께 울리고, 손가락끝 위에는 다음 끄덕임에 울릴 음이 미리 표시됩니다.
- 클래식 피아노, 일렉피아노, 기타 중에서 고를 수 있고, 아바타 모드와 영상 녹화(마이크 포함 가능)도 지원합니다.

Chrome에서 위 링크를 열고, 얼굴 전체가 화면 위쪽에 들어오게 앉은 뒤 손바닥이 카메라를 보게 해주세요. 영상은 컴퓨터 밖으로 나가지 않고 브라우저 안에서만 처리됩니다.
