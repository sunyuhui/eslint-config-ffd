### 标准规则

安装：


    npm install --save-dev eslint babel-eslint eslint-config-ffd


在项目根目录下创建 `.eslintrc.js`，并将以下内容复制到文件中：


    module.exports = {
        extends: [
            'eslint-config-ffd',
        ],
        globals: {
            // 这里填入你的项目需要的全局变量
            // 这里值为 false 表示这个全局变量不允许被重新赋值，比如：
            //
            // jQuery: false,
            // $: false
        },
        rules: {
            // 这里填入你的项目需要的个性化配置，比如：
            //
            // // @fixable 一个缩进必须用两个空格替代
            // 'indent': [
            //     'error',
            //     2,
            //     {
            //         SwitchCase: 1,
            //         flatTernaryExpressions: true
            //     }
            // ]
        }
    };


使用：


    eslint ./ --ext .js


备注：具体写法请以项目为准

### Vue

安装:


    npm install --save-dev eslint vue-eslint-parser@2.0.1-beta.2 eslint-plugin-vue@3 eslint-config-ffd


在项目根目录下创建 `.eslintrc.js`，并将以下内容复制到文件中：


    module.exports = {
        extends: [
            'eslint-config-ffd/vue',
        ],
        globals: {
            // 这里填入你的项目需要的全局变量
            // 这里值为 false 表示这个全局变量不允许被重新赋值，比如：
            //
            // Vue: false
        },
        rules: {
            // 这里填入你的项目需要的个性化配置，比如：
            //
            // // @fixable 一个缩进必须用两个空格替代
            // 'indent': [
            //     'error',
            //     2,
            //     {
            //         SwitchCase: 1,
            //         flatTernaryExpressions: true
            //     }
            // ]
        }
    };


### 使用


    eslint ./ --ext .js  --ext .vue


备注：具体写法请以项目为准


### 致谢

本规则参考了 [eslint-config-alloy](https://github.com/AlloyTeam/eslint-config-alloy)，根据团队实际情况做了一些调整。

感谢 AlloyTeam