<p align="center">
    <img src="https://github.com/jpjacobpadilla/Google-Colab-Selenium/blob/ecce30fd1f5f151e0c1d946259cf19de33aa8e9d/logo.png?raw=true">
</p>

<h3 align="left">The best way to use Selenium in Google Colab Notebooks!</h3>

- Selenium と ChromeDriver の簡単なセットアップ。
- Google Colab とのシームレスな統合。
- より高度なユースケース向けに、検出されない ChromeDriver をサポート。
<br>

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1MX3xY23Go1STe7LbDMvwf2KaqHpbrVhC?usp=sharing)

## インストール

基本版を使用するには:
```bash
%pip install google-colab-selenium
```

[undetected-chromedriver](https://github.com/ultrafunkamsterdam/undetected-chromedriver) 版を使用するには:
```bash
%pip install google-colab-selenium[undetected]
```


## 基本版での使い方
```python
import google_colab_selenium as gs

driver = gs.Chrome()
# Your code to interact with the driver here
# ...
driver.quit()
```

## 検出されない ChromeDriver版での使い方

```python
import google_colab_selenium as gs

driver = gs.UndetectedChrome()
# Your code to interact with the driver here
# ...
driver.quit()
```

## デフォルト・オプション

`google-colab-selenium` パッケージは、Google Colab 環境向けに最適化された一連のデフォルト・オプションで事前構成されています。次のものが含まれます:

- `--headless`: Runs Chrome in headless mode (without a GUI).
- `--no-sandbox`: Disables the Chrome sandboxing feature, necessary in the Colab environment.
- `--disable-dev-shm-usage`: Prevents issues with limited shared memory in Docker containers.
- `--lang=en`: Sets the language to English.

必要に応じて、これらのオプションを拡張または上書きすることができます:

```python
from selenium.webdriver.chrome.options import Options
import google_colab_selenium as gs

custom_options = Options()
# Add your custom options here

driver = gs.Chrome(options=custom_options)
```

## 貢献する
貢献を歓迎します! ご提案や問題がある場合は issue tracker を使用してお知らせください。
<br>
<br>

<div align="center">
<h3>ぜひご自身でお試しください!</h3>

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1MX3xY23Go1STe7LbDMvwf2KaqHpbrVhC?usp=sharing)
</div>
