---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 9D4A68A8-0A39-4C9A-8EA6-391A5E7A0E25
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/add-azapimanagementregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementRegion.md
ms.openlocfilehash: b180dabec976164eac70106b49378d832fb00db8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93751186"
---
# Add-AzApiManagementRegion

## SYNOPSIS
Psapsananamı örneğine yeni dağıtım bölgeleri ekler.

## INDEKI

```
Add-AzApiManagementRegion -ApiManagement <PsApiManagement> -Location <String> [-Sku <PsApiManagementSku>]
 [-Capacity <Int32>] [-VirtualNetwork <PsApiManagementVirtualNetwork>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Add-Azapsananagementregion** cmdlet 'ı, **psapimanagementregion** türünde sağlanan **Microsoft. Azure. Commands. Apsananad. model** **AdditionalRegions**
Bu cmdlet kendisiyle hiçbir şey dağıtmaz ancak bellekteki **Psapımana**
API yönetiminin dağıtımını güncelleştirmek için, değiştirilmiş **Psapsananadınstance** öğesini Update-Azapsananagementdeployment 'e geçirin.

## ÖRNEKLERDEN

### Örnek 1: bir Psapsanana, bir örneğine yeni dağıtım bölgeleri ekleme
```
PS C:\>Add-AzApiManagementRegion -ApiManagement $ApiManagement -Location "East US" -Sku "Premium" -Capacity 2
```

Bu komut iki Premium SKU birimi ve Doğu ABD adlı bölgeyi **Psapımanadıman**

### Örnek 2: psapsananadın
```
PS C:\>Get-AzApiManagement -ResourceGroupName "Contoso" -Name "ContosoApi" | Add-AzApiManagementRegion -Location "East US" -Sku "Premium" -Capacity 2 | Update-AzApiManagementDeployment
```

Bu komut, **Psapsanananabir** nesne alır, Doğu ABD adlı bölge için ıkı Premium SKU birimi ekler ve ardından dağıtımı güncelleştirir.

## PARAMETRELERINE

### -Ucuz
Bu cmdlet 'in ek dağıtım bölgelerini eklediği **Psapimana,** örneğini belirtir.

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
Dağıtım bölgesinin SKU kapasitesini belirtir.

```yaml
Type: System.Nullable`1[System.Int32]
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
API yönetim hizmeti için desteklenen bölge arasındaki yeni dağıtım bölgesinin konumunu belirtir.
Geçerli konumlar almak için, "Microsoft. Apsananae" Get-AzResourceProvider cmdlet 'ini kullanın. WHERE {$ _. ResourceTypes [0]. ResourceTypeName-EQ "hizmet"} | Select-Object konumları

```yaml
Type: System.String
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
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku]
Parameter Sets: (All)
Aliases:
Accepted values: Developer, Standard, Premium, Basic

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VirtualNetwork
Sanal ağ yapılandırmasını belirtir.

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork
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

### Microsoft. Azure. Commands. apsanana

## ÇıKıŞLAR

### Microsoft. Azure. Commands. apsanana

## NOTLARıNDA
* Cmdlet, güncelleştirilmiş **Psapsananadörneği** ardışık düzene yazar.

## ILGILI BAĞLANTıLAR

[Remove-Azapsananagementregion](./Remove-AzApiManagementRegion.md)

[Güncelleştirme-Azapsananagementregion](./Update-AzApiManagementRegion.md)

[Güncelleştirme-Azapsananagementdeployment](./Update-AzApiManagementDeployment.md)


