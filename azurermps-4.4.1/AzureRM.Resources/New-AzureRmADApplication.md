---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: F58FD77E-2946-44B1-B410-6E983FC20E21
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmADApplication.md
ms.openlocfilehash: c43bba247268d7ffcdbc2c33d7198415738c5694
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594581"
---
# New-AzureRmADApplication

## SYNOPSIS
Yeni bir Azure Active Directory uygulaması oluşturur.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

### ApplicationWithoutCredentialParameterSet (varsayılan)
```
New-AzureRmADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ApplicationWithPasswordPlainParameterSet
```
New-AzureRmADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -Password <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ApplicationWithPasswordCredentialParameterSet
```
New-AzureRmADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -PasswordCredentials <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ApplicationWithKeyPlainParameterSet
```
New-AzureRmADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ApplicationWithKeyCredentialParameterSet
```
New-AzureRmADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -KeyCredentials <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Tanım
Yeni bir Azure Active Directory uygulaması oluşturur.

## ÖRNEKLERDEN

### Yeni AAD uygulaması oluşturma--------------------------.  --------------------------
```
PS C:\> New-AzureRmADApplication -DisplayName "NewApplication" -HomePage "https://www.microsoft.com" -IdentifierUris "http://NewApplication"
```

Kimlik bilgileri olmadan yeni bir Azure Active Directory uygulaması oluşturur.

### Parolayla yeni AAD uygulaması oluşturmak--------------------------.  --------------------------
```
PS C:\> New-AzureRmADApplication -DisplayName "NewApplication" -HomePage "https://www.microsoft.com" -IdentifierUris "http:
//NewApplication" -Password "password"
```

Yeni bir Azure Active Directory uygulaması oluşturur ve parola kimlik bilgilerini onunla ilişkilendirir.

## PARAMETRELERINE

### -Availabletootherkiracılar
Uygulamanın tek kiracılı mı yoksa çok kiracılı mı olduğunu belirten değer.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -CertValue
"Asimetrik" kimlik bilgileri türü.
Temel 64 kodlu sertifikayı temsil eder.

```yaml
Type: System.String
Parameter Sets: ApplicationWithKeyPlainParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DisplayName
Yeni uygulamanın görünen adı.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -EndDate
Kimlik bilgisi kullanımının geçerli bitiş tarihi.
Varsayılan bitiş tarihi değeri bugünden itibaren bir yıldır. "Asimetrik" tür kimlik bilgileri için, bu, x509 sertifikasının geçerli olduğu tarihte veya bu tarihte ayarlanmalıdır.

```yaml
Type: System.DateTime
Parameter Sets: ApplicationWithPasswordPlainParameterSet, ApplicationWithKeyPlainParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Giriş sayfası
Uygulama giriş sayfasının URL 'SI.

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

### -Identifieruris
Uygulamayı tanımlayan URI 'Ler.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -KeyCredentials
Uygulamayla ilişkili sertifika kimlik bilgilerinin listesi.

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADKeyCredential[]
Parameter Sets: ApplicationWithKeyCredentialParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Parola
Uygulamayla ilişkilendirilecek parola.

```yaml
Type: System.String
Parameter Sets: ApplicationWithPasswordPlainParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PasswordCredentials
Uygulamayla ilişkili parola kimlik bilgileri listesi.

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADPasswordCredential[]
Parameter Sets: ApplicationWithPasswordCredentialParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ReplyUrls
Uygulama yanıt URL 'leri.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StartDate
Kimlik bilgisi kullanımının geçerli başlangıç tarihi.
Varsayılan başlangıç tarihi değeri bugün. "Asimetrik" tür kimlik bilgileri için, bu, x509 sertifikasının geçerli olduğu tarihten sonra veya bu tarihten sonra ayarlanmalıdır.

```yaml
Type: System.DateTime
Parameter Sets: ApplicationWithPasswordPlainParameterSet, ApplicationWithKeyPlainParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
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

## ÇıKıŞLAR

### Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADApplication

## NOTLARıNDA
Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, kaynak, Grup, şablon, dağıtım

## ILGILI BAĞLANTıLAR

[Remove-AzureRmADApplication](./Remove-AzureRmADApplication.md)

[Get-AzureRmADApplication](./Get-AzureRmADApplication.md)

[New-AzureRmADServicePrincipal](./New-AzureRmADServicePrincipal.md)

[Get-AzureRmADAppCredential](./Get-AzureRmADAppCredential.md)

[Yeni-AzureRmADAppCredential](./New-AzureRmADAppCredential.md)

[Remove-AzureRmADAppCredential](./Remove-AzureRmADAppCredential.md)

