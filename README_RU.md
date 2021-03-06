GAShell
 Скрипт bash, который генерирует и надежно управляет кодами Google Authenticator

 Techtonic Software 2019 - http://www.techtonicsoftware.com/

 Эта программа / сценарий лицензирована под GNU V3 (https://www.gnu.org/licenses/gpl-3.0.en.html) и поставляется без АБСОЛЮТНО ГАРАНТИИ.  Вы можете распространять, модифицировать и запускать его, однако вы не должны претендовать на него как на свое собственное или сублицензировать.

 Любой дистрибутив должен включать этот файл readme.

 Обратите внимание, что это был сценарий, который был сделан в мое свободное время, и хотя он прошел подстанционное тестирование, я рекомендую вам создать дополнительные резервные копии для ваших закрытых ключей Google Auth.  Я приветствую любые предложения по улучшению этого скрипта, особенно предложения по улучшению безопасности.  Я тестировал это только в Linux, но могу работать в других системах * nix или Linux.

 GAShell выступает в роли генератора и менеджера кода Google Authenticator, позволяя создавать, добавлять и удалять коды Google Authenticator внутри оболочки / терминала bash.  GAShell хранит ваши коды в вашей файловой системе, зашифрованные частной парольной фразой (которую вы установили самостоятельно) с помощью aes-256 в ~ / .config / gashell.  У него также есть возможность читать в Google Auth QR-коды либо через URL, либо через локальное изображение.

 Для использования этого скрипта вам потребуются следующие приложения / двоичные файлы: sed, oathtool, openssl, zbar, curl.  А также базовый набор системных команд * nix.

     Использование: ./gashell.sh args

     нет: Показать коды в цикле.
     -a: добавить новый ключ.
     -i: добавить новый ключ с помощью QR-кода (URL или путь к файлу).
     -r: удалить ключ.
     -o: выводить коды только один раз.
     -p: установить новый пароль.
     -h: Показать этот экран справки.

     Вы можете устранить необходимость ввода пароля в операциях вывода, указав его в следующей переменной: GASHELL_PASSPHRASE.  Обратите внимание, что этот скрипт автоматически получит пароль от этой переменной, если он определен.
