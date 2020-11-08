---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 482E8CD6-C38F-4BD5-8214-016D0D8C7FD0
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6381b8e0fac5ebf047122f131af6087d5bb5a9fb
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105554"
---
# Get-AzureStorSimpleResource

## SYNOPSIS
Oluşturduğunuz tüm kaynakları alır.

## INDEKI

```
Get-AzureStorSimpleResource [-ResourceName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Tanım
**Get-AzureStorSimpleResource** cmdlet 'ı, Azure Portal kullanarak oluşturduğunuz tüm kaynakları alır.
Cmdlet, kaynaklara bağlanmak için kullanabileceğiniz ayrıntıları alır.

## ÖRNEKLERDEN

### Örnek 1: tüm kaynakları alma
```
PS C:\>Get-AzureStorSimpleResource
VERBOSE: ClientRequestId: 5cd61b91-ef40-43b4-986d-156e06d2ed65_PS

ResourceName                                      ResourceId           ResourceState
------------                                      ----------           -------------
Contoso63-Tsqa                                    8838459798595306468  Started
Contoso68-Tsqa                                    2859070203638134681  Started
Contoso73-Tsqa                                    7871392677286863733  Started
Contoso87-Tsqa                                    1909806764156522689  Started
VERBOSE: Found 4 StorSimple resources.
```

Bu komut, oluşturduğunuz tüm kaynakları alır.
Bu örnekte üç kaynak vardır.

### Örnek 2: adını kullanarak bir kaynak alma
```
PS C:\>Get-AzureStorSimpleResource -ResourceName "Contoso63-Tsqa"
VERBOSE: ClientRequestId: efc3c85c-12aa-4345-b6eb-ccc532de4825_PS

ResourceName                                      ResourceId           ResourceState
------------                                      ----------           -------------
Contoso63-Tsqa                                    1909806764156522689  Started
VERBOSE: Found 1 StorSimple resource.
```

Bu komut, Contoso63-Tsqa adlı kaynağı alır.

### Örnek 3: varolmayan bir kaynağı edinme girişimi
```
PS C:\>Get-AzureStorSimpleResource -ResourceName "Contoso64-Tsqa"
VERBOSE: ClientRequestId: 5d08d40b-f9d7-4d43-956f-13f01e89625b_PS
VERBOSE: Invalid input : Could not find a resource named Contoso64-Tsqa in your subscription.
```

Bu komut, Contoso64-Tsqa adlı kaynağı almayı dener.
Bu ada sahip bir kaynak yok.
Bu örnek herhangi bir kaynak döndürmez.

## PARAMETRELERINE

### -Profil
Bir Azure profili belirtir.

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

### -ResourceName
Bu cmdlet 'in aldığı kaynağın adını belirtir.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### Yabilirsiniz

## ÇıKıŞLAR

### IEnumerable \<ResourceCredentials\> , ResourceCredentials
Bu cmdlet, aşağıdaki özellikleri içeren **ResourceCredentials** nesnelerini döndürür: 

- **Kaynak**
- **Kaynak kimliği**
- **ResourceState**

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-AzureStorSimpleResourceContext](./Get-AzureStorSimpleResourceContext.md)

[Select-AzureStorSimpleResource](./Select-AzureStorSimpleResource.md)


