# Apuntes de kamitsui

* Top Page ... [Apuntes de kamitsui](https://kamitsui.github.io/Apuntes_de_kamitsui/)

* Blog
* Develop
* System
* Project ... [42_Cursus](https://kamitsui.github.io/Apuntes_de_kamitsui/projects/42_cursus)
* Engineer

### Build & Deploy

* Preview
```
npx quartz build --serve
```

* Using GitHub Actions locally
```
open -a docker
./deploy_test_github_arc.sh # Runs GitHub Actions workflow locally
# or
./deploy_test_github_arc.sh dry # Dry mode is only check workflow
```

* Deploy
```
npx quartz sync
```
note : commit -> push -> sync (Build ./public to github.io)
