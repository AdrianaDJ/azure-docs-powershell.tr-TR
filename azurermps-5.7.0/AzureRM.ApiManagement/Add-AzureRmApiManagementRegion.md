---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
ms.assetid: 9D4A68A8-0A39-4C9A-8EA6-391A5E7A0E25
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/add-azurermapimanagementregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Add-AzureRmApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Add-AzureRmApiManagementRegion.md
ms.openlocfilehash: f7a2952bf466a0d964a8b9075832635d2560b6fb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594978"
---
# Add-AzureRmApiManagementRegion

## SYNOPSIS
Psapsananamı örneğine yeni dağıtım bölgeleri ekler.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

```
Add-AzureRmApiManagementRegion -ApiManagement <PsApiManagement> -Location <String> [-Sku <PsApiManagementSku>]
 [-Capacity <Int32>] [-VirtualNetwork <PsApiManagementVirtualNetwork>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Add-Azurermapsananagementregion** cmdlet 'ı, **psapsananagementregion** türünde sağlanan **Microsoft. Azure. Commands. Apsananad. model** **AdditionalRegions**
Bu cmdlet kendisiyle hiçbir şey dağıtmaz ancak bellekteki **Psapımana**
API yönetiminin dağıtımını güncelleştirmek için, değiştirilmiş **Psapımanadınstance** öğesini Update-Azurermapsananagementdeployment öğesine geçirin.

## ÖRNEKLERDEN

### Örnek 1: bir Psapsanana, bir örneğine yeni dağıtım bölgeleri ekleme
```
PS C:\>Add-AzureRmApiManagementRegion -ApiManagement $ApiManagement -Location "East US" -Sku "Premium" -Capacity 2
```

Bu komut iki Premium SKU birimi ve Doğu ABD adlı bölgeyi **Psapımanadıman**

### Örnek 2: psapsananadın
```
PS C:\>Get-AzureRmApiManagement -ResourceGroupName "Contoso" -Name "ContosoApi" | Add-AzureRmApiManagementRegion -Location "East US" -Sku "Premium" -Capacity 2 | Update-AzureRmApiManagementDeployment
```

Bu komut, **Psapsanananabir** nesne alır, Doğu ABD adlı bölge için ıkı Premium SKU birimi ekler ve ardından dağıtımı güncelleştirir.

## PARAMETRELERINE

### -Ucuz
Bu cmdlet 'in ek dağıtım bölgelerini eklediği **Psapimana,** örneğini belirtir.

```yaml
Type: PsApiManagement
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Kapasite
Dağıtım bölgesinin SKU kapasitesini belirtir.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
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

### -Konum
API yönetim hizmeti için desteklenen bölge arasındaki yeni dağıtım bölgesinin konumunu belirtir.

Geçerli konumlar almak için, "Microsoft. Apsananae" Get-AzureRmResourceProvider cmdlet 'ini kullanın. WHERE {$ _. ResourceTypes [0]. ResourceTypeName-EQ "hizmet"} | Select-Object konumları

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

### -SKU
Dağıtım bölgesinin katmanını belirtir.
Geçerli değerler: 

- İyle
- Ardından
- Min

```yaml
Type: PsApiManagementSku
Parameter Sets: (All)
Aliases: 
Accepted values: Developer, Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VirtualNetwork
Sanal ağ yapılandırmasını belirtir.

```yaml
Type: PsApiManagementVirtualNetwork
Parameter Sets: (All)
Aliases: 

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
* Cmdlet, güncelleştirilmiş **Psapsananadörneği** ardışık düzene yazar.

## ILGILI BAĞLANTıLAR

[Remove-Azurermapımanagementregion](./Remove-AzureRmApiManagementRegion.md)

[Güncelleştirme-azurermapsanana](./Update-AzureRmApiManagementRegion.md)

[Güncelleştirme-Azurermapımanagementdeployment](./Update-AzureRmApiManagementDeployment.md)


