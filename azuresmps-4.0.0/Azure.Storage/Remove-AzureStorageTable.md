---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 1B29AB8C-95DD-4C4F-86E2-2F81E8020CEA
online version: ''
schema: 2.0.0
ms.openlocfilehash: fcb08eb9e63917d072630f81a2026d961a70dd27
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93761712"
---
# Remove-AzureStorageTable

## SYNOPSIS
Depolama tablosunu kaldırır.

## INDEKI

```
Remove-AzureStorageTable [-Name] <String> [-Force] [-PassThru] [-Context <IStorageContext>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## Tanım
**Remove-AzureStorageTable** cmdlet 'ı, Azure 'daki depolama hesabından bir veya daha fazla depolama tablosunu kaldırır.

## ÖRNEKLERDEN

### Örnek 1: tablo kaldırma
```
PS C:\>Remove-AzureStorageTable -Name "TableABC"
```

Bu komut tabloyu kaldırır.

### Örnek 2: birkaç tabloyu kaldırma
```
PS C:\>Get-AzureStorageTable table* | Remove-AzureStorageTable
```

Bu örnekte, desen tablosuyla eşleşen tüm tabloları almak için *Name* parametresiyle birlikte joker karakter kullanılır ve ardından tabloları kaldırmak için sonucu ardışık düzene geçirir.

## PARAMETRELERINE

### -Context
Azure depolama bağlamını belirtir.
Bunu, New-AzureStorageContext cmdlet 'ini kullanarak oluşturabilirsiniz.

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Force
Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Ad
Kaldırılacak tablonun adını belirtir.

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Table

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Geçiş
Bu cmdlet 'in işlemin başarısını yansıtan bir **Boole değeri** döndürdüğü anlamına gelir.
Varsayılan olarak, bu cmdlet değer döndürmez.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Onay
Cmdlet 'i çalıştırmadan önce onaylamanızı ister.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Cmdlet çalışırsa ne olacağını gösterir.
Cmdlet çalışmaz.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

## ÇıKıŞLAR

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-AzureStorageTable](./Get-AzureStorageTable.md)
