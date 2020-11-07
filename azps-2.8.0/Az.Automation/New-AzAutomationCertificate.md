---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: A504099E-BA96-45C9-A7A6-195E7087A0D4
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationCertificate.md
ms.openlocfilehash: 1c3c3cb4fecfde01926e21a75470fc945f8c86c1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753281"
---
# New-AzAutomationCertificate

## SYNOPSIS
Otomasyon sertifikası oluşturur.

## INDEKI

```
New-AzAutomationCertificate [-Name] <String> [-Description <String>] [-Password <SecureString>]
 [-Path] <String> [-Exportable] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Yeni-AzAutomationCertificate** cmdlet 'ı Azure Otomasyonu 'nda sertifika oluşturur.
Karşıya yüklenecek sertifika dosyasının yolunu sağlayın.

## ÖRNEKLERDEN

### Örnek 1: yeni sertifika oluşturma
```
PS C:\>$Password = ConvertTo-SecureString -String "Password" -AsPlainText -Force
PS C:\> New-AzAutomationCertificate -AutomationAccountName "Contoso17" -Name "ContosoCertificate" -Path "./cert.pfx" -Password $Password -ResourceGroupName "ResourceGroup01"
```

İlk komut, ConvertTo-SecureString cmdlet 'ini kullanarak düz metin parolasını güvenli dize olacak şekilde dönüştürür.
Komut bu nesneyi $Password değişkeninde depolar.
İkinci komut, ContosoCertificate adlı bir sertifika oluşturur.
Komut $Password uygulamasında depolanan parolayı kullanır.
Komut, sayfanın adını ve karşıya yüklenen dosyanın yolunu belirtir.

## PARAMETRELERINE

### -AutomationAccountName
Bu cmdlet 'in sertifikayı sakladığı Otomasyon hesabının adını belirtir.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik

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

### -Açıklama
Sertifikanın açıklamasını belirtir.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Dışarı aktarılabilir
Sertifikanın dışarı aktarılabildiğinden belirtir.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Ad
Sertifikanın adını belirtir.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Parola
Sertifika dosyasının parolasını belirtir.

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Yol
Bu cmdlet 'in karşıya yüklemelerinin bir komut dosyasının yolunu belirtir.
Dosya bir. cer veya. pfx dosyası olabilir.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Bu cmdlet 'in sertifika oluşturduğu kaynak grubunun adını belirtir.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### System. String

### System. Security. SecureString

### System. Management. Automation. SwitchParameter

## ÇıKıŞLAR

### Microsoft. Azure. Commands. Automation. model. Certificateınfo

## NOTLARıNDA

Bu komut, yönetici olduğunuz bir makinede, ayrıca yükseltilmiş bir PowerShell oturumunda çalıştırılmalıdır; Sertifika yüklenmeden önce, bu cmdlet yerel X. 509.440 deposunu kullanarak parmak izi ve anahtarı alır ve bu cmdlet yükseltilmiş PowerShell oturumu dışında çalıştırıldığında, "erişim reddedildi" hatası alırsınız.

## ILGILI BAĞLANTıLAR

[Get-AzAutomationCertificate](./Get-AzAutomationCertificate.md)

[Remove-AzAutomationCertificate](./Remove-AzAutomationCertificate.md)

[Set-AzAutomationCertificate](./Set-AzAutomationCertificate.md)


