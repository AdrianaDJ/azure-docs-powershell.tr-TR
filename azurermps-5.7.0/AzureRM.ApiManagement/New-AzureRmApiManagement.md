---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 164C5205-01BA-47BB-B780-D0B9AE614A4B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagement.md
ms.openlocfilehash: ebf95d8e809731bdca2f288bc09054fd14353686
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594154"
---
# New-AzureRmApiManagement

## SYNOPSIS
Bir API yönetim dağıtımı oluşturur.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

```
New-AzureRmApiManagement -ResourceGroupName <String> -Name <String> -Location <String> -Organization <String>
 -AdminEmail <String> [-Sku <PsApiManagementSku>] [-Capacity <Int32>] [-VpnType <PsApiManagementVpnType>]
 [-VirtualNetwork <PsApiManagementVirtualNetwork>]
 [-Tag <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-AdditionalRegions <PsApiManagementRegion[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Yeni-Azurermapsanana,** Azure API YÖNETIMINDE bir API yönetim dağıtımı oluşturur.

## ÖRNEKLERDEN

### Örnek 1: Geliştirici katmanı API yönetim hizmeti oluşturma
```
PS C:\>New-AzureRmApiManagement -ResourceGroupName "ContosoGroup02" -Name "ContosoApi" -Location "Central US" -Organization "Contoso" -AdminEmail "admin@contoso.com"
```

Bu komut bir geliştirici katmanı API yönetim hizmeti oluşturur.
Bu komut, organizasyonu ve yönetici adresini belirtir.
Komut *SKU* parametresini belirtmez.
Bu nedenle, cmdlet geliştirici varsayılan değerini kullanır.

### Örnek 2: üç birimli standart bir katman hizmeti oluşturma
```
PS C:\>New-AzureRmApiManagement -ResourceGroupName "ContosoGroup02 -Name "ContosoApi" -Location "Central US" -Organization "Contoso" -AdminEmail "admin@contoso.com" -Sku Standard -Capacity 3
```

Bu komut, üç birimli bir standart katman API yönetim hizmeti oluşturur.

### Örnek 3: dış sanal ağ için API yönetim hizmeti oluşturma
```
PS C:\> $virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location "West US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-b1e8-3726ab15d0e2/resourceGroups/ContosoGroup/providers/Microsoft.Network/virtualNetworks/westUsVirtualNetwork/subnets/backendSubnet"
PS C:\> New-AzureRmApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization Contoso -AdminEmail admin@contoso.com -VirtualNetwork $virtualNetwork -VpnType "External" -Sku "Premium"
```

Bu komut, bir Azure sanal ağ alt ağında, Batı ABD 'deki ana bölgeyle birlikte dış bir ağ geçidi uç noktası içeren bir Premium katman API yönetim hizmeti oluşturur.

### Örnek 4: iç sanal ağ için bir API yönetim hizmeti oluşturma
```
PS C:\> $virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location "West US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-b1e8-3726ab15d0e2/resourceGroups/ContosoGroup/providers/Microsoft.Network/virtualNetworks/westUsVirtualNetwork/subnets/backendSubnet"
PS C:\> New-AzureRmApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization "Contoso" -AdminEmail "admin@contoso.com" -VirtualNetwork $virtualNetwork -VpnType "Internal" -Sku "Premium"
```

Bu komut, bir Azure sanal ağ alt ağında, Batı ABD 'deki ana bölgeyle birlikte dahili bir ağ geçidi uç noktası içeren bir Premium katman API yönetim hizmeti oluşturur.

## PARAMETRELERINE

### -Additionalbölgelerle
Azure API yönetimi için ek dağıtım bölgeleri.

```yaml
Type: PsApiManagementRegion[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -AdminEmail
API yönetim sisteminin gönderdiği tüm bildirimler için kaynak e-posta adresini belirtir.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Kapasite
Azure API yönetim hizmetinin SKU kapasitesini belirtir.
Varsayılan değer bir (1).

```yaml
Type: Int32
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
API Yönetim hizmetini oluşturacağınız konumu belirtir.

Geçerli konumlar almak için, "Microsoft. Apsananae" Get-AzureRmResourceProvider cmdlet 'ini kullanın. WHERE {$ _. ResourceTypes [0]. ResourceTypeName-EQ "hizmet"} | Select-Object konumları

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Ad
API yönetim dağıtımı için bir ad belirtir.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Kuruluş
Kuruluşun adını belirtir.
API Yönetimi, bu adresi Geliştirici Portalında e-posta bildirimlerinde kullanır.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Bu cmdlet 'in API yönetim dağıtımını oluşturduğu kaynak grubun adını belirtir.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SKU
API yönetim hizmetinin katmanını belirtir.
Geçerli değerler: 

- İyle 
- Ardından 
- Min 

Varsayılan olarak geliştirici kullanılır.

```yaml
Type: PsApiManagementSku
Parameter Sets: (All)
Aliases:
Accepted values: Developer, Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### Etiketli
Etiket sözlüğü.

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VirtualNetwork
Master Azure API yönetim dağıtım bölgesinin sanal ağ yapılandırması.

```yaml
Type: PsApiManagementVirtualNetwork
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VpnType
Sanal ağ 'ın sanal ağ türü. Geçerli değerler 
- "None" (varsayılan değer. Herhangi bir sanal ağın parçası değildir ")
- "Dış" (bir Internet 'e yönelik uç noktaya sahip bir sanal ağın içinde bir kuruluş)
- "İç" (bir sanal ağın iç uç noktasına sahip olduğu bir sanal ağ içinde, kuruluş)

```yaml
Type: PsApiManagementVpnType
Parameter Sets: (All)
Aliases:
Accepted values: None, External, Internal

Required: False
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

### Microsoft. Azure. Commands. apsanana

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Yedek-azurermapı](./Backup-AzureRmApiManagement.md)

[Get-azurermapı](./Get-AzureRmApiManagement.md)

[Remove-azurermapsanana](./Remove-AzureRmApiManagement.md)

[Geri yükleme-azurermapı](./Restore-AzureRmApiManagement.md)


