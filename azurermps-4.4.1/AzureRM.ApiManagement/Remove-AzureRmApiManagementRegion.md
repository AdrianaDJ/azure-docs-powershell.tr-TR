---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 17D7EBD2-FE3F-4D24-A1AA-8C45B9B1FEF5
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementRegion.md
ms.openlocfilehash: 8bacb26b4e30521ddd840d2a8081365ed9c4c6ad
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587021"
---
# Remove-AzureRmApiManagementRegion

## SYNOPSIS
Psapsananaddeğerinden var olan bir dağıtım bölgesini kaldırır.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

```
Remove-AzureRmApiManagementRegion -ApiManagement <PsApiManagement> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Remove-Azurermapsananagementregion** cmdlet 'i, Microsoft. Azure. Commands. **Apsananad. model. psapsananad,** sağlanan bir **Additionalregion** koleksiyonundan **Microsoft. Azure. Commands**
Bu cmdlet, dağıtımı kendi başına değiştirmez ancak bellekteki **Psapımana**
Bir API yönetiminin dağıtımını güncelleştirmek için, değiştirilmiş **Psapsananagementınstance** öğesini **güncelleştirmeye-Azurermapsananae** geçirin.

## ÖRNEKLERDEN

### Örnek 1: psapsanana
```
PS C:\>Remove-AzureRmApiManagementRegion -ApiManagement $ApiManagement -Location "East US"
```

Bu komut, **Psapsananadus** ÖRNEĞINDEKI Doğu US adındaki bölgeyi kaldırır.

### Örnek 2: bir dizi komutu kullanarak psapsanana
```
PS C:\>Get-AzureRmApiManagement -ResourceGroupName "Contoso" -Name ContosoApi | Remove-AzureRmApiManagementRegion -Location "East US" | Update-AzureRmApiManagementDeployment
```

İlk komut, contoso adlı bir kaynak grubundan Contosoapı adlı kaynak grubundan bir **Psapsananadörneği** alır.
Son komutu daha sonra o örnekten Doğu ABD adlı bölgeyi kaldırır ve dağıtımı güncelleştirir.

## PARAMETRELERINE

### -Ucuz
Bu cmdlet 'in ek dağıtım bölgesini kaldırdığı **Psapimanadörneği** 'ni belirtir.

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

### -Konum
Bu cmdlet 'in kaldırıldığı bölgenin konumunu belirtir.

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

[Güncelleştirme-azurermapsanana](./Update-AzureRmApiManagementRegion.md)


