---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/new-azdeploymentmanagerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerService.md
ms.openlocfilehash: aec721a3676a6b4510c7fe0eccf5badc4f9ccce2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94104382"
---
# <span data-ttu-id="27a5f-101">New-AzDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="27a5f-101">New-AzDeploymentManagerService</span></span>

## <span data-ttu-id="27a5f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="27a5f-102">SYNOPSIS</span></span>
<span data-ttu-id="27a5f-103">Belirtilen hizmet topolojisi altında bir hizmet oluşturur.</span><span class="sxs-lookup"><span data-stu-id="27a5f-103">Creates a service under the specified service topology.</span></span>

## <span data-ttu-id="27a5f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="27a5f-104">SYNTAX</span></span>

### <span data-ttu-id="27a5f-105">Etkileşimli (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="27a5f-105">Interactive (Default)</span></span>
```
New-AzDeploymentManagerService [-ResourceGroupName] <String> [-ServiceTopologyName] <String> -Name <String>
 -Location <String> -TargetLocation <String> -TargetSubscriptionId <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="27a5f-106">ByServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="27a5f-106">ByServiceTopologyObject</span></span>
```
New-AzDeploymentManagerService [-ResourceGroupName] <String> -Name <String> -Location <String>
 -TargetLocation <String> -TargetSubscriptionId <String> [-ServiceTopologyObject] <PSServiceTopologyResource>
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="27a5f-107">Byservicetopologyresourceıd</span><span class="sxs-lookup"><span data-stu-id="27a5f-107">ByServiceTopologyResourceId</span></span>
```
New-AzDeploymentManagerService [-ResourceGroupName] <String> -Name <String> -Location <String>
 -TargetLocation <String> -TargetSubscriptionId <String> [-ServiceTopologyId] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="27a5f-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="27a5f-108">DESCRIPTION</span></span>
<span data-ttu-id="27a5f-109">**Yeni-AzDeploymentManagerService** cmdlet 'i hizmet topolojisi altında bir hizmet oluşturur ve bu hizmeti temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="27a5f-109">The **New-AzDeploymentManagerService** cmdlet creates a service under a service topology, and returns an object that represents that service.</span></span>
<span data-ttu-id="27a5f-110">Hizmeti adına, hizmet topolojisine ve kaynak grubu adına göre belirtin.</span><span class="sxs-lookup"><span data-stu-id="27a5f-110">Specify the service by its name, service topology it is in and the resource group name.</span></span> 

<span data-ttu-id="27a5f-111">Cmdlet bir hizmet nesnesi döndürür.</span><span class="sxs-lookup"><span data-stu-id="27a5f-111">The cmdlet returns a Service object.</span></span> <span data-ttu-id="27a5f-112">Bu nesneyi yerel olarak değiştirebilir ve Set-AzDeploymentManagerService cmdlet 'ini kullanarak değişiklikleri hizmete uygulayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="27a5f-112">You can modify this object locally, and then apply changes to the service by using the Set-AzDeploymentManagerService cmdlet.</span></span>

## <span data-ttu-id="27a5f-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="27a5f-113">EXAMPLES</span></span>

### <span data-ttu-id="27a5f-114">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="27a5f-114">Example 1</span></span>
```powershell
PS C:\> New-AzDeploymentManagerService -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology -Name ContosoService1 -Location "Central US" -TargetLocation "East US" -TargetSubscriptionId XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
```

<span data-ttu-id="27a5f-115">Hizmet topolojisi altında ad ContosoService1 içeren yeni bir hizmet oluştururken, ABD 'deki konum Merkezi</span><span class="sxs-lookup"><span data-stu-id="27a5f-115">Creates a new service with name ContosoService1 under service topology ContosoServiceTopology in Resource Group ContosoResourceGroup, in the location Central US.</span></span> <span data-ttu-id="27a5f-116">TargetLocation özelliği, hizmet ContosoService1 'in belirtilen abonelikteki Doğu US bölgesine dağıtılması gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="27a5f-116">The TargetLocation property indicates that the service ContosoService1 should be deployed to the East US region in the subscription specified.</span></span>

## <span data-ttu-id="27a5f-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="27a5f-117">PARAMETERS</span></span>

### <span data-ttu-id="27a5f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27a5f-118">-DefaultProfile</span></span>
<span data-ttu-id="27a5f-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="27a5f-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="27a5f-120">-Konum</span><span class="sxs-lookup"><span data-stu-id="27a5f-120">-Location</span></span>
<span data-ttu-id="27a5f-121">Hizmet kaynağının konumu.</span><span class="sxs-lookup"><span data-stu-id="27a5f-121">The location of the service resource.</span></span>

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

### <span data-ttu-id="27a5f-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="27a5f-122">-Name</span></span>
<span data-ttu-id="27a5f-123">Hizmetin adı.</span><span class="sxs-lookup"><span data-stu-id="27a5f-123">The name of the service.</span></span>

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

### <span data-ttu-id="27a5f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="27a5f-124">-ResourceGroupName</span></span>
<span data-ttu-id="27a5f-125">Kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="27a5f-125">The resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27a5f-126">-Servicetopologyıd</span><span class="sxs-lookup"><span data-stu-id="27a5f-126">-ServiceTopologyId</span></span>
<span data-ttu-id="27a5f-127">Hizmetin oluşturulması gereken hizmet topolojisi kaynak tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="27a5f-127">The service topology resource identifier in which the service should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: ByServiceTopologyResourceId
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27a5f-128">-ServiceTopologyName</span><span class="sxs-lookup"><span data-stu-id="27a5f-128">-ServiceTopologyName</span></span>
<span data-ttu-id="27a5f-129">Bu hizmetin ait olduğu hizmet topolojisinin adı.</span><span class="sxs-lookup"><span data-stu-id="27a5f-129">The name of the service topology this service belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27a5f-130">-ServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="27a5f-130">-ServiceTopologyObject</span></span>
<span data-ttu-id="27a5f-131">Hizmetin oluşturulması gereken hizmet topolojisi nesnesi.</span><span class="sxs-lookup"><span data-stu-id="27a5f-131">The service topology object in which the service should be created.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource
Parameter Sets: ByServiceTopologyObject
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27a5f-132">Etiketli</span><span class="sxs-lookup"><span data-stu-id="27a5f-132">-Tag</span></span>
<span data-ttu-id="27a5f-133">Kaynak etiketlerini temsil eden karma bir tablo.</span><span class="sxs-lookup"><span data-stu-id="27a5f-133">A hash table which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27a5f-134">-TargetLocation</span><span class="sxs-lookup"><span data-stu-id="27a5f-134">-TargetLocation</span></span>
<span data-ttu-id="27a5f-135">Hizmetin altındaki kaynakların dağıtılacağı konumu belirler.</span><span class="sxs-lookup"><span data-stu-id="27a5f-135">Determines the location where resources under the service would be deployed to.</span></span>

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

### <span data-ttu-id="27a5f-136">-Targetsubscriptionıd</span><span class="sxs-lookup"><span data-stu-id="27a5f-136">-TargetSubscriptionId</span></span>
<span data-ttu-id="27a5f-137">Hizmetin altındaki kaynakların dağıtılacağı aboneliği belirler.</span><span class="sxs-lookup"><span data-stu-id="27a5f-137">Determines the subscription to which resources under the service would be deployed to.</span></span>

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

### <span data-ttu-id="27a5f-138">-Onay</span><span class="sxs-lookup"><span data-stu-id="27a5f-138">-Confirm</span></span>
<span data-ttu-id="27a5f-139">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="27a5f-139">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27a5f-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="27a5f-140">-WhatIf</span></span>
<span data-ttu-id="27a5f-141">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="27a5f-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="27a5f-142">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="27a5f-142">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27a5f-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27a5f-143">CommonParameters</span></span>
<span data-ttu-id="27a5f-144">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="27a5f-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27a5f-145">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="27a5f-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27a5f-146">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="27a5f-146">INPUTS</span></span>

### <span data-ttu-id="27a5f-147">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="27a5f-147">System.Collections.Hashtable</span></span>

## <span data-ttu-id="27a5f-148">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="27a5f-148">OUTPUTS</span></span>

### <span data-ttu-id="27a5f-149">Microsoft. Azure. Commands. DeploymentManager. modeller. PSServiceResource</span><span class="sxs-lookup"><span data-stu-id="27a5f-149">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span></span>

## <span data-ttu-id="27a5f-150">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="27a5f-150">NOTES</span></span>

## <span data-ttu-id="27a5f-151">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="27a5f-151">RELATED LINKS</span></span>
