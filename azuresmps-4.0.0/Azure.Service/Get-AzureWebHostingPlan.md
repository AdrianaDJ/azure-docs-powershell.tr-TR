---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 3B3F1870-348D-4303-9520-FD81D4650F5F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2103a155b12fdf1e481173d529ff3308a3b2200b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106512"
---
# Get-AzureWebHostingPlan

## SYNOPSIS
Geçerli abonelikteki Azure Web barındırma planlarını alır.

## INDEKI

```
Get-AzureWebHostingPlan [-WebSpaceName <String>] [-Name <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## Tanım
Bu konuda, Microsoft Azure PowerShell modülünün 0.8.10 sürümündeki cmdlet açıklanmaktadır.
Kullandığınız modülün sürümünü edinmek için, Azure PowerShell konsolunda yazın `(Get-Module -Name Azure).Version` .

**Get-AzureWebHostingPlan** cmdlet 'i geçerli abonelikteki Azure Web barındırma planlarını alır.

Varsayılan olarak **Get-AzureWebHostingPlan** , geçerli abonelikteki tüm Azure barındırma planlarını alır ve planlar hakkında temel bilgiler sağlayan bir nesne döndürür.
*Web alanı* ve *ad* parametrelerini kullandığınızda **Get-AzureWebHostingPlan** , belirli bir barındırma planı nesnesini döndürür.

Geçerli aboneliği bulmak için **Get-Azuyeniden gönderme scripscripts** cmdlet 'inin *Current* parametresini kullanın.
Geçerli aboneliği değiştirmek için, **Select-azuyeniden komut** dosyası cmdlet 'ini kullanın.

## ÖRNEKLERDEN

### Örnek 1: abonelikteki tüm Web barındırma planlarını alma
```
PS C:\> Get-AzureWebHostingPlan 

Name : Default1 
SKU : Basic 
WorkerSize : Small 
NumberOfWorkers : 1 
CurrentWorkerSize : Small 
CurrentNumberOfWorkers : 1 
Status : Ready 
WebSpace : eastuswebspace 
Name : Default0 
SKU : Free 
WorkerSize : Small 
NumberOfWorkers : 0 
CurrentWorkerSize : Small 
CurrentNumberOfWorkers : 0 
Status : Ready
```

Bu komut, geçerli abonelikteki tüm Azure Web barındırma planlarını alır.

### Örnek 2: bir abonelikte belirli bir Web barındırma planı alma
```
PS C:\> Get-AzureWebHostingPlan -WebSpaceName "westeuropewebspace" -Name "Default0" 

Name : Default0 
SKU : Free 
WorkerSize : Small 
NumberOfWorkers : 0 
CurrentWorkerSize : Small 
CurrentNumberOfWorkers : 0 
Status : Ready 
WebSpace : westeuropewebspace
```

Bu komut, geçerli abonelikteki westeuropewebspace adındaki Web alanında Default0 adlı web barındırma planını alır.

## PARAMETRELERINE

### -Ad
Abonelikteki bir planın adını belirtir.
Varsayılan olarak, bu cmdlet geçerli abonelikteki tüm planları alır.
Bu parametre joker karakterleri desteklemez.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
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

### -WebSpaceName
Abonelikteki bir Web sayfasının adını belirtir.
Varsayılan olarak, bu cmdlet belirtilen Web alanındaki tüm Web sitelerini alır.
Bu parametre joker karakterleri desteklemez.

```yaml
Type: String
Parameter Sets: (All)
Aliases: WebSpace

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

###  
Bu cmdlet 'e girişi, değer olarak değil, özellik adıyla geçirebilirsiniz.

## ÇıKıŞLAR

### Microsoft. Windowsazde. Commands. Utilities. WebEntities. Services. WebEntities. WebHostingPlan
Varsayılan olarak **Get-AzureWebHostingPlan** , **webhostingplan** nesnelerinin dizisini döndürür.

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

