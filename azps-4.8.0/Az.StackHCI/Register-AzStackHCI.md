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
# <span data-ttu-id="a5946-101">Register-AzStackHCI</span><span class="sxs-lookup"><span data-stu-id="a5946-101">Register-AzStackHCI</span></span>

## <span data-ttu-id="a5946-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a5946-102">SYNOPSIS</span></span>
<span data-ttu-id="a5946-103">Register-AzStackHCI, şirket içi kümeyi temsil eden bir Microsoft. AzureStackHCI bulut kaynağı oluşturur ve şirket içi kümeyi Azure ile kaydeder.</span><span class="sxs-lookup"><span data-stu-id="a5946-103">Register-AzStackHCI creates a Microsoft.AzureStackHCI cloud resource representing the on-premise cluster and registers the on-premise cluster with Azure.</span></span>

## <span data-ttu-id="a5946-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a5946-104">SYNTAX</span></span>

```
Register-AzStackHCI [-SubscriptionId] <String> [[-Region] <String>] [[-ResourceName] <String>]
 [[-TenantId] <String>] [[-ResourceGroupName] <String>] [[-ArmAccessToken] <String>]
 [[-GraphAccessToken] <String>] [[-AccountId] <String>] [[-EnvironmentName] <String>]
 [[-ComputerName] <String>] [[-Credential] <PSCredential>] [<CommonParameters>]
```

## <span data-ttu-id="a5946-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a5946-105">DESCRIPTION</span></span>
<span data-ttu-id="a5946-106">Register-AzStackHCI, şirket içi kümeyi temsil eden bir Microsoft. AzureStackHCI bulut kaynağı oluşturur ve şirket içi kümeyi Azure ile kaydeder.</span><span class="sxs-lookup"><span data-stu-id="a5946-106">Register-AzStackHCI creates a Microsoft.AzureStackHCI cloud resource representing the on-premise cluster and registers the on-premise cluster with Azure.</span></span>

## <span data-ttu-id="a5946-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a5946-107">EXAMPLES</span></span>

### <span data-ttu-id="a5946-108">ÖRNEK 1</span><span class="sxs-lookup"><span data-stu-id="a5946-108">EXAMPLE 1</span></span>
```
Invoking on one of the cluster node.
```

<span data-ttu-id="a5946-109">C:\PS \> register-AzStackHCI-SubscriptionID "12a0f531-56cb-4340-9501-257726vseç741fd" Result: Success RESOURCEID:/Subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster1-RG/Providers/Microsoft.AzureStackHCI/Clusters/DemoHCICluster1 PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster1-rg/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster1/overview PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/980be58d-578c-4cff-b4cd-43e9c3a77826/isMSAApp/</span><span class="sxs-lookup"><span data-stu-id="a5946-109">C:\PS\>Register-AzStackHCI -SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" Result: Success ResourceId: /subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster1-rg/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster1 PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster1-rg/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster1/overview PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/980be58d-578c-4cff-b4cd-43e9c3a77826/isMSAApp/</span></span>

### <span data-ttu-id="a5946-110">ÖRNEK 2</span><span class="sxs-lookup"><span data-stu-id="a5946-110">EXAMPLE 2</span></span>
```
Invoking from the management node
```

<span data-ttu-id="a5946-111">C:\PS \> register-AzStackHCI-SubscriptionID "12a0f531-56cb-4340-9501-257726vseç741fd"-ComputerName ClusterNode1 Result: Success RESOURCEID:/Subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster2-RG/Providers/Microsoft.AzureStackHCI/Clusters/DemoHCICluster2 PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster2-rg/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster2/overview PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/950be58d-578c-4cff-b4cd-43e9c3a77866/isMSAApp/</span><span class="sxs-lookup"><span data-stu-id="a5946-111">C:\PS\>Register-AzStackHCI -SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" -ComputerName ClusterNode1 Result: Success ResourceId: /subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster2-rg/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster2 PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster2-rg/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster2/overview PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/950be58d-578c-4cff-b4cd-43e9c3a77866/isMSAApp/</span></span>

### <span data-ttu-id="a5946-112">ÖRNEK 3</span><span class="sxs-lookup"><span data-stu-id="a5946-112">EXAMPLE 3</span></span>
```
Invoking from WAC
```

<span data-ttu-id="a5946-113">C:\PS \> register-AzStackHCI-SubscriptionID "12a0f531-56cb-4340-9501-257726vseç741fd"-ArmAccessToken etyer.. ere =-GraphAccessToken.. rerrer-AccountID user1@corp1.com -Region westus-resourceName DemoHCICluster3-ResourceGroupName DemoHCIRG Result: Pendingforadminonay RESOURCEID:/Subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCIRG/Providers/Microsoft.AzureStackHCI/Clusters/DemoHCICluster3 PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCIRG/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster3/overview PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/980be58d-578c-4cff-b4cd-43e9c3a77866/isMSAApp/</span><span class="sxs-lookup"><span data-stu-id="a5946-113">C:\PS\>Register-AzStackHCI -SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" -ArmAccessToken etyer..ere= -GraphAccessToken acyee..rerrer -AccountId user1@corp1.com -Region westus -ResourceName DemoHCICluster3 -ResourceGroupName DemoHCIRG Result: PendingForAdminConsent ResourceId: /subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCIRG/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster3 PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCIRG/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster3/overview PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/980be58d-578c-4cff-b4cd-43e9c3a77866/isMSAApp/</span></span>

### <span data-ttu-id="a5946-114">ÖRNEK 4</span><span class="sxs-lookup"><span data-stu-id="a5946-114">EXAMPLE 4</span></span>
```
Invoking with all the parameters
```

<span data-ttu-id="a5946-115">C:\PS \> register-AzStackHCI-SubscriptionID "12a0f531-56cb-4340-9501-257726vseç741fd"-Region westus-resourceName HciCluster1-tenanfilelist "c31c0dbb-ce27-4c78-ad26-a5f717c14557"-ResourceGroupName HciClusterRG-ArmAccessToken eerrer.. ... rerrer-AccountID user1@corp1.com -environmentname Azurecsesli-ComputerName node1hci-Credential Get-Credential Result: Success RESOURCEID:/Subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/HciClusterRG/Providers/Microsoft.AzureStackHCI/Clusters/HciCluster1 PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/HciClusterRG/providers/Microsoft.AzureStackHCI/clusters/HciCluster1/overview PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/990be58d-578c-4cff-b4cd-43e9c3a77866/isMSAApp/</span><span class="sxs-lookup"><span data-stu-id="a5946-115">C:\PS\>Register-AzStackHCI -SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" -Region westus -ResourceName HciCluster1 -TenantId "c31c0dbb-ce27-4c78-ad26-a5f717c14557" -ResourceGroupName HciClusterRG -ArmAccessToken eerrer..ere= -GraphAccessToken acee..rerrer -AccountId user1@corp1.com -EnvironmentName AzureCloud -ComputerName node1hci -Credential Get-Credential Result: Success ResourceId: /subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/HciClusterRG/providers/Microsoft.AzureStackHCI/clusters/HciCluster1 PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/HciClusterRG/providers/Microsoft.AzureStackHCI/clusters/HciCluster1/overview PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/990be58d-578c-4cff-b4cd-43e9c3a77866/isMSAApp/</span></span>

## <span data-ttu-id="a5946-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a5946-116">PARAMETERS</span></span>

### <span data-ttu-id="a5946-117">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="a5946-117">-SubscriptionId</span></span>
<span data-ttu-id="a5946-118">Kaynağı oluşturmak için Azure aboneliğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a5946-118">Specifies the Azure Subscription to create the resource.</span></span>
<span data-ttu-id="a5946-119">Bu, tek zorunlu parametredir.</span><span class="sxs-lookup"><span data-stu-id="a5946-119">This is the only Mandatory parameter.</span></span>

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

### <span data-ttu-id="a5946-120">-Bölge</span><span class="sxs-lookup"><span data-stu-id="a5946-120">-Region</span></span>
<span data-ttu-id="a5946-121">Kaynağın oluşturulacağı bölgeyi belirtir.</span><span class="sxs-lookup"><span data-stu-id="a5946-121">Specifies the Region to create the resource.</span></span>
<span data-ttu-id="a5946-122">Varsayılan EastUS.</span><span class="sxs-lookup"><span data-stu-id="a5946-122">Default is EastUS.</span></span>

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

### <span data-ttu-id="a5946-123">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="a5946-123">-ResourceName</span></span>
<span data-ttu-id="a5946-124">Azure 'da oluşturulan kaynağın kaynak adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a5946-124">Specifies the resource name of the resource created in Azure.</span></span>
<span data-ttu-id="a5946-125">Belirtilmemişse, şirket içi küme adı kullanılır.</span><span class="sxs-lookup"><span data-stu-id="a5946-125">If not specified, on-premise cluster name is used.</span></span>

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

### <span data-ttu-id="a5946-126">-Tenantıd</span><span class="sxs-lookup"><span data-stu-id="a5946-126">-TenantId</span></span>
<span data-ttu-id="a5946-127">Azure Tenantıd 'yi belirtir.</span><span class="sxs-lookup"><span data-stu-id="a5946-127">Specifies the Azure TenantId.</span></span>

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

### <span data-ttu-id="a5946-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5946-128">-ResourceGroupName</span></span>
<span data-ttu-id="a5946-129">Azure Resource grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a5946-129">Specifies the Azure Resource Group name.</span></span>
<span data-ttu-id="a5946-130">Belirtilmemişse \<LocalClusterName\> -RG kaynak grubu adı olarak kullanılır.</span><span class="sxs-lookup"><span data-stu-id="a5946-130">If not specified \<LocalClusterName\>-rg will be used as resource group name.</span></span>

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

### <span data-ttu-id="a5946-131">-ArmAccessToken</span><span class="sxs-lookup"><span data-stu-id="a5946-131">-ArmAccessToken</span></span>
<span data-ttu-id="a5946-132">ARM erişim belirtecini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a5946-132">Specifies the ARM access token.</span></span>
<span data-ttu-id="a5946-133">GraphAccessToken ve AccountID ile birlikte bunu belirtmek için Azure etkileşimli oturum açma önlenir.</span><span class="sxs-lookup"><span data-stu-id="a5946-133">Specifying this along with GraphAccessToken and AccountId will avoid Azure interactive logon.</span></span>

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

### <span data-ttu-id="a5946-134">-GraphAccessToken</span><span class="sxs-lookup"><span data-stu-id="a5946-134">-GraphAccessToken</span></span>
<span data-ttu-id="a5946-135">Grafik erişim belirtecini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a5946-135">Specifies the Graph access token.</span></span>
<span data-ttu-id="a5946-136">ArmAccessToken ve AccountID ile birlikte belirtmek için Azure etkileşimli oturum açma önlenir.</span><span class="sxs-lookup"><span data-stu-id="a5946-136">Specifying this along with ArmAccessToken and AccountId will avoid Azure interactive logon.</span></span>

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

### <span data-ttu-id="a5946-137">-AccountId</span><span class="sxs-lookup"><span data-stu-id="a5946-137">-AccountId</span></span>
<span data-ttu-id="a5946-138">ARM erişim belirtecini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a5946-138">Specifies the ARM access token.</span></span>
<span data-ttu-id="a5946-139">ArmAccessToken ve GraphAccessToken ile birlikte belirtmek için Azure etkileşimli oturum açma önlenir.</span><span class="sxs-lookup"><span data-stu-id="a5946-139">Specifying this along with ArmAccessToken and GraphAccessToken will avoid Azure interactive logon.</span></span>

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

### <span data-ttu-id="a5946-140">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="a5946-140">-EnvironmentName</span></span>
<span data-ttu-id="a5946-141">Azure ortamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a5946-141">Specifies the Azure Environment.</span></span>
<span data-ttu-id="a5946-142">Varsayılan olarak Azurecyüksek.</span><span class="sxs-lookup"><span data-stu-id="a5946-142">Default is AzureCloud.</span></span>
<span data-ttu-id="a5946-143">Geçerli değerler Azurecyüksek, AzureChinaCloud, AzureUSGovernment, AzureGermanCloud, AzurePPE</span><span class="sxs-lookup"><span data-stu-id="a5946-143">Valid values are AzureCloud, AzureChinaCloud, AzureUSGovernment, AzureGermanCloud, AzurePPE</span></span>

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

### <span data-ttu-id="a5946-144">-ComputerName</span><span class="sxs-lookup"><span data-stu-id="a5946-144">-ComputerName</span></span>
<span data-ttu-id="a5946-145">Azure 'a kaydolan şirket içi kümesindeki küme adını veya küme düğümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="a5946-145">Specifies the cluster name or one of the cluster node in on-premise cluster that is being registered to Azure.</span></span>

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

### <span data-ttu-id="a5946-146">-Credential</span><span class="sxs-lookup"><span data-stu-id="a5946-146">-Credential</span></span>
<span data-ttu-id="a5946-147">ComputerName kimlik bilgisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a5946-147">Specifies the credential for the ComputerName.</span></span>
<span data-ttu-id="a5946-148">Varsayılan, cmdlet 'ı yürüten geçerli kullanıcıdır.</span><span class="sxs-lookup"><span data-stu-id="a5946-148">Default is the current user executing the Cmdlet.</span></span>

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

### <span data-ttu-id="a5946-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5946-149">CommonParameters</span></span>
<span data-ttu-id="a5946-150">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a5946-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5946-151">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="a5946-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5946-152">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a5946-152">INPUTS</span></span>

## <span data-ttu-id="a5946-153">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a5946-153">OUTPUTS</span></span>

### <span data-ttu-id="a5946-154">PSCustomObject.</span><span class="sxs-lookup"><span data-stu-id="a5946-154">PSCustomObject.</span></span> <span data-ttu-id="a5946-155">PSCustomObject 'de aşağıdaki özellikleri döndürür</span><span class="sxs-lookup"><span data-stu-id="a5946-155">Returns following Properties in PSCustomObject</span></span>
### <span data-ttu-id="a5946-156">Sonuç: başarı veya başarısız ya da Beklemeforadminonay veya Iptal edildi.</span><span class="sxs-lookup"><span data-stu-id="a5946-156">Result: Success or Failed or PendingForAdminConsent or Cancelled.</span></span>
### <span data-ttu-id="a5946-157">RESOURCEID: Azure 'da oluşturulan kaynağın kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="a5946-157">ResourceId: Resource ID of the resource created in Azure.</span></span>
### <span data-ttu-id="a5946-158">PortalResourceURL: Azure Portal kaynak URL 'SI.</span><span class="sxs-lookup"><span data-stu-id="a5946-158">PortalResourceURL: Azure Portal Resource URL.</span></span>
### <span data-ttu-id="a5946-159">PortalAADAppPermissionsURL: AAD uygulama izinleri sayfası için Azure Portal URL 'SI.</span><span class="sxs-lookup"><span data-stu-id="a5946-159">PortalAADAppPermissionsURL: Azure Portal URL for AAD App permissions page.</span></span>
## <span data-ttu-id="a5946-160">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a5946-160">NOTES</span></span>

## <span data-ttu-id="a5946-161">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a5946-161">RELATED LINKS</span></span>
