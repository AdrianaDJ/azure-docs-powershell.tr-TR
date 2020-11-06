---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 56604912-53A0-496D-9BDC-472BCE45A6A2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/update-azurermapimanagementdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Update-AzureRmApiManagementDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Update-AzureRmApiManagementDeployment.md
ms.openlocfilehash: f8f0273ab624cd81488734f9b84debc045f6fed2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587322"
---
# Update-AzureRmApiManagementDeployment

## SYNOPSIS
Bir API yönetim hizmetinin dağıtımını güncelleştirir.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

### UpdateSpecificService (varsayılan)
```
Update-AzureRmApiManagementDeployment -ResourceGroupName <String> -Name <String> -Location <String>
 -Sku <PsApiManagementSku> -Capacity <Int32> [-VirtualNetwork <PsApiManagementVirtualNetwork>]
 [-VpnType <PsApiManagementVpnType>]
 [-AdditionalRegions <System.Collections.Generic.IList`1[Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion]>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Updatefrompsapsananagementınstance
```
Update-AzureRmApiManagementDeployment -ApiManagement <PsApiManagement> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Güncelleştirme-Azurermapımanagementdeployment** cmdlet 'i, bir API yönetim hizmetinin geçerli dağıtımlarını güncelleştirir.

## ÖRNEKLERDEN

### Örnek 1: bir anlık ileti örneğinin dağıtımını güncelleştirme
```powershell
PS C:\>Update-AzureRmApiManagementDeployment -ResourceGroupName "Contoso" -Name "ContosoApi" -Sku "Standard" -Capacity 3
```

Bu komut, API yönetim örneğinin dağıtımını üç birim kapasite standardına göre güncelleştirir.

### Örnek 2: bir anlık ileti alma ve yeniden boyutlandırma
```powershell
PS C:\>$ApiManagement = Get-AzureRmApiManagement -ResourceGroupName "Contoso" -Name "ContosoApi"
PS C:\> $ApiManagement.Sku = "Premium"
PS C:\> $ApiManagement.Capacity = 5
PS C:\> $ApiManagement.AddRegion("Central US", "Premium", 3)
PS C:\> Update-AzureRmApiManagementDeployment -ApiManagement $ApiManagement
```

Bu örnekte bir API yönetim örneği alınır, bunu beş Premium birime ölçeklendirir ve Premium bölgeye ek üç birim ekler.

### Örnek 3: güncelleştirme dağıtımı (dış VNET)
```powershell
PS C:\> $virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location "East US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-a1e8-3726ab15d0e2/resourceGroups/Api-Default-WestUS/providers/Microsoft.Network/virtualNetworks/dfVirtualNetwork/subnets/backendSubnet"
PS C:\> Update-AzureRmApiManagementDeployment -ResourceGroupName "ContosoGroup" -Name "ContosoApi" -VirtualNetwork $virtualNetwork -VpnType "External"
```

Bu komut, var olan bir API yönetim dağıtımını güncelleştirir ve bir dış *Vpntype* 'a katılır.

### Örnek 4: güncelleştirme dağıtımı (iç VNET)
```powershell
PS C:\> $virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location "East US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-a1e8-3726ab15d0e2/resourceGroups/Api-Default-WestUS/providers/Microsoft.ClassicNetwork/virtualNetworks/dfVirtualNetwork/subnets/backendSubnet"
PS C:\> Update-AzureRmApiManagementDeployment -ResourceGroupName "ContosoGroup" -Name "ContosoApi" -VirtualNetwork $virtualNetwork -VpnType "Internal"
```

Bu komut, var olan bir API yönetim dağıtımını güncelleştirir ve bir iç *Vpntype* 'a katılır.

## PARAMETRELERINE

### -Additionalbölgelerle
Azure API Yönetimi 'nin ek dağıtım bölgelerini belirtir.

```yaml
Type: System.Collections.Generic.IList`1[Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion]
Parameter Sets: UpdateSpecificService
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Ucuz
Dağıtım yapılandırmasını almak için **Psapimana,** örneğini belirtir.
Örnekte gerekli tüm değişiklikler varsa bu parametreyi kullanın.

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement
Parameter Sets: UpdateFromPsApiManagementInstance
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Kapasite
Ana Azure API Yönetimi dağıtım bölgesinin SKU kapasitesini belirtir.

```yaml
Type: System.Int32
Parameter Sets: UpdateSpecificService
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
Master API Yönetimi dağıtım bölgesinin konumunu belirtir.
Geçerli konumlar almak için, "Microsoft. Apsananae" Get-AzureRmResourceProvider cmdlet 'ini kullanın. WHERE {$ _. ResourceTypes [0]. ResourceTypeName-EQ "hizmet"} | Select-Object konumları

```yaml
Type: System.String
Parameter Sets: UpdateSpecificService
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Ad
Bu cmdlet 'in güncelleştirdiği API yönetiminin adını belirtir.

```yaml
Type: System.String
Parameter Sets: UpdateSpecificService
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Geçiş
Çalıştığınız öğeyi temsil eden bir nesne döndürür.
Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
API yönetiminin altında bulunduğu kaynak grubunun adını belirtir.

```yaml
Type: System.String
Parameter Sets: UpdateSpecificService
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SKU
Ana Azure API Yönetimi dağıtım bölgesinin katmanını belirtir.
Bu parametre için kabul edilebilir değerler şunlardır:
- İyle
- Ardından
- Min

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku
Parameter Sets: UpdateSpecificService
Aliases:
Accepted values: Developer, Standard, Premium, Basic

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VirtualNetwork
Ana Azure API Yönetimi dağıtım bölgesinin sanal ağ yapılandırmasını belirtir.

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork
Parameter Sets: UpdateSpecificService
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VpnType
API yönetim dağıtımının sanal ağ türünü belirtir.
Bu parametre için kabul edilebilir değerler şunlardır:
- Yabilirsiniz.
API yönetim dağıtımı hiçbir sanal ağın parçası değildir.
Bu varsayılan değerdir. 
- External.
API yönetim dağıtımında dış bir açık sanal adres vardır. 
- Ýç.
API yönetim dağıtımında, bir intranete bağlanan sanal adres vardır.

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVpnType
Parameter Sets: UpdateSpecificService
Aliases:
Accepted values: None, External, Internal

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

### Microsoft. Azure. Commands. apsananad

### System. Koleksiyonlar. Generic. IList ' 1 [[Microsoft. Azure. Commands. Apsananad. modeller. Psapsananagementregion, Microsoft. Azure. Commands. Apsananad, Version = 6.1.2.0, Culture = neutral, PublicKeyToken = null]]

## ÇıKıŞLAR

### Microsoft. Azure. Commands. apsanana

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-azurermapı](./Get-AzureRmApiManagement.md)


