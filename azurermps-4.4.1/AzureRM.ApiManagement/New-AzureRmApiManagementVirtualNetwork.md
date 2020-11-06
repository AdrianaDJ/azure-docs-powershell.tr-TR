---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: FB5E4ED2-8EF3-462F-A053-7EC82C767E8D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementVirtualNetwork.md
ms.openlocfilehash: 42213ddd4a7780b4d69b357c4b801df34aa9aca4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587038"
---
# New-AzureRmApiManagementVirtualNetwork

## SYNOPSIS
PsApiManagementVirtualNetwork örneğini oluşturur.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

```
New-AzureRmApiManagementVirtualNetwork -Location <String> -SubnetResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**New-AzureRmApiManagementVirtualNetwork** cmdlet 'i, bir **PsApiManagementVirtualNetwork** örneği oluşturmak için yardımcı komuttur.
Bu komut **set-Azurermapımanagementvirtualnetworks** cmdlet ile kullanılır.

## ÖRNEKLERDEN

### Örnek 1: sanal ağ oluşturma
```
PS C:\>$VirtualNetworks = @()
PS C:\> $VirtualNetworks += New-AzureRmApiManagementVirtualNetwork -Location "East US" -SubtenName "ContosoNet" -VnetId "089D3F4D-B986-4DFD-9259-9112BA7A1F03"
PS C:\> Set-AzureRmApiManagementVirtualNetworks -ResourceGroupName "ContosoGroup" -Name "ContosoApi" -VirtualNetworks $VirtualNetworks
```

Bu örnekte sanal bir ağ oluşturulur ve ardından **set-Azurermapımanagementvirtualnetworks** cmdlet 'ini arar.

## PARAMETRELERINE

### -Konum
Bu cmdlet 'in örneği oluşturduğu sanal ağın konumunu belirtir.

Bu parametre için kabul edilebilir değerler şunlardır:

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

### -Subnetresourceıd
Sanal ağın alt ağ kaynak KIMLIĞINI belirtir.

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

### Microsoft. Azure. Commands. apsanana

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

