### ｽﾀｯｸﾁｬﾝについて ###
- M5StackCoreS3にRobitsサーボを組み合わせて作られています。
- バッテリは、背中に背負っています。
- M5StacKCores3はPCと繋がったUSBケーブルを接続すると起動しますが、起動しない場合は、電源ボタンを押すと電源が入ります。
- M5stackCores3の電源を落とすには、電源ボタンを6秒以上押し続ける必要があります。
- バッテリの充電は、M5StackCores3の電源をOFF、スライドスイッチをOnにし、USBケーブルから充電することができます。充電中はリセット端子の近くから赤い光が漏れます。充電が終わると赤い光は消灯します。
- リセットボタンを3秒以上押し続けるとリセットボタンのところから緑の光が見えます。緑の光が見えた時は、プログラム書き込みモードになります。プログラムの書き込み時に書けない時書き込みモードにすると書き込みすることができます。
- 開発していると記述が正しいはずなのにプログラムが意図しない動作をすることがあります。その時は、Flashをeraseすることで解決することがあります。eraseするとWindowsのWLS2ではｽﾀｯｸﾁｬﾝをusbipdで認識できないためプログラム書き込みモードにする必要があります。
    - eraseコマンド
        - idfのパージョン(idf5.3)とpythonのバージョン(py3.12_env)はインストールしたバージョンにあわせてください。
            - ubuntu
                - /home/ubuntu/.espressif/python_env/idf5.3_py3.12_env/bin/esptool.py erase_flash
            - windows11(WLS2)
                - /home/ubuntu/.espressif/python_env/idf5.3_py3.10_env/bin/esptool.py erase_flash
            - macOS
                - /Users/ユーザ名/.espressif/python_env/idf5.3_py3.12_env/bin/esptool.py erase_flash 