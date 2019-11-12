---
title: How to install React Native with Typescript without React Native CLI
description: I'll show how to install React Native with Typescript without React Native CLI
date: '2019-11-12 08:36:34'
image: /assets/img/react-native-header.png
category: mobile
background: '#03A9F4'
---
When you need install some dependence in your project you can use:

```
npx --ignore-existing ....
```

Its allow you get the new version from npm package without look for your node_modules/bin that was installed in your operational system.

I was trouble with that when I attempt install React Native with Typescript! 

I tried:

```
npm uninstall -g react-native-cli
```

and this:

```
yarn global add @react-native-community/cli
```

And nothing worked for me, then I saw this answer:
<https://github.com/react-native-community/react-native-template-typescript/issues/80#issuecomment-536419979>

So, I googled about `npx --ignore-existing `

and I got this:

> \--ignore-existing - If this flag is set, npx will not look in $PATH , or in the current package's node_modules/.bin for an existing version before deciding whether to install. Binaries in those paths will still be available for execution, but will be shadowed by any packages requested by this install.
>
> \
>
>
> from: https://www.npmjs.com/package/npx

Then, I tried:

```
npx --ignore-existing react-native init MyApp --template react-native-template-typescript
```

And it works \o/! But it expend more time, because it grab all content in the Internet, doesn't look for your cache files.



credit: [Image](https://medium.com/reactbrasil/quais-desafios-vou-enfrentar-ao-come%C3%A7ar-um-app-com-react-native-a456db89c081)