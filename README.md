OpenMW 非公式日本語表示対応版
======

*※現状、リポジトリは準備中であり、OpenMW Ver.0.50のままです。今ダウンロードしても素のソースしかありません。*

概要
------
このリポジトリは [OpenMW](https://github.com/OpenMW/openmw) のフォークです。  
本プロジェクトは、本家OpenMWによる公式の配布物ではありません。

[OpenMW](https://github.com/OpenMW/openmw)は、有志による「The Elder Scrolls III: Morrowind」のゲームエンジンをC++で再実装するプロジェクトで、
最終的には汎用的なオープンワールドゲームエンジンとなることを目標としています。

本プロジェクトは本家OpenMWから派生し、
日本語表示対応を施したものです。
そのため、upstreamの最新の変更が反映されていない場合があります。

本家OpenMWでは、将来的に多言語サポートを行う旨が[1.0ロードマップ](https://gitlab.com/OpenMW/openmw/blob/master/docs/openmw-stage1.md)に記載があります。
本プロジェクトにおける実装は、上記ロードマップで想定される実装とは異なるものであり、互換性はおそらくありません。
本家OpenMWが日本語対応した暁には、本プロジェクトは時代遅れ（obsoleted）になり、不要になります。

本家OpenMW同様、「The Elder Scrolls III: Morrowind」本体のゲームデータが無いと遊べません。
MorrowindはSteam等で購入可能です。


サポート
------

本プロジェクトに関するサポートは現在受け付けておりません（ちょうどいい場所が無いため）。

そのうちなんとかします。

また、本プロジェクトに関するサポートを、本家OpenMWフォーラムやメーリングリストに投げる行為はご遠慮ください。

本プロジェクト固有でない問題については、本家OpenMWのFAQやフォーラムを参照ください。

FAQ
------
#### Q. 起動しても何も遊べません。

まず前提として、OpenMWは単一では「ゲームエンジン」であり、Morrowind本体の内容を含まず、それだけで遊ぶことはできません。
Morrowindを適切にインストール済の場合、公式と同様の手順に従ってセットアップすることで動く想定です。
詳しい手順についてはいずれ用意します（先延ばし癖）。

#### Q. 本家OpenMWとの違いは何ですか？

本家OpenMWとの一番の違いは、文字コードの扱いです。
本家OpenMWは、Morrowindのデータ(ESMファイル)を、

*ここで文章は途切れている* （書きかけです）

---

以下、本家の説明文ママ

OpenMW
======

OpenMW is an open-source open-world RPG game engine that supports playing Morrowind by Bethesda Softworks. You need to own the game for OpenMW to play Morrowind.

OpenMW also comes with OpenMW-CS, a replacement for Bethesda's Construction Set.

* Version: 0.50.0
* License: GPLv3 (see [LICENSE](https://gitlab.com/OpenMW/openmw/-/raw/master/LICENSE) for more information)
* Website: https://www.openmw.org
* IRC: #openmw on irc.libera.chat
* Discord: https://discord.gg/bWuqq2e


Font Licenses:
* DejaVuLGCSansMono.ttf: custom (see [files/data/fonts/DejaVuFontLicense.txt](https://gitlab.com/OpenMW/openmw/-/raw/master/files/data/fonts/DejaVuFontLicense.txt) for more information)
* DemonicLetters.ttf: SIL Open Font License (see [files/data/fonts/DemonicLettersFontLicense.txt](https://gitlab.com/OpenMW/openmw/-/raw/master/files/data/fonts/DemonicLettersFontLicense.txt) for more information)
* MysticCards.ttf: SIL Open Font License (see [files/data/fonts/MysticCardsFontLicense.txt](https://gitlab.com/OpenMW/openmw/-/raw/master/files/data/fonts/MysticCardsFontLicense.txt) for more information)

Current Status
--------------

The main quests in Morrowind, Tribunal and Bloodmoon are all completable. Some issues with side quests are to be expected (but rare). Check the [bug tracker](https://gitlab.com/OpenMW/openmw/-/issues/?milestone_title=openmw-1.0) for a list of issues we need to resolve before the "1.0" release. Even before the "1.0" release however, OpenMW boasts some new [features](https://wiki.openmw.org/index.php?title=Features), such as improved graphics and user interfaces.

Pre-existing modifications created for the original Morrowind engine can be hit-and-miss. The OpenMW script compiler performs more thorough error-checking than Morrowind does, meaning that a mod created for Morrowind may not necessarily run in OpenMW. Some mods also rely on quirky behaviour or engine bugs in order to work. We are considering such compatibility issues on a case-by-case basis - in some cases adding a workaround to OpenMW may be feasible, in other cases fixing the mod will be the only option. If you know of any mods that work or don't work, feel free to add them to the [Mod status](https://wiki.openmw.org/index.php?title=Mod_status) wiki page.

Getting Started
---------------

* [Official forums](https://forum.openmw.org/)
* [Installation instructions](https://openmw.readthedocs.io/en/latest/manuals/installation/index.html)
* [Build from source](https://wiki.openmw.org/index.php?title=Development_Environment_Setup)
* [Testing the game](https://wiki.openmw.org/index.php?title=Testing)
* [How to contribute](https://wiki.openmw.org/index.php?title=Contribution_Wanted)
* [Report a bug](https://gitlab.com/OpenMW/openmw/issues) - read the [guidelines](https://wiki.openmw.org/index.php?title=Bug_Reporting_Guidelines) before submitting your first bug!
* [Known issues](https://gitlab.com/OpenMW/openmw/issues?label_name%5B%5D=Bug)

The data path
-------------

The data path tells OpenMW where to find your Morrowind files. If you run the launcher, OpenMW should be able to pick up the location of these files on its own, if both Morrowind and OpenMW are installed properly (installing Morrowind under WINE is considered a proper install).

Command line options
--------------------

    Syntax: openmw <options>
    Allowed options:
      --help                                print help message
      --version                             print version information and quit
      --data arg (=data)                    set data directories (later directories
                                            have higher priority)
      --data-local arg                      set local data directory (highest
                                            priority)
      --fallback-archive arg (=fallback-archive)
                                            set fallback BSA archives (later
                                            archives have higher priority)
      --resources arg (=resources)          set resources directory
      --start arg                           set initial cell
      --content arg                         content file(s): esm/esp, or
                                            omwgame/omwaddon
      --no-sound [=arg(=1)] (=0)            disable all sounds
      --script-verbose [=arg(=1)] (=0)      verbose script output
      --script-all [=arg(=1)] (=0)          compile all scripts (excluding dialogue
                                            scripts) at startup
      --script-all-dialogue [=arg(=1)] (=0) compile all dialogue scripts at startup
      --script-console [=arg(=1)] (=0)      enable console-only script
                                            functionality
      --script-run arg                      select a file containing a list of
                                            console commands that is executed on
                                            startup
      --script-warn [=arg(=1)] (=1)         handling of warnings when compiling
                                            scripts
                                            0 - ignore warning
                                            1 - show warning but consider script as
                                            correctly compiled anyway
                                            2 - treat warnings as errors
      --load-savegame arg                   load a save game file on game startup
                                            (specify an absolute filename or a
                                            filename relative to the current
                                            working directory)
      --skip-menu [=arg(=1)] (=0)           skip main menu on game startup
      --new-game [=arg(=1)] (=0)            run new game sequence (ignored if
                                            skip-menu=0)
      --encoding arg (=win1252)             Character encoding used in OpenMW game
                                            messages:

                                            win1250 - Central and Eastern European
                                            such as Polish, Czech, Slovak,
                                            Hungarian, Slovene, Bosnian, Croatian,
                                            Serbian (Latin script), Romanian and
                                            Albanian languages

                                            win1251 - Cyrillic alphabet such as
                                            Russian, Bulgarian, Serbian Cyrillic
                                            and other languages

                                            win1252 - Western European (Latin)
                                            alphabet, used by default
      --fallback arg                        fallback values
      --no-grab                             Don't grab mouse cursor
      --export-fonts [=arg(=1)] (=0)        Export Morrowind .fnt fonts to PNG
                                            image and XML file in current directory
      --activate-dist arg (=-1)             activation distance override
      --random-seed arg (=<impl defined>)   seed value for random number generator
