---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: EE3D2BA0-32E7-4A37-BCAF-F0E8FAAC43CE
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/get-Azwebappsslbinding
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzWebAppSSLBinding.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzWebAppSSLBinding.md
ms.openlocfilehash: 4c1739120c024629e68395f34a7f66b4259eb311
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936109"
---
# Get-AzWebAppSSLBinding

## SYNOPSIS
Azure Web App sertifika SSL bağlamasını alır.

## INDEKI

### S1
```
Get-AzWebAppSSLBinding [[-Name] <String>] [-ResourceGroupName] <String> [-WebAppName] <String>
 [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### S2
```
Get-AzWebAppSSLBinding [[-Name] <String>] [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Tanım
**Get-AzWebAppSSLBinding** cmdlet 'i, bir Azure Web App Için güvenli yuva KATMANı (SSL) bağlaması alır.
SSL bağlamaları, bir Web uygulamasını karşıya yüklenen sertifikayla ilişkilendirmek için kullanılır.
Web Apps, birden çok sertifikaya bağlanabilir.

## ÖRNEKLERDEN

### Örnek 1: Web uygulaması için SSL bağlamaları alma
```
PS C:\>Get-AzWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp"
```

Bu komut, ContosoResourceGroup kaynak grubuyla ilişkilendirilmiş olan ContosoWebApp Web App 'in SSL bağlarını alır.

### Örnek 2: Web uygulaması için SSL bağlamaları almak üzere nesne başvurusu kullanma
```
PS C:\>$WebApp = Get-AzWebApp -Name "ContosoWebApp"
PS C:\> Get-AzWebAppSSLBinding -WebApp $WebApp
```

Bu örnekteki komutlar, Web uygulamasının ContosoWebApp için SSL bağlamalarını de alır; Bununla birlikte, Web uygulaması adı ve ilişkili kaynak grubunun adı yerine bir nesne başvurusu kullanılır.
Bu nesne başvurusu, örnekte, ContosoWebApp adlı Web uygulamasına bir nesne başvurusu oluşturmak üzere **Get-AzWebApp** kullanan ilk komut tarafından oluşturulur.
Bu nesne başvurusu $WebApp adlı bir değişkende depolanır.

Bu değişken ve **Get-AzWebAppSSLBinding** cmdlet 'ı, SSL bağlarını almak için ikinci komut tarafından kullanılır.

## PARAMETRELERINE

### -DefaultProfile
Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Ad
SSL bağlamanın adını belirtir.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Sertifikanın atandığı kaynak grubunun adını belirtir.

Aynı komutta *Resourcegroupname* parametresini ve *WebApp* parametresini kullanamazsınız.

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### Yuvalı
Web uygulaması dağıtım yuvasını belirtir.
Dağıtım yuvası almak için Get-AzWebAppSlot cmdlet 'ini kullanın.

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WebApp
Web uygulaması belirtir.
Web uygulaması edinmek için Get-AzWebApp cmdlet 'ini kullanın.

```yaml
Type: Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -WebAppName
Bu cmdlet 'in SSL bağlarını aldığı Web uygulamasının adını belirtir.

Aynı komutta *Webappname* parametresini ve *WebApp* parametresini kullanamazsınız.

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### Bölge
' WebApp ' parametresi ardışık düzenin ' site ' türünün değerini kabul eder

## ÇıKıŞLAR

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Yeni-AzWebAppSSLBinding](./New-AzWebAppSSLBinding.md)

[Remove-AzWebAppSSLBinding](./Remove-AzWebAppSSLBinding.md)

[Get-AzWebApp](./Get-AzWebApp.md)


