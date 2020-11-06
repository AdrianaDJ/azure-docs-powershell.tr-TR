---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 9D4A68A8-0A39-4C9A-8EA6-391A5E7A0E25
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Add-AzureRmApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Add-AzureRmApiManagementRegion.md
ms.openlocfilehash: 7edf16a6970f831235f76c64ef5cb5181a49bf98
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593860"
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

### -Konum
Yeni dağıtım bölgesinin konumunu belirtir.

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
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork
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
* Cmdlet, güncelleştirilmiş **Psapsananadörneği** ardışık düzene yazar.

## ILGILI BAĞLANTıLAR

[Remove-Azurermapımanagementregion](./Remove-AzureRmApiManagementRegion.md)

[Güncelleştirme-azurermapsanana](./Update-AzureRmApiManagementRegion.md)

[Güncelleştirme-Azurermapımanagementdeployment](./Update-AzureRmApiManagementDeployment.md)


