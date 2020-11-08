---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 0DF54C9D-7A19-4591-A1FC-33C6A4C9BF33
online version: ''
schema: 2.0.0
ms.openlocfilehash: 05a99e1a4965329c0eeb29fe0e014814fd1807b2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105937"
---
# Test-AzureName

## SYNOPSIS
Microsoft Azure bulut hizmeti adı, depolama hizmeti adı veya hizmet veri yolu ad alanı adı olup olmadığını sınar.

## INDEKI

### Hizmetinin
```
Test-AzureName [-Service] -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### Alanını
```
Test-AzureName [-Storage] -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ServiceBusNamespace
```
Test-AzureName [-ServiceBusNamespace] -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### Web sitesi
```
Test-AzureName [-Website] -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Tanım
Ad varsa, cmdlet $True döndürür.
Ad yoksa $False döndürür.

## ÖRNEKLERDEN

### Örnek 1
```
PS C:\> Test-AzureName -Service "MyNameService1"
```

Bu komut, "MyNameService1" nin varolan bir Microsoft Azure bulut hizmeti adı olup olmadığını sınar.

### Örnek 2
```
PS C:\> Test-AzureName -Storage "mystorename1"
```

Bu komut, "mystorename1" nin varolan bir Microsoft Azure depolama hizmeti adı olup olmadığını sınar.

### Örnek 3
```
PS C:\> Test-AzureName -ServiceBusNamespace "mynamespace"
```

Bu komut, "MyNameSpace" nin varolan bir Microsoft Azure Service Bus ad alanı adı olup olmadığını sınar.

## PARAMETRELERINE

### -Ad
Sınanacak hizmetin adını veya depolama hesabını belirtir.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Profil
Bu cmdlet 'in okuduğu Azure profilini belirtir.
Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Hizmet
Var olan hizmet hesabını sınaytkullanılacağını belirtir.

```yaml
Type: SwitchParameter
Parameter Sets: Service
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServiceBusNamespace
Var olan bir hizmet veri yolu ad boşluğunu sınamanızı belirtir.

```yaml
Type: SwitchParameter
Parameter Sets: ServiceBusNamespace
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Depolama
Var olan bir depolama hesabını sınaykullanılacağını belirtir.

```yaml
Type: SwitchParameter
Parameter Sets: Storage
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Web sitesi
Var olan bir Web sitesinin test edileceği belirtir.

```yaml
Type: SwitchParameter
Parameter Sets: Website
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

## ÇıKıŞLAR

## NOTLARıNDA
* düğüm-dev, php-dev, Python-dev

## ILGILI BAĞLANTıLAR

