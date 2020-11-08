---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/remove-azdeploymentmanagerservicetopology
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerServiceTopology.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerServiceTopology.md
ms.openlocfilehash: 7323883028d062cf11f4e1befe1ea42cb1f8bcb2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94104399"
---
# <span data-ttu-id="65bed-101">Remove-AzDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="65bed-101">Remove-AzDeploymentManagerServiceTopology</span></span>

## <span data-ttu-id="65bed-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="65bed-102">SYNOPSIS</span></span>
<span data-ttu-id="65bed-103">Hizmet topolojisini siler.</span><span class="sxs-lookup"><span data-stu-id="65bed-103">Deletes the service topology.</span></span> <span data-ttu-id="65bed-104">Hizmet topolojisi altında oluşturulan hizmetlerin, hizmet topolojisini silmeden önce silinmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="65bed-104">All services created under a service topology need to be deleted before deleting the service topology.</span></span>

## <span data-ttu-id="65bed-105">INDEKI</span><span class="sxs-lookup"><span data-stu-id="65bed-105">SYNTAX</span></span>

### <span data-ttu-id="65bed-106">Etkileşimli (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="65bed-106">Interactive (Default)</span></span>
```
Remove-AzDeploymentManagerServiceTopology [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="65bed-107">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="65bed-107">ResourceId</span></span>
```
Remove-AzDeploymentManagerServiceTopology [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="65bed-108">InputObject</span><span class="sxs-lookup"><span data-stu-id="65bed-108">InputObject</span></span>
```
Remove-AzDeploymentManagerServiceTopology [-InputObject] <PSServiceTopologyResource> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="65bed-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="65bed-109">DESCRIPTION</span></span>
<span data-ttu-id="65bed-110">**Remove-AzDeploymentManagerServiceTopology** cmdlet 'i bir hizmet topolojisini siler.</span><span class="sxs-lookup"><span data-stu-id="65bed-110">The **Remove-AzDeploymentManagerServiceTopology** cmdlet deletes a service topology.</span></span>

<span data-ttu-id="65bed-111">Hizmet topolojisini adına ve kaynak grubu adına göre belirtin.</span><span class="sxs-lookup"><span data-stu-id="65bed-111">Specify the service topology by its name and the resource group name.</span></span> <span data-ttu-id="65bed-112">Alternatif olarak, ServiceTopology nesnesini veya RESOURCEID 'yi de sağlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="65bed-112">Alternately, you can provide the ServiceTopology object or the ResourceId.</span></span>

## <span data-ttu-id="65bed-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="65bed-113">EXAMPLES</span></span>

### <span data-ttu-id="65bed-114">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="65bed-114">Example 1</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerServiceTopology -ResourceGroupName ContosoResourceGroup -Name ContosoServiceTopology
```

<span data-ttu-id="65bed-115">Bu komut, ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="65bed-115">This command deletes a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="65bed-116">Örnek 2: kaynak tanımlayıcısını kullanarak hizmet topolojisini silme.</span><span class="sxs-lookup"><span data-stu-id="65bed-116">Example 2: Delete a service topology using the resource identifier.</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerServiceTopology -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology"
```

<span data-ttu-id="65bed-117">Bu komut, ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="65bed-117">This command deletes a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="65bed-118">Örnek 3: hizmet topolojisi nesnesini kullanarak hizmet topolojisini silme.</span><span class="sxs-lookup"><span data-stu-id="65bed-118">Example 3: Delete a service topology using the service topology object.</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerService -InputObject $serviceTopologyObject
```

<span data-ttu-id="65bed-119">Bu komut, adı ve ResourceGroup 'in sırasıyla $serviceTopologyObject Name ve ResourceGroupName özellikleriyle eşleşen bir hizmet topolojisini siler.</span><span class="sxs-lookup"><span data-stu-id="65bed-119">This command deletes a service topology whose name and ResourceGroup match the Name and ResourceGroupName properties of the $serviceTopologyObject, respectively.</span></span>

## <span data-ttu-id="65bed-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="65bed-120">PARAMETERS</span></span>

### <span data-ttu-id="65bed-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65bed-121">-DefaultProfile</span></span>
<span data-ttu-id="65bed-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="65bed-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="65bed-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="65bed-123">-InputObject</span></span>
<span data-ttu-id="65bed-124">Kaldırılacak kaynak.</span><span class="sxs-lookup"><span data-stu-id="65bed-124">The resource to be removed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="65bed-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="65bed-125">-Name</span></span>
<span data-ttu-id="65bed-126">Hizmet topolojisinin adı.</span><span class="sxs-lookup"><span data-stu-id="65bed-126">The name of the service topology.</span></span>

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

### <span data-ttu-id="65bed-127">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="65bed-127">-PassThru</span></span>
<span data-ttu-id="65bed-128">{{Dolgu geçiş açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="65bed-128">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="65bed-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65bed-129">-ResourceGroupName</span></span>
<span data-ttu-id="65bed-130">Kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="65bed-130">The resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65bed-131">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="65bed-131">-ResourceId</span></span>
<span data-ttu-id="65bed-132">Kaynak tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="65bed-132">The resource identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65bed-133">-Onay</span><span class="sxs-lookup"><span data-stu-id="65bed-133">-Confirm</span></span>
<span data-ttu-id="65bed-134">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="65bed-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="65bed-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="65bed-135">-WhatIf</span></span>
<span data-ttu-id="65bed-136">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="65bed-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="65bed-137">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="65bed-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="65bed-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65bed-138">CommonParameters</span></span>
<span data-ttu-id="65bed-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="65bed-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65bed-140">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="65bed-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65bed-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="65bed-141">INPUTS</span></span>

### <span data-ttu-id="65bed-142">System. String</span><span class="sxs-lookup"><span data-stu-id="65bed-142">System.String</span></span>

### <span data-ttu-id="65bed-143">Microsoft. Azure. Commands. DeploymentManager. modeller. PSServiceTopologyResource</span><span class="sxs-lookup"><span data-stu-id="65bed-143">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span></span>

## <span data-ttu-id="65bed-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="65bed-144">OUTPUTS</span></span>

### <span data-ttu-id="65bed-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="65bed-145">System.Boolean</span></span>

## <span data-ttu-id="65bed-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="65bed-146">NOTES</span></span>

## <span data-ttu-id="65bed-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="65bed-147">RELATED LINKS</span></span>
