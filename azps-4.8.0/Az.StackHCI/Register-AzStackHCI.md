---
external help file: Az.StackHCI-help.xml
Module Name: Az.StackHCI
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackhci/register-azstackhci
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Register-AzStackHCI.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Register-AzStackHCI.md
ms.openlocfilehash: c09c4b4c8d71d90bbbac0771c75ea3ea51ee05dc
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94268669"
---
# Register-AzStackHCI

## SYNOPSIS
Register-AzStackHCI, şirket içi kümeyi temsil eden bir Microsoft. AzureStackHCI bulut kaynağı oluşturur ve şirket içi kümeyi Azure ile kaydeder.

## INDEKI

```
Register-AzStackHCI [-SubscriptionId] <String> [[-Region] <String>] [[-ResourceName] <String>]
 [[-TenantId] <String>] [[-ResourceGroupName] <String>] [[-ArmAccessToken] <String>]
 [[-GraphAccessToken] <String>] [[-AccountId] <String>] [[-EnvironmentName] <String>]
 [[-ComputerName] <String>] [[-Credential] <PSCredential>] [<CommonParameters>]
```

## Tanım
Register-AzStackHCI, şirket içi kümeyi temsil eden bir Microsoft. AzureStackHCI bulut kaynağı oluşturur ve şirket içi kümeyi Azure ile kaydeder.

## ÖRNEKLERDEN

### ÖRNEK 1
```
Invoking on one of the cluster node.
```

C:\PS \> register-AzStackHCI-SubscriptionID "12a0f531-56cb-4340-9501-257726vseç741fd" Result: Success RESOURCEID:/Subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster1-RG/Providers/Microsoft.AzureStackHCI/Clusters/DemoHCICluster1 PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster1-rg/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster1/overview PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/980be58d-578c-4cff-b4cd-43e9c3a77826/isMSAApp/

### ÖRNEK 2
```
Invoking from the management node
```

C:\PS \> register-AzStackHCI-SubscriptionID "12a0f531-56cb-4340-9501-257726vseç741fd"-ComputerName ClusterNode1 Result: Success RESOURCEID:/Subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster2-RG/Providers/Microsoft.AzureStackHCI/Clusters/DemoHCICluster2 PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster2-rg/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster2/overview PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/950be58d-578c-4cff-b4cd-43e9c3a77866/isMSAApp/

### ÖRNEK 3
```
Invoking from WAC
```

C:\PS \> register-AzStackHCI-SubscriptionID "12a0f531-56cb-4340-9501-257726vseç741fd"-ArmAccessToken etyer.. ere =-GraphAccessToken.. rerrer-AccountID user1@corp1.com -Region westus-resourceName DemoHCICluster3-ResourceGroupName DemoHCIRG Result: Pendingforadminonay RESOURCEID:/Subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCIRG/Providers/Microsoft.AzureStackHCI/Clusters/DemoHCICluster3 PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCIRG/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster3/overview PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/980be58d-578c-4cff-b4cd-43e9c3a77866/isMSAApp/

### ÖRNEK 4
```
Invoking with all the parameters
```

C:\PS \> register-AzStackHCI-SubscriptionID "12a0f531-56cb-4340-9501-257726vseç741fd"-Region westus-resourceName HciCluster1-tenanfilelist "c31c0dbb-ce27-4c78-ad26-a5f717c14557"-ResourceGroupName HciClusterRG-ArmAccessToken eerrer.. ... rerrer-AccountID user1@corp1.com -environmentname Azurecsesli-ComputerName node1hci-Credential Get-Credential Result: Success RESOURCEID:/Subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/HciClusterRG/Providers/Microsoft.AzureStackHCI/Clusters/HciCluster1 PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/HciClusterRG/providers/Microsoft.AzureStackHCI/clusters/HciCluster1/overview PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/990be58d-578c-4cff-b4cd-43e9c3a77866/isMSAApp/

## PARAMETRELERINE

### -SubscriptionID
Kaynağı oluşturmak için Azure aboneliğini belirtir.
Bu, tek zorunlu parametredir.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Bölge
Kaynağın oluşturulacağı bölgeyi belirtir.
Varsayılan EastUS.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceName
Azure 'da oluşturulan kaynağın kaynak adını belirtir.
Belirtilmemişse, şirket içi küme adı kullanılır.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Tenantıd
Azure Tenantıd 'yi belirtir.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Azure Resource grubunun adını belirtir.
Belirtilmemişse \<LocalClusterName\> -RG kaynak grubu adı olarak kullanılır.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ArmAccessToken
ARM erişim belirtecini belirtir.
GraphAccessToken ve AccountID ile birlikte bunu belirtmek için Azure etkileşimli oturum açma önlenir.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -GraphAccessToken
Grafik erişim belirtecini belirtir.
ArmAccessToken ve AccountID ile birlikte belirtmek için Azure etkileşimli oturum açma önlenir.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AccountId
ARM erişim belirtecini belirtir.
ArmAccessToken ve GraphAccessToken ile birlikte belirtmek için Azure etkileşimli oturum açma önlenir.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnvironmentName
Azure ortamını belirtir.
Varsayılan olarak Azurecyüksek.
Geçerli değerler Azurecyüksek, AzureChinaCloud, AzureUSGovernment, AzureGermanCloud, AzurePPE

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: $AzureCloud
Accept pipeline input: False
Accept wildcard characters: False
```

### -ComputerName
Azure 'a kaydolan şirket içi kümesindeki küme adını veya küme düğümünü belirtir.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Credential
ComputerName kimlik bilgisini belirtir.
Varsayılan, cmdlet 'ı yürüten geçerli kullanıcıdır.

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: 11
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.

## GÖLGELENDIRICI

## ÇıKıŞLAR

### PSCustomObject. PSCustomObject 'de aşağıdaki özellikleri döndürür
### Sonuç: başarı veya başarısız ya da Beklemeforadminonay veya Iptal edildi.
### RESOURCEID: Azure 'da oluşturulan kaynağın kaynak KIMLIĞI.
### PortalResourceURL: Azure Portal kaynak URL 'SI.
### PortalAADAppPermissionsURL: AAD uygulama izinleri sayfası için Azure Portal URL 'SI.
## NOTLARıNDA

## ILGILI BAĞLANTıLAR
