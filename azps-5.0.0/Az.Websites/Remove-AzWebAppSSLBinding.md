---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 3AB3D398-E5DB-4214-BA27-6E3B7D225550
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/remove-azwebappsslbinding
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppSSLBinding.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppSSLBinding.md
ms.openlocfilehash: bed5cb961fd39975b3f10debe8791a418fd5dcda
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94279251"
---
# Remove-AzWebAppSSLBinding

## SYNOPSIS
Karşıya yüklenen sertifikadan SSL bağlamasını kaldırır.

## INDEKI

### S1
```
Remove-AzWebAppSSLBinding [-Name] <String> [[-DeleteCertificate] <Boolean>] [-Force]
 [-ResourceGroupName] <String> [-WebAppName] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### S2
```
Remove-AzWebAppSSLBinding [-Name] <String> [[-DeleteCertificate] <Boolean>] [-Force] [-WebApp] <PSSite>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Tanım
**Remove-AzWebAppSSLBinding** cmdlet 'i, bir Azure Web uygulamasından güvenli yuva KATMANı (SSL) bağlamasını kaldırır.
SSL bağlamaları bir Web uygulamasını sertifikayla ilişkilendirmek için kullanılır.

## ÖRNEKLERDEN

### Örnek 1: Web uygulamasının SSL bağlamasını kaldırma
```
PS C:\>Remove-AzWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp" -Name "www.contoso.com"
```

Bu komut, Web uygulamasının ContosoWebApp için SSL bağlamasını kaldırır.
*Deletecertificate* parametresi dahil olmadığından, SERTIFIKA artık SSL bağlamaları yoksa silinir.

### Örnek 2: sertifikayı kaldırmadan SSL bağlamasını kaldırma
```
PS C:\>Remove-AzWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp" -Name "www.contoso.com" -DeleteCertificate $False
```

Bu komut, örnek 1 ' e benzer şekilde, Web uygulamasının ContosoWebApp için SSL bağlamasını da kaldırır.
Bu örnekte, *Deletecertificate* parametresi eklenir ve parametre değeri $false olarak ayarlanır.
Bu, herhangi bir SSL bağlaması olup olmamasına bakılmaksızın sertifikanın silinmeyeceği anlamına gelir.

### Örnek 3: SSL bağlamasını kaldırmak için nesne başvurusu kullanma
```
PS C:\>$WebApp = Get-AzWebApp -Name "ContosoWebApp"
PS C:\> Remove-AzWebAppSSLBinding -WebApp $WebApp -Name "www.contoso.com"
```

Bu örnekte, Web uygulamasının SSL bağlamasını kaldırmak için Web App Web sitesinin nesne başvurusu kullanılır.
İlk komut, Get-AzWebApp cmdlet 'ini kullanarak, ContosoWebApp adlı Web uygulamasına nesne başvurusu oluşturur.
Bu nesne başvurusu $WebApp adlı bir değişkende depolanır.
İkinci komut, SSL bağlamasını kaldırmak için nesne başvurusu ve **Remove-AzWebAppSSLBinding** cmdlet 'ini kullanır.

## PARAMETRELERINE

### -DefaultProfile
Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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
Dağıtım yuvası almak için Get-AzWebAppSlot cmdlet 'ini kullanın.

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
Web uygulaması edinmek için Get-AzWebApp cmdlet 'ini kullanın.
*WebApp* parametresini, *resourcegroupname* parametresi ve/veya *webappname* ile aynı komutta kullanamazsınız.

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
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

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### Microsoft. Azure. Commands. WebApps. modeller. PSSite

## ÇıKıŞLAR

### System. void

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-AzWebAppSSLBinding](./Get-AzWebAppSSLBinding.md)

[Yeni-AzWebAppSSLBinding](./New-AzWebAppSSLBinding.md)

[Get-AzWebAppSlot](./Get-AzWebAppSlot.md)

[Get-AzWebApp](./Get-AzWebApp.md)


