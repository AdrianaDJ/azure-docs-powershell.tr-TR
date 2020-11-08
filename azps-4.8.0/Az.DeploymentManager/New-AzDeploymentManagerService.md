---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/new-azdeploymentmanagerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerService.md
ms.openlocfilehash: aec721a3676a6b4510c7fe0eccf5badc4f9ccce2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94275016"
---
# <span data-ttu-id="cca88-101">New-AzDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="cca88-101">New-AzDeploymentManagerService</span></span>

## <span data-ttu-id="cca88-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cca88-102">SYNOPSIS</span></span>
<span data-ttu-id="cca88-103">Belirtilen hizmet topolojisi altında bir hizmet oluşturur.</span><span class="sxs-lookup"><span data-stu-id="cca88-103">Creates a service under the specified service topology.</span></span>

## <span data-ttu-id="cca88-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="cca88-104">SYNTAX</span></span>

### <span data-ttu-id="cca88-105">Etkileşimli (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="cca88-105">Interactive (Default)</span></span>
```
New-AzDeploymentManagerService [-ResourceGroupName] <String> [-ServiceTopologyName] <String> -Name <String>
 -Location <String> -TargetLocation <String> -TargetSubscriptionId <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cca88-106">ByServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="cca88-106">ByServiceTopologyObject</span></span>
```
New-AzDeploymentManagerService [-ResourceGroupName] <String> -Name <String> -Location <String>
 -TargetLocation <String> -TargetSubscriptionId <String> [-ServiceTopologyObject] <PSServiceTopologyResource>
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cca88-107">Byservicetopologyresourceıd</span><span class="sxs-lookup"><span data-stu-id="cca88-107">ByServiceTopologyResourceId</span></span>
```
New-AzDeploymentManagerService [-ResourceGroupName] <String> -Name <String> -Location <String>
 -TargetLocation <String> -TargetSubscriptionId <String> [-ServiceTopologyId] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cca88-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="cca88-108">DESCRIPTION</span></span>
<span data-ttu-id="cca88-109">**Yeni-AzDeploymentManagerService** cmdlet 'i hizmet topolojisi altında bir hizmet oluşturur ve bu hizmeti temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="cca88-109">The **New-AzDeploymentManagerService** cmdlet creates a service under a service topology, and returns an object that represents that service.</span></span>
<span data-ttu-id="cca88-110">Hizmeti adına, hizmet topolojisine ve kaynak grubu adına göre belirtin.</span><span class="sxs-lookup"><span data-stu-id="cca88-110">Specify the service by its name, service topology it is in and the resource group name.</span></span> 

<span data-ttu-id="cca88-111">Cmdlet bir hizmet nesnesi döndürür.</span><span class="sxs-lookup"><span data-stu-id="cca88-111">The cmdlet returns a Service object.</span></span> <span data-ttu-id="cca88-112">Bu nesneyi yerel olarak değiştirebilir ve Set-AzDeploymentManagerService cmdlet 'ini kullanarak değişiklikleri hizmete uygulayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="cca88-112">You can modify this object locally, and then apply changes to the service by using the Set-AzDeploymentManagerService cmdlet.</span></span>

## <span data-ttu-id="cca88-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="cca88-113">EXAMPLES</span></span>

### <span data-ttu-id="cca88-114">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="cca88-114">Example 1</span></span>
```powershell
PS C:\> New-AzDeploymentManagerService -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology -Name ContosoService1 -Location "Central US" -TargetLocation "East US" -TargetSubscriptionId XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
```

<span data-ttu-id="cca88-115">Hizmet topolojisi altında ad ContosoService1 içeren yeni bir hizmet oluştururken, ABD 'deki konum Merkezi</span><span class="sxs-lookup"><span data-stu-id="cca88-115">Creates a new service with name ContosoService1 under service topology ContosoServiceTopology in Resource Group ContosoResourceGroup, in the location Central US.</span></span> <span data-ttu-id="cca88-116">TargetLocation özelliği, hizmet ContosoService1 'in belirtilen abonelikteki Doğu US bölgesine dağıtılması gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="cca88-116">The TargetLocation property indicates that the service ContosoService1 should be deployed to the East US region in the subscription specified.</span></span>

## <span data-ttu-id="cca88-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="cca88-117">PARAMETERS</span></span>

### <span data-ttu-id="cca88-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cca88-118">-DefaultProfile</span></span>
<span data-ttu-id="cca88-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="cca88-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cca88-120">-Konum</span><span class="sxs-lookup"><span data-stu-id="cca88-120">-Location</span></span>
<span data-ttu-id="cca88-121">Hizmet kaynağının konumu.</span><span class="sxs-lookup"><span data-stu-id="cca88-121">The location of the service resource.</span></span>

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

### <span data-ttu-id="cca88-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="cca88-122">-Name</span></span>
<span data-ttu-id="cca88-123">Hizmetin adı.</span><span class="sxs-lookup"><span data-stu-id="cca88-123">The name of the service.</span></span>

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

### <span data-ttu-id="cca88-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cca88-124">-ResourceGroupName</span></span>
<span data-ttu-id="cca88-125">Kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="cca88-125">The resource group.</span></span>

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

### <span data-ttu-id="cca88-126">-Servicetopologyıd</span><span class="sxs-lookup"><span data-stu-id="cca88-126">-ServiceTopologyId</span></span>
<span data-ttu-id="cca88-127">Hizmetin oluşturulması gereken hizmet topolojisi kaynak tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="cca88-127">The service topology resource identifier in which the service should be created.</span></span>

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

### <span data-ttu-id="cca88-128">-ServiceTopologyName</span><span class="sxs-lookup"><span data-stu-id="cca88-128">-ServiceTopologyName</span></span>
<span data-ttu-id="cca88-129">Bu hizmetin ait olduğu hizmet topolojisinin adı.</span><span class="sxs-lookup"><span data-stu-id="cca88-129">The name of the service topology this service belongs to.</span></span>

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

### <span data-ttu-id="cca88-130">-ServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="cca88-130">-ServiceTopologyObject</span></span>
<span data-ttu-id="cca88-131">Hizmetin oluşturulması gereken hizmet topolojisi nesnesi.</span><span class="sxs-lookup"><span data-stu-id="cca88-131">The service topology object in which the service should be created.</span></span>

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

### <span data-ttu-id="cca88-132">Etiketli</span><span class="sxs-lookup"><span data-stu-id="cca88-132">-Tag</span></span>
<span data-ttu-id="cca88-133">Kaynak etiketlerini temsil eden karma bir tablo.</span><span class="sxs-lookup"><span data-stu-id="cca88-133">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="cca88-134">-TargetLocation</span><span class="sxs-lookup"><span data-stu-id="cca88-134">-TargetLocation</span></span>
<span data-ttu-id="cca88-135">Hizmetin altındaki kaynakların dağıtılacağı konumu belirler.</span><span class="sxs-lookup"><span data-stu-id="cca88-135">Determines the location where resources under the service would be deployed to.</span></span>

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

### <span data-ttu-id="cca88-136">-Targetsubscriptionıd</span><span class="sxs-lookup"><span data-stu-id="cca88-136">-TargetSubscriptionId</span></span>
<span data-ttu-id="cca88-137">Hizmetin altındaki kaynakların dağıtılacağı aboneliği belirler.</span><span class="sxs-lookup"><span data-stu-id="cca88-137">Determines the subscription to which resources under the service would be deployed to.</span></span>

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

### <span data-ttu-id="cca88-138">-Onay</span><span class="sxs-lookup"><span data-stu-id="cca88-138">-Confirm</span></span>
<span data-ttu-id="cca88-139">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="cca88-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cca88-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cca88-140">-WhatIf</span></span>
<span data-ttu-id="cca88-141">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="cca88-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cca88-142">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="cca88-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cca88-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cca88-143">CommonParameters</span></span>
<span data-ttu-id="cca88-144">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="cca88-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cca88-145">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="cca88-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cca88-146">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="cca88-146">INPUTS</span></span>

### <span data-ttu-id="cca88-147">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="cca88-147">System.Collections.Hashtable</span></span>

## <span data-ttu-id="cca88-148">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="cca88-148">OUTPUTS</span></span>

### <span data-ttu-id="cca88-149">Microsoft. Azure. Commands. DeploymentManager. modeller. PSServiceResource</span><span class="sxs-lookup"><span data-stu-id="cca88-149">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span></span>

## <span data-ttu-id="cca88-150">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="cca88-150">NOTES</span></span>

## <span data-ttu-id="cca88-151">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="cca88-151">RELATED LINKS</span></span>
