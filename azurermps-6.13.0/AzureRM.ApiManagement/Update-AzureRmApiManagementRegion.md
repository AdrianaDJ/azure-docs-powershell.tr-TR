---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 5B7B285A-6418-44D7-BD78-E14AFFAA7765
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/update-azurermapimanagementregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Update-AzureRmApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Update-AzureRmApiManagementRegion.md
ms.openlocfilehash: ed26538e54cef189837bd36bf9e6f561df3541f4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587320"
---
# Update-AzureRmApiManagementRegion

## SYNOPSIS
Psapımanadörneği örneğinde varolan dağıtım bölgesini güncelleştirir.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

```
Update-AzureRmApiManagementRegion -ApiManagement <PsApiManagement> -Location <String> -Sku <PsApiManagementSku>
 -Capacity <Int32> [-VirtualNetwork <PsApiManagementVirtualNetwork>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Tanım
**Update-Azurermapsananagementregion** cmdlet 'ı, **Microsoft. Azure. Commands. Apsananamedid. model. Psapsananad,** sağlanan bir örnek **Addiregion** nesneleri koleksiyonunda **Microsoft. Azure. Commands**
Bu cmdlet hiçbir şey dağıtmaz ancak bellekteki bir **Psapımanadın** örneğini güncelleştirir.
Bir API yönetiminin dağıtımını güncelleştirmek için, değiştirilmiş **Psapsananagementınstance** 'ı Update-AzureRmApiManagementDeployment cmdlet 'ine kullanın.

## ÖRNEKLERDEN

## PARAMETRELERINE

### -Ucuz
Var olan bir dağıtım bölgesini güncelleştirmek için **Psapimana,** örneğini belirtir.

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Kapasite
Dağıtım bölgesi için yeni SKU kapasite değerini belirtir.

```yaml
Type: System.Int32
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
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Konum
Güncelleştirilecek dağıtım bölgesinin konumunu belirtir.
API yönetim hizmeti için desteklenen bölge arasındaki yeni dağıtım bölgesinin konumunu belirtir.
Geçerli konumlar almak için, "Microsoft. Apsananae" Get-AzureRmResourceProvider cmdlet 'ini kullanın. WHERE {$ _. ResourceTypes [0]. ResourceTypeName-EQ "hizmet"} | Select-Object konumları

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

### -SKU
Dağıtım bölgesi için yeni katman değerini belirtir.
Geçerli değerler:
- İyle
- Ardından
- Min

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku
Parameter Sets: (All)
Aliases:
Accepted values: Developer, Standard, Premium, Basic

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VirtualNetwork
Dağıtım bölgesi için sanal ağ yapılandırmasını belirtir.
$Null geçirmek, bölgenin sanal ağ yapılandırmasını kaldırır.

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork
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

### Microsoft. Azure. Commands. apsanana
Parametreler: Apsananad(ByValue)

### System. String

### Microsoft. Azure. Commands. apsanana

### System. Int32

### Microsoft. Azure. Commands. apsanana

## ÇıKıŞLAR

### Microsoft. Azure. Commands. apsanana

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Add-Azurermapımanagementregion](./Add-AzureRmApiManagementRegion.md)

[Remove-Azurermapımanagementregion](./Remove-AzureRmApiManagementRegion.md)

[Güncelleştirme-Azurermapımanagementdeployment](./Update-AzureRmApiManagementDeployment.md)
