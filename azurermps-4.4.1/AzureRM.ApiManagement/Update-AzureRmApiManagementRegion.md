---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 5B7B285A-6418-44D7-BD78-E14AFFAA7765
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Update-AzureRmApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Update-AzureRmApiManagementRegion.md
ms.openlocfilehash: 29dd6d1938228d3e76c0393ca27f49a3a9fe2564
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587009"
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

### -Konum
Güncelleştirilecek dağıtım bölgesinin konumunu belirtir.

Geçerli değerler:

- Kuzey Orta ABD
- Güney Orta ABD
- Orta ABD
- Batı Avrupa
- Kuzey Avrupa
- Batı ABD
- Doğu ABD
- Doğu ABD 2
- Japon Doğu
- Japon Batı
- Brezilya Güney
- Güneydoğu Asya
- Doğu Asya
- Avustralya Doğu
- Avustralya Güneydoğu

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
Accepted values: Developer, Standard, Premium

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

### Bağış
Parametre ' Apsananadeğeri ', ardışık düzen

## ÇıKıŞLAR

### Microsoft. Azure. Commands. apsanana

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Add-Azurermapımanagementregion](./Add-AzureRmApiManagementRegion.md)

[Remove-Azurermapımanagementregion](./Remove-AzureRmApiManagementRegion.md)

[Güncelleştirme-Azurermapımanagementdeployment](./Update-AzureRmApiManagementDeployment.md)
