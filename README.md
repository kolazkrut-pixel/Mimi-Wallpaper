[README.md](https://github.com/user-attachments/files/33879711/README.md)
# Mimi Wallpaper

![Mimi Wallpaper](preview.jpg)

**[English](#english) · [Русский](#русский)**

---

## English

Live desktop wallpaper that dances to whatever is playing on your PC: music in the browser, Spotify, Yandex Music, YouTube or a game. One self-contained HTML file on WebGL2. No servers, no tracking, and it works offline.

### Features

- **Reacts to all system audio.** It catches beats, drops and BPM, and splits the sound into bass, mids and highs.
- **10 scenes:** Rays, Flash, Wave, Nebula, Vortex, Ring, Hyperjump, Tunnel, Equalizer and Kaleidoscope. They can switch on their own with the music, or you can lock one.
- **8 color palettes** with smooth transitions.
- **Visual effects:** bloom, chromatic aberration, film grain and a camera kick on beats.
- **Now playing.** Shows the track title and artist in the bottom-right corner, away from desktop icons.
- **Calm when silent.** The wallpaper keeps breathing slowly instead of freezing on a black screen.
- **Light on resources.** It pauses during fullscreen games and lowers its resolution if it starts to lag.
- **Gentle flashes mode** for sensitive eyes.

### Installation

#### Lively Wallpaper (free, recommended)

1. Install [Lively Wallpaper](https://www.rocksdanister.com/lively/) from the Microsoft Store.
2. Download `Mimi_Wallpaper.zip` from [Releases](../../releases).
3. Drag the zip into the Lively window as is, without unpacking it.
4. Right-click **Mimi Wallpaper**, then choose **Set as Wallpaper**.

#### Wallpaper Engine

1. Unpack the archive into `steamapps\common\wallpaper_engine\projects\myprojects\Mimi`.
2. Restart Wallpaper Engine. The wallpaper will appear in your library.

### Settings

You can change these in the wallpaper's customize panel in Lively or Wallpaper Engine:

| Setting | What it does |
|---|---|
| Scene | A fixed scene, or automatic switching |
| Colors | A fixed palette, or automatic switching |
| Audio sensitivity | Raise it if the wallpaper barely reacts |
| Motion speed, trail length | How fast and how smooth the motion is |
| Brightness, bloom | How bright the picture and its glow are |
| Image quality | Lower it if the PC is weak or the wallpaper lags |
| Frames per second | 30, 60 or unlimited (Lively only) |
| Gentle flashes, film grain, track title | Toggle each one on or off |

### Browser version

`mimi_visualizer.html` is the same visualizer as a standalone page. Open it in Chrome or Edge and pick a sound source: a browser tab, the whole system, a microphone, audio files or a demo beat. It can also:

- record video with sound (`R`) and save a frame as PNG (`S`);
- play a playlist of files that you drag into the window.

Press `?` to see all hotkeys.

### Troubleshooting

- **It doesn't react to sound.** Make sure the audio plays through the default Windows output device. Lively takes the sound from there.
- **No track title.** The player has to support the Windows media overlay, the popup that appears when you press the volume keys. Chrome, Spotify and Yandex Music support it.
- **It lags.** Lower "Image quality" and set the frame limit to 30.
- **You changed the files but nothing changed.** Delete the wallpaper from the Lively library and import the zip again.

### Project structure

```
index.html              the visualizer itself (WebGL2, one file)
LivelyInfo.json         Lively manifest
LivelyProperties.json   settings for Lively
project.json            manifest and settings for Wallpaper Engine
thumbnail.jpg           library thumbnail
preview.jpg             preview image
```

### How it works

Each frame, the previous frame is zoomed, rotated and warped with noise, faded slightly, and new light is drawn on top. That feedback loop creates the trails and the sense of depth. The light comes from rays, the spectrum ring, the tunnel, the equalizer and the stars. After that, bright areas get a bloom pass, and a tone mapping step turns the result into the final image. Lively and Wallpaper Engine send the audio spectrum to the page. The page finds beats in it using spectral flux against an adaptive threshold.

### Author

**koliziym**

---

## Русский

Живые обои для рабочего стола, которые танцуют под всё, что играет на компьютере: музыку в браузере, Spotify, Яндекс Музыку, YouTube или игру. Это один самодостаточный HTML-файл на WebGL2. Без серверов и слежки, работает офлайн.

### Возможности

- **Реагирует на весь звук системы.** Ловит доли, дропы и темп (BPM), разделяет звук на бас, середину и верха.
- **10 сцен:** Лучи, Вспышка, Волна, Туман, Воронка, Кольцо, Гиперпрыжок, Тоннель, Эквалайзер и Калейдоскоп. Они могут меняться сами под музыку, или можно закрепить одну.
- **8 палитр** с плавными переходами.
- **Эффекты:** свечение (bloom), хроматическая аберрация, зерно плёнки и толчок камеры на долях.
- **Название трека.** Показывает название и исполнителя в правом нижнем углу, не перекрывая ярлыки.
- **Спокойствие в тишине.** Обои медленно «дышат», а не застывают чёрным экраном.
- **Бережёт ресурсы.** Ставится на паузу во время полноэкранных игр и само снижает разрешение, если тормозит.
- **Режим мягких вспышек** для чувствительных глаз.

### Установка

#### Lively Wallpaper (бесплатно, рекомендуется)

1. Установи [Lively Wallpaper](https://www.rocksdanister.com/lively/) из Microsoft Store.
2. Скачай `Mimi_Wallpaper.zip` из [Releases](../../releases).
3. Перетащи архив в окно Lively как есть, не распаковывая.
4. Нажми правой кнопкой на **Мими-обои** и выбери **Установить как обои**.

#### Wallpaper Engine

1. Распакуй архив в `steamapps\common\wallpaper_engine\projects\myprojects\Mimi`.
2. Перезапусти Wallpaper Engine, и обои появятся в библиотеке.

### Настройки

Их можно поменять в панели настройки обоев в Lively или Wallpaper Engine:

| Настройка | Что делает |
|---|---|
| Сцена | Одна сцена или автоматическая смена |
| Цвета | Одна палитра или автоматическая смена |
| Чувствительность к звуку | Подними, если обои еле реагируют |
| Скорость движения, длина шлейфа | Насколько быстрое и плавное движение |
| Яркость, свечение | Насколько яркие картинка и ореол |
| Качество картинки | Понизь, если ПК слабый или обои тормозят |
| Кадров в секунду | 30, 60 или без ограничения (только Lively) |
| Мягкие вспышки, зерно плёнки, название трека | Включаются и выключаются отдельно |

### Версия для браузера

`mimi_visualizer.html` — тот же визуализатор отдельной страницей. Открой его в Chrome или Edge и выбери источник звука: вкладку, весь компьютер, микрофон, аудиофайлы или демо-бит. Ещё он умеет:

- записывать видео со звуком (`R`) и сохранять кадр в PNG (`S`);
- играть плейлист из файлов, перетащенных в окно.

Все клавиши показываются по `?`.

### Если что-то не так

- **Не реагирует на звук.** Проверь, что звук идёт через устройство вывода Windows по умолчанию: Lively берёт его оттуда.
- **Нет названия трека.** Плеер должен поддерживать медиа-оверлей Windows, всплывашку при нажатии клавиш громкости. Chrome, Spotify и Яндекс Музыка его поддерживают.
- **Тормозит.** Понизь «Качество картинки» и поставь 30 кадров.
- **Поменял файлы, а ничего не изменилось.** Удали обои из библиотеки Lively и импортируй архив заново.

### Структура проекта

```
index.html              сам визуализатор (WebGL2, один файл)
LivelyInfo.json         манифест для Lively
LivelyProperties.json   настройки для Lively
project.json            манифест и настройки для Wallpaper Engine
thumbnail.jpg           миниатюра в библиотеке
preview.jpg             превью
```

### Как это работает

Каждый кадр прошлое изображение увеличивается, поворачивается и закручивается шумом, немного гаснет, а поверх рисуется новый свет. Из этой обратной связи появляются шлейфы и ощущение глубины. Свет дают лучи, кольцо спектра, тоннель, эквалайзер и звёзды. Дальше яркие места получают свечение (bloom), а тонмаппинг превращает результат в итоговую картинку. Lively и Wallpaper Engine передают странице спектр звука, а она ищет в нём доли по спектральному потоку с адаптивным порогом.

### Автор

**koliziym**
