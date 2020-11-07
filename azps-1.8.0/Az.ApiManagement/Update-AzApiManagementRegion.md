---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 5B7B285A-6418-44D7-BD78-E14AFFAA7765
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/update-azapimanagementregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementRegion.md
ms.openlocfilehash: fce2d356b7da56d2b93fa8634e737f96f54da178
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93917651"
---
# Update-AzApiManagementRegion

## SYNOPSIS
Psapımanadörneği örneğinde varolan dağıtım bölgesini güncelleştirir.

## INDEKI

```
Update-AzApiManagementRegion -ApiManagement <PsApiManagement> -Location <String> -Sku <PsApiManagementSku>
 -Capacity <Int32> [-VirtualNetwork <PsApiManagementVirtualNetwork>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Tanım
**Update-Azapsananagementregion** cmdlet 'i, Microsoft. **Azure. Commands. Apsananamedid. model. Psapsananad,** sağlanan bir örnek **Addiregion** nesneleri koleksiyonunda **Microsoft. Azure. Commands**
Bu cmdlet hiçbir şey dağıtmaz ancak bellekteki bir **Psapımanadın** örneğini güncelleştirir.
Bir API yönetiminin dağıtımını güncelleştirmek için, değiştirilmiş **Psapsananagementınstance** 'ı Update-AzApiManagementDeployment cmdlet 'ine kullanın.

## ÖRNEKLERDEN

### Örnek 1: psapsanan
```powershell
PS C:\>$apimService = Get-AzApiManagement -ResourceGroupName $resourceGroupName -Name $apiManagementName
PS C:\>$apimService = Update-AzApiManagementRegion -ApiManagement $apimService -Location "North Central US" -Capacity 2 -Sku Premium

# Set the ApiManagement service and Enable Msi idenity on the service
PS C:\>$updatedService = Set-AzApiManagement -InputObject $apimService -PassThru
```

Bu komut, Güney Merkezi ABD ve Kuzey Merkezi ABD 'de bölgeleri bulunan API Yönetimi Premium SKU hizmetini alır. Ardından, **güncelleştirme-Azapsananagementregion** kullanarak Kuzey Merkezi ABD bölgesinin kapasitesini 2 ile artırır. Sonraki cmdlet Set-AzApiManagement yapılandırma değişikliğini API Yönetim hizmetine uygular.

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
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Konum
Güncelleştirilecek dağıtım bölgesinin konumunu belirtir.
API yönetim hizmeti için desteklenen bölge arasındaki yeni dağıtım bölgesinin konumunu belirtir.
Geçerli konumlar almak için, "Microsoft. Apsananae" Get-AzResourceProvider cmdlet 'ini kullanın. WHERE {$ _. ResourceTypes [0]. ResourceTypeName-EQ "hizmet"} | Select-Object konumları

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

### System. String

### Microsoft. Azure. Commands. apsanana

### System. Int32

### Microsoft. Azure. Commands. apsanana

## ÇıKıŞLAR

### Microsoft. Azure. Commands. apsanana

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Add-Azapsananagementregion](./Add-AzApiManagementRegion.md)

[Remove-Azapsananagementregion](./Remove-AzApiManagementRegion.md)

[Güncelleştirme-Azapsananagementdeployment](./Update-AzApiManagementDeployment.md)
