---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
ms.assetid: D4C465CE-1B8A-4CFC-BAA8-21CC66B7D6D6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementhostnameconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementHostnameConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementHostnameConfiguration.md
ms.openlocfilehash: 066538db3a763c5a3c6d9de9f621ca2b81552983
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586847"
---
# New-AzureRmApiManagementHostnameConfiguration

## SYNOPSIS
PsApiManagementHostnameConfiguration örneği oluşturur.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

```
New-AzureRmApiManagementHostnameConfiguration -CertificateThumbprint <String> -Hostname <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Yeni-Azurermapsananagementhostnameconfiguration** cmdlet 'ı, **Psapimanagementhostnameconfiguration** örneğini oluşturan bir yardımcı komuttur.
Bu komut Set-AzureRmApiManagementHostnames cmdlet 'le kullanılır.

## ÖRNEKLERDEN

### Örnek 1: PsApiManagementHostnameConfiguration örneği oluşturma ve başlatma
```
PS C:\>New-AzureRmApiManagementHostnameConfiguration -Hostname "portal.contoso.com" -CertificateThumbprint "33CC47C6FCA848DC9B14A6F071C1EF7C"
```

Bu komut bir **Psapsananagementhostnameconfiguration** örneği oluşturur ve başlatır.

## PARAMETRELERINE

### -CertificateThumbprint
Sertifika parmak izini belirtir.
Sertifikanın öncelikle Import-AzureRmApiManagementHostnameCertificate cmdlet 'i ile içeri aktarılması gerekir.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
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

### -Ana bilgisayar adı
Bu cmdlet 'in **Psapimanagementhostnameconfiguration** örneğini oluşturduğu özel ana bilgisayar adını belirtir.

```yaml
Type: String
Parameter Sets: (All)
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

### Yabilirsiniz
Bu cmdlet hiçbir girişi kabul etmez.

## ÇıKıŞLAR

### Microsoft. Azure. Commands. Apsananad. modeller. Psapsananagementhostnameconfiguration

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Import-Azurermapımanagementhostnamecertificate](./Import-AzureRmApiManagementHostnameCertificate.md)

[Set-Azurermapımanagementhostnames](./Set-AzureRmApiManagementHostnames.md)


