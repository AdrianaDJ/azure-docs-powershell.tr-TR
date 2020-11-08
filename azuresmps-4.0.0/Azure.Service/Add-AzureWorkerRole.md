---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 8632A865-D4CC-4AE5-8307-055CDD776D26
online version: ''
schema: 2.0.0
ms.openlocfilehash: a2b79ee50bb5097896c2a120a9b7316adb2146b5
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105710"
---
# Add-AzureWorkerRole

## SYNOPSIS
Özel bir çalışan rolü için gerekli dosyaları ve yapılandırmayı oluşturur.

## INDEKI

```
Add-AzureWorkerRole [-TemplateFolder <String>] [-Name <String>] [-Instances <Int32>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Tanım
Bu konuda, Microsoft Azure PowerShell modülünün 0.8.10 sürümündeki cmdlet açıklanmaktadır.
Kullandığınız modülün sürümünü edinmek için, Azure PowerShell konsolunda yazın `(Get-Module -Name Azure).Version` .

**Add-AzureWorkerRole** cmdlet 'i, özel bir çalışan rolü için bazen scafkatlama olarak da adlandırılır.

## ÖRNEKLERDEN

### Örnek 1: tek bir örnek çalışanı oluşturma
```
PS C:\> Add-AzureWorkerRole -Name MyWorkerRole
```

Bu örnek, geçerli uygulamaya MyWorkerRole adlı tek bir çalışan rolü için scafkatlama ekler.

### Örnek 2: birden çok örnek çalışanı oluşturma
```
PS C:\> Add-AzureWorkerRole MyWorkerRole -I 2
```

Bu örnek, geçerli uygulamaya MyWorkerRole adlı yeni bir çalışan rolü için, rol örneği sayısı 2 olan bir scafkatlama ekler.

### Örnek 3: özel dolandırıcılarla çalışan rolü oluşturma
```
PS C:\> Add-AzureWorkerRole MyWorkerRole -TemplateFoldr .\MyWorkerRoleTemplate
```

Bu örnek özel dolandırıcılarla bir çalışan rolü oluşturur.

## PARAMETRELERINE

### -Örnekler
Bu çalışan rolünün rol örneklerinin sayısını belirtir.
Varsayılan değer 1 ' dir.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: i

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Ad
Çalışan rolünün adını belirtir.
Bu değer, çalışan rolünde barındırılan özel uygulama için scaflesi içeren klasör adını belirler.
Varsayılan, Workerrolen ' dır; burada sayı, hizmette çalışan rollerin sayısıdır.

```yaml
Type: String
Parameter Sets: (All)
Aliases: n

Required: False
Position: Named
Default value: None
Accept pipeline input: False
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

### -TemplateFolder
Çalışan rolünü oluştururken kullanılacak scafkatlama şablonu klasörünü belirtir.

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

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

## ÇıKıŞLAR

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Add-AzureWebRole](./Add-AzureWebRole.md)

[Yeni-AzureRoleTemplate](./New-AzureRoleTemplate.md)


