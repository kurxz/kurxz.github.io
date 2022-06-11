---
title: "Remover Bloatware de celulares"
date: 2022-06-11
description: "Como remover os aplicativos que não são possiveis desinstalar do seu celular"
type: post
weight: 25
showTableOfContents: true
---

## O que é isso?
Como forçar a desinstalção de aplicativos android
Os Bloatwares que vem junto com seu celular e nativamente não é possivel desinstalalos

## O que preciso?
Primeiramente você vai precisar do seu cabo usb e o ABD tools recomenda-se a utilização de linux para isso 

## Como faço?
Após isso ativar as configurações de Desenvolvedor no seu celular ( Isso vária de celular para celular então pesquise de acordo com o seu modelo )\
Então procure por depuração usb e a habliite-a
Então no seu terminal do linux digite ``` adb devices ``` para forçar a abertura de um novo servidor adb\
( Se já tiver um aberto digite ``` sudo killall adb ``` )

Seu dispositivo deve aparecer 1 notificação para permitir o uso do computador
Após confirmar seu dispositivo deverá aparecer no adb devices

Se tudo estiver correto digite, ```adb shell```. Seu diretorio base deve mudar \
Para algo como: **spes:/ $**

## Como sei o nome do app?
Então você descobrir o nome do app você ira digitar: 
```pm list packages | grep 'Nome do Desenvolvedor ou Pesquisa'```

**Nome do Desenvolvedor?** aqui vai alguns exemplos 
```
com.google.android.apps.youtube.music
com.google.android.apps.photos
com.android.chrome
com.google.android.apps.subscriptions.red
com.miui.videoplayer
```

Para o campo desenvolvedor pode ser: xiaomi, google, samsumg\
E ele irá listar pacotes que possuem o nome do desenvolvedor\

Ou você pode procurar por termos

Exemplos: 
```
pm list packages | grep 'com.google' 
pm list packages | grep 'video' 
```

## Desinstalando...
Então finalmente para desinsntalar você digita 

pm uninstall -k --user 0 **Nome.do.pacote**

Por exemplo: 
```
pm uninstall -k --user 0 com.android.chrome
```

Pronto seu aplicativo será desinstalado logo em seguida

## A Play store..
No entanto a Play Store **poderá reinstalar** o aplicativo.\
**Se** por acaso o aplicativo for reinstalado pela play store **ele poderá mostrar a função desinsntalar**. A que antes não era possível, então basta desisntalar normalmente.

## Fim
Após um pouco de sofrência os aplicativos não estarão mais no seu celular

 