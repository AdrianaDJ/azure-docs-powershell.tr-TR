---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/remove-azdeploymentmanagerservicetopology
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerServiceTopology.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerServiceTopology.md
ms.openlocfilehash: 7323883028d062cf11f4e1befe1ea42cb1f8bcb2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94108326"
---
# <span data-ttu-id="ed88c-101">Remove-AzDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="ed88c-101">Remove-AzDeploymentManagerServiceTopology</span></span>

## <span data-ttu-id="ed88c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ed88c-102">SYNOPSIS</span></span>
<span data-ttu-id="ed88c-103">Hizmet topolojisini siler.</span><span class="sxs-lookup"><span data-stu-id="ed88c-103">Deletes the service topology.</span></span> <span data-ttu-id="ed88c-104">Hizmet topolojisi altında oluşturulan hizmetlerin, hizmet topolojisini silmeden önce silinmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="ed88c-104">All services created under a service topology need to be deleted before deleting the service topology.</span></span>

## <span data-ttu-id="ed88c-105">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ed88c-105">SYNTAX</span></span>

### <span data-ttu-id="ed88c-106">Etkileşimli (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="ed88c-106">Interactive (Default)</span></span>
```
Remove-AzDeploymentManagerServiceTopology [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ed88c-107">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="ed88c-107">ResourceId</span></span>
```
Remove-AzDeploymentManagerServiceTopology [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ed88c-108">InputObject</span><span class="sxs-lookup"><span data-stu-id="ed88c-108">InputObject</span></span>
```
Remove-AzDeploymentManagerServiceTopology [-InputObject] <PSServiceTopologyResource> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ed88c-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="ed88c-109">DESCRIPTION</span></span>
<span data-ttu-id="ed88c-110">**Remove-AzDeploymentManagerServiceTopology** cmdlet 'i bir hizmet topolojisini siler.</span><span class="sxs-lookup"><span data-stu-id="ed88c-110">The **Remove-AzDeploymentManagerServiceTopology** cmdlet deletes a service topology.</span></span>

<span data-ttu-id="ed88c-111">Hizmet topolojisini adına ve kaynak grubu adına göre belirtin.</span><span class="sxs-lookup"><span data-stu-id="ed88c-111">Specify the service topology by its name and the resource group name.</span></span> <span data-ttu-id="ed88c-112">Alternatif olarak, ServiceTopology nesnesini veya RESOURCEID 'yi de sağlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ed88c-112">Alternately, you can provide the ServiceTopology object or the ResourceId.</span></span>

## <span data-ttu-id="ed88c-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ed88c-113">EXAMPLES</span></span>

### <span data-ttu-id="ed88c-114">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="ed88c-114">Example 1</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerServiceTopology -ResourceGroupName ContosoResourceGroup -Name ContosoServiceTopology
```

<span data-ttu-id="ed88c-115">Bu komut, ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="ed88c-115">This command deletes a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="ed88c-116">Örnek 2: kaynak tanımlayıcısını kullanarak hizmet topolojisini silme.</span><span class="sxs-lookup"><span data-stu-id="ed88c-116">Example 2: Delete a service topology using the resource identifier.</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerServiceTopology -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology"
```

<span data-ttu-id="ed88c-117">Bu komut, ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="ed88c-117">This command deletes a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="ed88c-118">Örnek 3: hizmet topolojisi nesnesini kullanarak hizmet topolojisini silme.</span><span class="sxs-lookup"><span data-stu-id="ed88c-118">Example 3: Delete a service topology using the service topology object.</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerService -InputObject $serviceTopologyObject
```

<span data-ttu-id="ed88c-119">Bu komut, adı ve ResourceGroup 'in sırasıyla $serviceTopologyObject Name ve ResourceGroupName özellikleriyle eşleşen bir hizmet topolojisini siler.</span><span class="sxs-lookup"><span data-stu-id="ed88c-119">This command deletes a service topology whose name and ResourceGroup match the Name and ResourceGroupName properties of the $serviceTopologyObject, respectively.</span></span>

## <span data-ttu-id="ed88c-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ed88c-120">PARAMETERS</span></span>

### <span data-ttu-id="ed88c-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed88c-121">-DefaultProfile</span></span>
<span data-ttu-id="ed88c-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ed88c-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ed88c-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ed88c-123">-InputObject</span></span>
<span data-ttu-id="ed88c-124">Kaldırılacak kaynak.</span><span class="sxs-lookup"><span data-stu-id="ed88c-124">The resource to be removed.</span></span>

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

### <span data-ttu-id="ed88c-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="ed88c-125">-Name</span></span>
<span data-ttu-id="ed88c-126">Hizmet topolojisinin adı.</span><span class="sxs-lookup"><span data-stu-id="ed88c-126">The name of the service topology.</span></span>

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

### <span data-ttu-id="ed88c-127">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="ed88c-127">-PassThru</span></span>
<span data-ttu-id="ed88c-128">{{Dolgu geçiş açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="ed88c-128">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="ed88c-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed88c-129">-ResourceGroupName</span></span>
<span data-ttu-id="ed88c-130">Kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="ed88c-130">The resource group.</span></span>

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

### <span data-ttu-id="ed88c-131">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="ed88c-131">-ResourceId</span></span>
<span data-ttu-id="ed88c-132">Kaynak tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="ed88c-132">The resource identifier.</span></span>

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

### <span data-ttu-id="ed88c-133">-Onay</span><span class="sxs-lookup"><span data-stu-id="ed88c-133">-Confirm</span></span>
<span data-ttu-id="ed88c-134">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ed88c-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ed88c-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ed88c-135">-WhatIf</span></span>
<span data-ttu-id="ed88c-136">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ed88c-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ed88c-137">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ed88c-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ed88c-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed88c-138">CommonParameters</span></span>
<span data-ttu-id="ed88c-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ed88c-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed88c-140">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="ed88c-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed88c-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ed88c-141">INPUTS</span></span>

### <span data-ttu-id="ed88c-142">System. String</span><span class="sxs-lookup"><span data-stu-id="ed88c-142">System.String</span></span>

### <span data-ttu-id="ed88c-143">Microsoft. Azure. Commands. DeploymentManager. modeller. PSServiceTopologyResource</span><span class="sxs-lookup"><span data-stu-id="ed88c-143">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span></span>

## <span data-ttu-id="ed88c-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ed88c-144">OUTPUTS</span></span>

### <span data-ttu-id="ed88c-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ed88c-145">System.Boolean</span></span>

## <span data-ttu-id="ed88c-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ed88c-146">NOTES</span></span>

## <span data-ttu-id="ed88c-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ed88c-147">RELATED LINKS</span></span>
