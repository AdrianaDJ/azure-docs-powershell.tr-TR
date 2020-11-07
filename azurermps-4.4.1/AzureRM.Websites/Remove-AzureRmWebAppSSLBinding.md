---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 3AB3D398-E5DB-4214-BA27-6E3B7D225550
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmWebAppSSLBinding.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmWebAppSSLBinding.md
ms.openlocfilehash: 553a9561939ffcef3337b0c13d384c5f5f47340e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764743"
---
# Remove-AzureRmWebAppSSLBinding

## SYNOPSIS
Karşıya yüklenen sertifikadan SSL bağlamasını kaldırır.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

### S1
```
Remove-AzureRmWebAppSSLBinding [-Name] <String> [[-DeleteCertificate] <Boolean>] [-Force]
 [-ResourceGroupName] <String> [-WebAppName] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### S2
```
Remove-AzureRmWebAppSSLBinding [-Name] <String> [[-DeleteCertificate] <Boolean>] [-Force] [-WebApp] <Site>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Tanım
**Remove-AzureRmWebAppSSLBinding** cmdlet 'i, bir Azure Web uygulamasından güvenli yuva KATMANı (SSL) bağlamasını kaldırır.
SSL bağlamaları bir Web uygulamasını sertifikayla ilişkilendirmek için kullanılır.

## ÖRNEKLERDEN

### Örnek 1: Web uygulamasının SSL bağlamasını kaldırma
```
PS C:\>Remove-AzureRmWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp" -Name "www.contoso.com"
```

Bu komut, Web uygulamasının ContosoWebApp için SSL bağlamasını kaldırır.
*Deletecertificate* parametresi dahil olmadığından, SERTIFIKA artık SSL bağlamaları yoksa silinir.

### Örnek 2: sertifikayı kaldırmadan SSL bağlamasını kaldırma
```
PS C:\>Remove-AzureRmWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp" -Name "www.contoso.com" -DeleteCertificate $False
```

Bu komut, örnek 1 ' e benzer şekilde, Web uygulamasının ContosoWebApp için SSL bağlamasını da kaldırır.
Bu örnekte, *Deletecertificate* parametresi eklenir ve parametre değeri $false olarak ayarlanır.
Bu, herhangi bir SSL bağlaması olup olmamasına bakılmaksızın sertifikanın silinmeyeceği anlamına gelir.

### Örnek 3: SSL bağlamasını kaldırmak için nesne başvurusu kullanma
```
PS C:\>$WebApp = Get-AzureRmWebApp -Name "ContosoWebApp"
PS C:\> Remove-AzureRmWebAppSSLBinding -WebApp $WebApp -Name "www.contoso.com"
```

Bu örnekte, Web uygulamasının SSL bağlamasını kaldırmak için Web App Web sitesinin nesne başvurusu kullanılır.

İlk komut, Get-AzureRmWebApp cmdlet 'ini kullanarak, ContosoWebApp adlı Web uygulamasına nesne başvurusu oluşturur.
Bu nesne başvurusu $WebApp adlı bir değişkende depolanır.

İkinci komut, SSL bağlamasını kaldırmak için nesne başvurusu ve **Remove-AzureRmWebAppSSLBinding** cmdlet 'ini kullanır.

## PARAMETRELERINE

### -DeleteCertificate
Kaldırılan SSL bağlaması sertifika tarafından kullanılan tek bağlamadır, gerçekleşecek eylemi belirtir.
*Deletecertificate* $false olarak ayarlanırsa, bağlama silindiğinde sertifika silinmez.
*Deletecertificate* $true olarak ayarlanmışsa veya komuta dahil değilse, sertifika SSL bağlamasıyla birlikte silinir.

Sertifika yalnızca kaldırılan SSL bağlaması sertifika tarafından kullanılan tek bağlamadır silinir.
Sertifikada birden fazla bağlama varsa, sertifika *deletecertificate* parametresinin değerinden bağımsız olarak kaldırılamaz.

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Ad
Web uygulamasının adını belirtir.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Sertifikanın atandığı kaynak grubunun adını belirtir.

Aynı komutta *Resourcegroupname* parametresini ve *WebApp* parametresini kullanamazsınız.

```yaml
Type: System.String
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
Dağıtım yuvası almak için Get-AzureRMWebAppSlot cmdlet 'ini kullanın.

```yaml
Type: System.String
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
Web uygulaması edinmek için Get-AzureRmWebApp cmdlet 'ini kullanın.

*WebApp* parametresini, *resourcegroupname* parametresi ve/veya *webappname* ile aynı komutta kullanamazsınız.

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -WebAppName
Web uygulamasının adını belirtir.

Aynı komutta *Webappname* parametresini ve *WebApp* parametresini kullanamazsınız.

```yaml
Type: System.String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Onay
Cmdlet 'i çalıştırmadan önce onaylamanızı ister.

```yaml
Type: System.Management.Automation.SwitchParameter
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
Cmdlet çalışmaz. Cmdlet çalışırsa ne olacağını gösterir.
Cmdlet çalışmaz.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### Bölge
' WebApp ' parametresi ardışık düzenin ' site ' türünün değerini kabul eder

## ÇıKıŞLAR

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-AzureRmWebAppSSLBinding](./Get-AzureRmWebAppSSLBinding.md)

[Yeni-AzureRmWebAppSSLBinding](./New-AzureRmWebAppSSLBinding.md)

[Get-AzureRMWebAppSlot](./Get-AzureRMWebAppSlot.md)

[Get-AzureRmWebApp](./Get-AzureRmWebApp.md)


