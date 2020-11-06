---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementidentityprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementIdentityProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementIdentityProvider.md
ms.openlocfilehash: e25e3bfad6c40b136c3cbaa65999b8118e0abd11
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592515"
---
# Get-AzureRmApiManagementIdentityProvider

## SYNOPSIS
Kimlik sağlayıcısı yapılandırma ayrıntılarını edinin.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

### Aldentityproviders (varsayılan)
```
Get-AzureRmApiManagementIdentityProvider -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### IdentityProvider
```
Get-AzureRmApiManagementIdentityProvider -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
Kimlik sağlayıcısı yapılandırma ayrıntılarını edinin.

## ÖRNEKLERDEN

### Örnek 1: tüm kimlik sağlayıcılarını alma

```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementIdentityProvider -Context $apimContext
```

Hizmette tüm kimlik sağlayıcısı yapılandırmasını edinin.

### AAD türü kimlik sağlayıcısını alma
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementIdentityProvider -Context $apimContext -Type Aad
```

Azure Active Directory 'nin kimlik sağlayıcı yapılandırmasını alır.

## PARAMETRELERINE

### -Context
Psapsananagementcontext örneği.
Bu parametre gereklidir.

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.
 
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Tür
Kimlik sağlayıcısının tanımlayıcısı.
Belirtilmişse tanımlayıcı tarafından kimlik sağlayıcı yapılandırmasını bulmaya çalışır.
Bu parametre isteğe bağlıdır.

```yaml
Type: PsApiManagementIdentityProviderType
Parameter Sets: IdentityProviderByType
Aliases: 
Accepted values: Facebook, Google, Microsoft, Twitter, Aad

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### Yabilirsiniz
Bu cmdlet hiçbir girişi kabul etmez.

## ÇıKıŞLAR

### Microsoft. Azure. Commands. Apsananad. ServiceManagement. modeller. Psapsananagementidentityprovider
API Yönetim hizmetinde yapılandırılan kimlik sağlayıcısının ayrıntıları.

### IList<Microsoft. Azure. Commands. Apsananad. ServiceManagement. modeller. Psapsananagementidentityprovider>
API Yönetim hizmetinde yapılandırılan kimlik sağlayıcılarının listesi.

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

