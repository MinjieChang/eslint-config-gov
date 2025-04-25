# 使用方式

## 安装

```shell
npm install @bike/eslint-config-gov
```

## .eslintrc 中配置

```js
module.exports = {
  extends: ['@bike/eslint-config-gov'],
  rules: {
    'react-hooks/exhaustive-deps': 'off',
    '@typescript-eslint/no-empty-function': 'off',
    'no-restricted-imports': 'off',
    '@typescript-eslint/no-restricted-imports': [
      'warn',
      {
        name: 'react-redux',
        importNames: ['useSelector', 'useDispatch'],
        message: 'Use typed hooks `useAppDispatch` and `useAppSelector` form @/utils/hooks instead.',
      },
    ],
  },
}
```
