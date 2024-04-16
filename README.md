# 📝 FuncaptchaServer

> 📝 Based on🔗 [MagicalMadoka/funcaptcha-challenger](https://github.com/MagicalMadoka/funcaptcha-challenger) Image recognition server

## Sponsors

### [Capsolver](https://capsolver.com?utm_source=github&utm_medium=banner_github&utm_campaign=funcaptcha-server)

[![capsolver](https://github.com/MrDgbot/funcaptcha-server/assets/60038945/6b1ea84b-5469-42d9-9167-c575de1b1749)](https://capsolver.com/?utm_source=github&utm_medium=banner_github&utm_campaign=funcaptcha-server)


[Capsolver.com](https://www.capsolver.com/?utm_source=github&utm_medium=banner_github&utm_campaign=funcaptcha-server) is an AI-powered service that specializes in solving various types of captchas automatically. It supports captchas such as [reCAPTCHA V2](https://docs.capsolver.com/guide/captcha/ReCaptchaV2.html?utm_source=github&utm_medium=banner_github&utm_campaign=funcaptcha-server), [reCAPTCHA V3](https://docs.capsolver.com/guide/captcha/ReCaptchaV3.html?utm_source=github&utm_medium=banner_github&utm_campaign=funcaptcha-server), [hCaptcha](https://docs.capsolver.com/guide/captcha/HCaptcha.html?utm_source=github&utm_medium=banner_github&utm_campaign=funcaptcha-server), [FunCaptcha](https://docs.capsolver.com/guide/captcha/FunCaptcha.html?utm_source=github&utm_medium=banner_github&utm_campaign=funcaptcha-server), [DataDome](https://docs.capsolver.com/guide/captcha/DataDome.html?utm_source=github&utm_medium=banner_github&utm_campaign=funcaptcha-server), [AWS Captcha](https://docs.capsolver.com/guide/captcha/awsWaf.html?utm_source=github&utm_medium=banner_github&utm_campaign=funcaptcha-server), [Geetest](https://docs.capsolver.com/guide/captcha/Geetest.html?utm_source=github&utm_medium=banner_github&utm_campaign=funcaptcha-server), and Cloudflare [Captcha](https://docs.capsolver.com/guide/antibots/cloudflare_turnstile.html?utm_source=github&utm_medium=banner_github&utm_campaign=funcaptcha-server) / [Challenge 5s](https://docs.capsolver.com/guide/antibots/cloudflare_challenge.html?utm_source=github&utm_medium=banner_github&utm_campaign=funcaptcha-server), [Imperva / Incapsula](https://docs.capsolver.com/guide/antibots/imperva.html?utm_source=github&utm_medium=banner_github&utm_campaign=funcaptcha-server), among others.

For developers, Capsolver offers API integration options detailed in their [documentation](https://docs.capsolver.com/?utm_source=github&utm_medium=banner_github&utm_campaign=funcaptcha-server), facilitating the integration of captcha solving into applications. They also provide browser extensions for [Chrome](https://chromewebstore.google.com/detail/captcha-solver-auto-captc/pgojnojmmhpofjgdmaebadhbocahppod) and [Firefox](https://addons.mozilla.org/es/firefox/addon/capsolver-captcha-solver/), making it easy to use their service directly within a browser. Different pricing packages are available to accommodate varying needs, ensuring flexibility for users.

## 🔍️ **Supported models**
-  SUPPORTED MODELS:

|                         |                         |                         |                         |
|-------------------------|-------------------------|-------------------------|-------------------------|
| animal_rotation_towards_hand | match_count_similarity | match_count_target_detection | match_count_source_detection |
| hopscotch_highsec        | icon_connect            | 3d_rollball_objects     | 3d_rollball_objects_v2  |
| numericalmatch_target_detection | numericalmatch_similarity | coordinatesmatch         | penguin                 |
| shadows                 | dice_pair               | train_coordinates       | numericalmatch          |
| dicematch               | hand_number_puzzle      | penguins                | frankenhead             |
| BrokenJigsawbrokenjigsaw_swap | counting                | knotsCrossesCircle      | orbit_match_game        |


- https://github.com/MagicalMadoka/funcaptcha-challenger/releases/download/model/version.json
- http://Deployed API port/support

- Funcaptcha Other types welcome PR.

## 🐅 Project Introduction

### ⬇️ **Deployment-related**

- **📡 Installation dependency**:

```bash
pip install -r requirements.txt
```

- **📡 Run**:

```bash
python main.py
```

## 🖼️ Example of use

- **📡 Example curl command**:

```bash
curl --location --request POST 'http://127.0.0.1:8181/createTask' \
--header 'Content-Type: application/json' \
--data-raw '{
    "clientKey": "your_key",
    "task": {
        "type": "FunCaptchaClassification",
        "image": "data:image/jpeg;base64,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pTk5cyOylWgockjGjsbuUgJbSHP+yRW1p2gbGEt5gkciMcj8a2EAHQBR6DoKkroucT3DpRRRQIKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKAKl9ptvfpiVcOOjjqKwLjw5eRE+VtmXtg4P611VFMLnGDSNQzj7K/6VINE1HGfs/8A48P8a6+ii4XOEmhlt5DHKhRh2IqI12uoafFqEGyQYYfdcdRXI3tlPYzGOZMejDo1Mdy5YahbeYFv4I3PQSlQSPr611MewoGQgqRwR0xXA5rR0zWZbBgjZkgPVfT6UrAdhRUVtcw3cIlhcMp/SpaQhaKSloAKKKKACiiigAoopKAFopKKAFopKKAFopKKAFopKKAFopKKAFopKKAFopKKAFopKKAFopKKAFooooAKKKKACiiigAopKKAFopKKADFUNas3vNOaOJA8gIKir9FAHJ2fh27nOZ/3C+/JP4VvWOkWljhkTfJ/fbk//Wq9RTuAUtJRSAWikooAWikooAWikooAWikooAWikooAWikooAWiiigAoopKAFopKKAFopKKAFopKKAFopKKAFpKKKAIpoVmQqcjPcdRVb+zIyxLs7bm3tljy3r9avUUWGpNbDFQL0pzIrjDKGHuM0tFAgpaSigBaKSigBaKSigBaKSloAKKKKACiiigAopKKAFopKKAFopKKAFopKKAFopKKAFopKKAFopKKAFopKKAFopKKAFopKKAFooooAKKKKACkpawPEWrG3X7HA2JGHzsP4R6UAM13WgoNpavyeJHHb2Fc5mmZpyAuwVQSxOAB3qhksMck8qxRqWdjgAV2OlaVHp8IJw0zD5m9PYVHo2krYQiSQAzuOT/AHfatSkITFJgU6ikAmKWiigAoopKAFopKKAFopKKAFopKKAFoopKAFopKWgAooooAKKSigBaKSigBaKSigBaKSigBaKSloAKKSigBaiuLaK6iMUyB1Pr2qSigDjtU0ebT2LqDJB2f0+tZlehsqupVgCp4IPeuX1fw/JCzT2al4zyUHVfp6incLmZZahcWEu+F8A/eU9GrrtM1WHUosr8ki/eQnp9PauHPBwaktrmW1nWaJtrKfzp2GehUtQWlwt3axzp0dc49KnqRBRRRQAUlFFMQUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABS0lFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFAC0lFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFLSUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUALRRSUALSUUUgCvPb+Zp7+eRjyzn+dehVkr4b08TNK6vIWYthm4H5UxnI29tNdSiOCNnY9gOldZo+hJY4nnw8/b0X6VqQ28NumyGJY19FGKkoC4UUUUhBRRRQAUUUUAFFFFMAooooAKKKKACiiigAooooAKWkooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKQBRRRTAKKKKAKF7otlfEs8eyQ/wAacH/69Y83hOUHMFyrD0cY/lXT0UAUNGs57GwEE5UsrEjacjFX6KKACiiigAooooAKKKKACiiigAoopKAFopKKAFopKKAFoopKAFopKKAFopKKAFopKKAFopKWgAopKWgAooooAKKKKACiiigAooooAKKSigBaKSigBaKSloAKKSigBaKSigBaKSigBaKSigBaKKSgBaKKKACiiigAooooAKKKKACiikoAWikooAWikooAWiikoAWikooAWikooAWikooAWikpaACikpaACiiigAooooAKKKKACiiigAoopKAFopKKAFopKWgAopKKAFopKKAFopKKAFopKKAFoopKAFooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiikoAWiiigAopKWgAopKWgAopKWgAooooAKKKKACiiigAooooAKKKSgBaKKSgBaKSloAKKSigBaKSloAKKKKACiiigAooooAKKKKAEyPUUZHqPzryfJ9B+dAYg9P1p2A9YyPUUZHqK8oLEnOP1pMn0/WiwHrGR6ijI9RXlG47cY/WkyfT9aLAesZHqKMj1FeUAkHOKCSSTj9aLAer5HqKMj1FeUrg9TinYX+8fyp2EeqZHqKMj1FeVhVJwCfypmT6D86Vhnq+R6j86Mj1FeUZPp+tLk+n60WA9WyPUUZHqK8rByuDxzQFUnGT+VFgseqZHqKMj1FeUSY8puf4TVGgR7LkeooyPUV41RSA9lyPUUZHqK8aooA9lyPUUZHqK8aooA9lyPUUZHqK8aooA9lyPUfnRkeorxqigD2XI9RRkeorxqigD2XI9RRkeorxqigD2XI9RRkeorxqigD2XI9RRkeorxqigD2XI9RRkeo/OvGqKAPZcj1FGR6ivGqKAPZcj1FGR6ivGqKAPZcj1FGR6ivGqKAPZcj1FGR6ivGqKAPZcj1FGR6ivGqKAPZcj1FGR6ivGqKAPZcj1FGR6j868aooA9lyPUUZHqK8aooA9lyPUUZHqK8aooA9lyPUUZHqK8aooA9lyPUUZHqK8aooA9lyPUUZHqK8aooA9lyPUfnRkeorxqigD2XI9RRkeorxqigD2XI9RRkeorxqigD2XI9RRkeorxqigD2XI9RRkeorxqigD2XI9RRkeorxqigD2XI9RRkeorxqigD2XI9R+dGR6ivGqKAPZcj1FGR6ivGqKAPZcj1FGR6ivGqKAPZcj1FGR6ivGqKAPZcj1FGR6ivGqKAPZcj1FGR6j868aooA9lyPUUZHqK8aooA9lyPUUZHqK8aooA9lyPUUZHqK8aooA9lyPUUZHqK8aooA9lyPUUZHqK8aooA9lyPUUZHqK8aooA9lyPUUZHqK8aooA9lyPUUZHqK8aooA9lyPUUZHqK8aooA9lyPUUZHqK8aooA9lyPUUZHqK8aooA9lyPUUZHqK8aooA9lyPUUZHqK8aooA9lyPUUZHqK8aooA9lyPUUZHqK8aooA9lyPUUZHqK8aooA9lyPUUZHqK8aooA9lyPUUZHqK8aooA9lyPUUZHqK8aooA9lyPUfnRkeorxqigD2XI9RRkeorxqigD2XI9RRkeorxqigD2XI9RRkeorxqigD2XI9RRkeorxqigD2XI9RRkeorxqigD2XI9RRkeorxqigD2XI9RRkeorxqigD2XI9RRkeorxqigD2XI9RRkeorxqigD2XI9RRkeorxqigD2XI9RRkeorxqigC/hfU0oVScZNR5PtTgSCDxVjFwvqaML6mj5fekYYxjuO9ACkLjIzScUmTjHFHPekAvPtRz7U75fQ0fL70wG8+1GT7U4hQAeeaQ4/hz+NIAUkEHApcL703n2p/wAvoaYDSCGI9KTn2p5Kkk880hAwCM/jSARevzfpTwVBB54qPntRlvamAsgXyn6/dNUKuyZ8pun3TVKpYBRRRSEFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQBe+XHAOfrSc+35UKeeeRTsr6H86sY3n1FOyCBuHT0oyvofzpH4PHTFACkLgEA0nFJkkYoHWkAc+oo59RTvl9D+dL8vofzpgNyxAGRx7UuDtznnNLlc9D+dLlcYwfzoAj59R+VL83qPyp3y46H86X5fQ/nQAzn1FLk4wad8vofzowu3OD19aAGjGead8vofzpDjsMH60nPr+lADZM+W30NUquyghHGex7VSqWDCiiikIKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigC5zRk+tO+XPT9aX5f7p/OrGN59f0p2QfvDJoyv90/nRlf7v60AJ8vofzpTt7A5+tHy/wB0/nSjaex6etADOfX9Kflf7p/Okyv90/nTefX9KAHH24pOc9f0pOfUflS4Pr+lABg+v6UvPr+lABJHP6UmDnr+lADmBDEA8UA4GDyKXcD1GT9aQgFMjg5pDDK8cfrS5X+6fzpmD6/pRz6/pTELKQY3OOcHvVCrj58tuexqnUsGFFFFIQUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFAFzn1o59RRRVDF59aOfX9KTJ9RTgVxyDmmAEEAc9aQFh3H5U4lTjg8e9ACnsfzpAN59f0p2V9D+dHy+h/OmfN6j8qYDj/ALPH1rvfB3ga1v7FNQ1ZWkWXmKJWKjb6nHPNc74Q0Q63rSJMpa2h+eXC9fQfjXsUsiWlrlEBYjbGo9e1cterbRG9KnfVnGReANOHiiUjc2nQorCJmJy56qT1wOD+NN+Imh6TYaDBc2tpDa3HnhF8pAu8YOQcfTNdzaxiNPn4PVi3GfevIfG/iJtd1p0hkzZWzFIQOh9W/Ej8qxpuc5pX2NZqMYtnNgk9x+VOBIBB5FN59aUHkZ5rvOMcNpzwenrSU4FR2P50fL6H86YEcn+rb6GqVXpgBG2O61RqWAUUUUhBRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAXvl96UBcE88UzJ9qUE4IwOaoYvy+9Jz26UmT7U4be+aYCHIx0oBIPPSnHafWkIGDjOfekAvy+9Otra5vLlLa2jMs0hwiDqTUcaSyyrHGm93ICqOpNeseFvB1npdtHcXCGS+YZaQMRs9his6lRQRcIczNLwto0Gg6QkGQJSN8zkYJbv+FW7RGuL6S7kjkQPhYlJ4x/ex2J/oKdcWc7xhEmWRAwOyZc5x2DDkfrUn2426Hz4WiPQH7yfmOg+uK89tt3Z2paWRy3xI1+K00+LS7d83M3zs6Ngxp9R69PpmvLuPevQPEHw9uZxPqllfi5dyZDCw5Yk5whH6D9a4S4tZrOUxXUEsEg/hkQqfrzXXh1FRsnqc9bmb8iIjB4pKd8p7mlCqQTk8V0nONyw9KXn2oIXHU0mT7UwFkOYmz1CnpVCrzYMT564NUalgwooopCCiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAvYX+8fypdq4zuP5UzPtS7vlxjvVjFwv94/lS4X+9+lNBJPSkyc9KAH4X+8fyo+X1P5U0sT/CaQk4+6aAOx8BaKJ7s6lKuUjO2LI79z/T869Pj4Wuf8LwJDpFrGgwFiX8SRkmugWvOnLmlc7YxsrEgNOBqMU9RmouUNlsbaSffa+ZAeuQR175HQ/lXD/Em/36Rb2rQxbvtBUykckqOSvoORn8q7+4litLV58nCJuO7jnFeS/EW9D6tbWCusgtIsuynq7cnP5D86mm+askip+7SbZyLAqRjnIzQGIzx1HrS5DAc4wMUbR/eFeqecNyR2p+F9T+VJtGPvCkyfSgBJOI3xzkGqVXHP7thg9DVOkwCiiikIKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigC4eOOv0ozxnBoyKXcNvXvVjEDcjg0bvY0m4UbhSAXPsaTOcjn8aCwzWt4a0mXV9WhUWzzW8bhpyo4A9D9aTaSuxpXdkejeG7+2TSbYtMoBjUbj0zjpnpmujR1YZBBB9KZC0IjEIQKoGAhXHH0qP+y4c5tXNq3X5D8p/wCAnj+teY730PQTXUtqM1YVQgyao280kEpiuwm5V3B14Vh6+1cR40+IAIk07RZMk5WS4U8D2U/1rH3qkuSJo1GC5pbGr4o8badaJPawSrPPFx5YGQX7Z7YHU15S8jTSvI77mZiSxPJNQc855J5JqRFJUGvSoUI0lpucNWs6mnQUDPccU4L7ikCkE8Uu0+ldJgGw+o/Omk4OMHilDDPWhuWJHrSAY5+RuD92qdXXH7tv901SpMQUUUUgCiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAuMRnr2oAJ6DNJSjiqGG0+h/Kl2n0NJk+tGT60ASQW811cR28CF5ZWCqo7mvaPDmiQ6FpUdrGAZPvSvj7zdzXD/Deyil1G5vZAGeBQqZ7Z6n9K9LVxXDXqpy5L7HZSpNR5u45kVxh1DD0IzTTG8CmWHcwQZZCev0NSxo0jBVBYnsKxfGuvL4f0CTy2H2q5BjhHcerfhWEr7Ldmsbbs4bx/4qXVNRjttNun+zxRlZGjYgSEnOPcDH6muLpKcv8Aq2/CvQp01TjZHFObnK7EqRCAo5pi9afWpmOyPWlQjd17UwdTS0xi7T6GjafQ0ZPrQpO0c0CGyKdjcH7pqlV6Qny257GqNSxBRRRSAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigC8zEMeaTe3rRu9h+VG72H5VYw3H1pdzetJu9h+VLu9h+VAF7R9bvdDvftNo4+YYkRhlXHvXf6V8Q9LvAqXoayl6Evymf94f1xXl8nDECo/auWthqdXV7m9OvOnotj3lNZ0+O1N59tgMAG4uJARivIfFfiCTxHrUl1yIE+SBD2X1+p61iYp1TRwypO7dyquIdRWSsBHyKfrSU7tinKAVY46V1HMIFGKerEKOaM+wpP0pgO3H1pyMSwBNMI+UHJoGQcgmgBMD0owPSnbvYUKeOgoAY4Hlt9DVOr0h/dPwOhqjSYBRRRSEFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQBbOQaMmk6mnAAjk/pVDEyaMn1pcL/eP5UELg8n8qAIySSSe9A60uB60YFAg4oopQM0DFI+VSOpzSgkAjjmnDBUA8Yo2jaSD0oGN59acpGORTaBkdqBEmRjGP1oUKSBg8+9MyfSlDEEHHT3oAd8vofzpPpwKQsSen60Bj6UwBhmN8n+E1Rq6zERvx/Cf5VSqWDCiiikIKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigC5tPqPzpOnFLtb0NG0+hqhiZoJ4pdp9DSMrY6GgBlLjjNG0+hp2D5Z470AMqQECmqjdcGnbT6H8qAFBpynII9aZjB54pRz0pgLtPqPzo2EdSPzo2n0NOcHI4PQUAN2n1H50bD6j86Np9D+VKAc9DQA0jBwaAcU51O88HrTcEdRSARz+7b6GqdXH/wBW30NU6TEFFFFIAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKALmT60rk7zzTaXcfb8qoYZPrRk+tLnKNkCm4oAXrSbfeigdaYEidfwNNyfWgcHIpdx9B+VACUdxStyqn+VNxQA7J9aMn1pv50D6mgCTJ8vr3puT60nbGTRigYuT605vur+NI4Ac0gJAx/OkA1/9W30NU6uyN+7bp0PaqVJkhRRRSAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKACiiigD//2Q==",
        "question": "3d_rollball_objects"
    }
}'
```

- **📡 Response Example**:

```json
 {
  "errorCode": "",
  "errorId": 0,
  "solution": {
    "objects": [
      4
    ]
  },
  "status": "ready",
  "taskId": "bb11d056130b5e41f3d870edfa21c6a4"
}
```

- **📡 Identification instructions**:

> errorId: 0 Recognition successful.\
> objects: Corresponding recognition results\
> *Counting from 0，`"objects": [4]` The recognition result is identified as sequence 4, corresponding to the finger.

# 📝  Contact me:
youngjimmy8305@gmail.com
