### Installation (全局安装，也可以项目级安装)
```
npm install -g commitizen
```

### init a package.json file.(如果是node项目，可以公用项目的package.json文件也行)
```
npm init --yes
```

### 初始化cz-conventional-changelog适配器（生成符合AngularJS规范的提交说明）
```
commitizen init cz-conventional-changelog --save-dev --save-exact
```

### 使用
```
git cz(代替git commit)
```
