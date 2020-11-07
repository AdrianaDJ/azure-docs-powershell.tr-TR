---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/remove-azdeploymentmanagerservicetopology
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerServiceTopology.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerServiceTopology.md
ms.openlocfilehash: 695a10eb71cc2c4bd1a6bc7eef6cba265d524fe6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93752123"
---
# <span data-ttu-id="435f9-101">Remove-AzDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="435f9-101">Remove-AzDeploymentManagerServiceTopology</span></span>

## <span data-ttu-id="435f9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="435f9-102">SYNOPSIS</span></span>
<span data-ttu-id="435f9-103">Hizmet topolojisini siler.</span><span class="sxs-lookup"><span data-stu-id="435f9-103">Deletes the service topology.</span></span> <span data-ttu-id="435f9-104">Hizmet topolojisi altında oluşturulan hizmetlerin, hizmet topolojisini silmeden önce silinmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="435f9-104">All services created under a service topology need to be deleted before deleting the service topology.</span></span>

## <span data-ttu-id="435f9-105">INDEKI</span><span class="sxs-lookup"><span data-stu-id="435f9-105">SYNTAX</span></span>

### <span data-ttu-id="435f9-106">Etkileşimli (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="435f9-106">Interactive (Default)</span></span>
```
Remove-AzDeploymentManagerServiceTopology [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="435f9-107">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="435f9-107">ResourceId</span></span>
```
Remove-AzDeploymentManagerServiceTopology [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="435f9-108">InputObject</span><span class="sxs-lookup"><span data-stu-id="435f9-108">InputObject</span></span>
```
Remove-AzDeploymentManagerServiceTopology [-InputObject] <PSServiceTopologyResource> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="435f9-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="435f9-109">DESCRIPTION</span></span>
<span data-ttu-id="435f9-110">**Remove-AzDeploymentManagerServiceTopology** cmdlet 'i bir hizmet topolojisini siler.</span><span class="sxs-lookup"><span data-stu-id="435f9-110">The **Remove-AzDeploymentManagerServiceTopology** cmdlet deletes a service topology.</span></span>

<span data-ttu-id="435f9-111">Hizmet topolojisini adına ve kaynak grubu adına göre belirtin.</span><span class="sxs-lookup"><span data-stu-id="435f9-111">Specify the service topology by its name and the resource group name.</span></span> <span data-ttu-id="435f9-112">Alternatif olarak, ServiceTopology nesnesini veya RESOURCEID 'yi de sağlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="435f9-112">Alternately, you can provide the ServiceTopology object or the ResourceId.</span></span>

## <span data-ttu-id="435f9-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="435f9-113">EXAMPLES</span></span>

### <span data-ttu-id="435f9-114">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="435f9-114">Example 1</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerServiceTopology -ResourceGroupName ContosoResourceGroup -Name ContosoServiceTopology
```

<span data-ttu-id="435f9-115">Bu komut, ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="435f9-115">This command deletes a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="435f9-116">Örnek 2: kaynak tanımlayıcısını kullanarak hizmet topolojisini silme.</span><span class="sxs-lookup"><span data-stu-id="435f9-116">Example 2: Delete a service topology using the resource identifier.</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerServiceTopology -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology"
```

<span data-ttu-id="435f9-117">Bu komut, ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="435f9-117">This command deletes a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="435f9-118">Örnek 3: hizmet topolojisi nesnesini kullanarak hizmet topolojisini silme.</span><span class="sxs-lookup"><span data-stu-id="435f9-118">Example 3: Delete a service topology using the service topology object.</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerService -InputObject $serviceTopologyObject
```

<span data-ttu-id="435f9-119">Bu komut, adı ve ResourceGroup 'in sırasıyla $serviceTopologyObject Name ve ResourceGroupName özellikleriyle eşleşen bir hizmet topolojisini siler.</span><span class="sxs-lookup"><span data-stu-id="435f9-119">This command deletes a service topology whose name and ResourceGroup match the Name and ResourceGroupName properties of the $serviceTopologyObject, respectively.</span></span>

## <span data-ttu-id="435f9-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="435f9-120">PARAMETERS</span></span>

### <span data-ttu-id="435f9-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="435f9-121">-DefaultProfile</span></span>
<span data-ttu-id="435f9-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="435f9-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="435f9-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="435f9-123">-InputObject</span></span>
<span data-ttu-id="435f9-124">Kaldırılacak kaynak.</span><span class="sxs-lookup"><span data-stu-id="435f9-124">The resource to be removed.</span></span>

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

### <span data-ttu-id="435f9-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="435f9-125">-Name</span></span>
<span data-ttu-id="435f9-126">Hizmet topolojisinin adı.</span><span class="sxs-lookup"><span data-stu-id="435f9-126">The name of the service topology.</span></span>

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

### <span data-ttu-id="435f9-127">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="435f9-127">-PassThru</span></span>
<span data-ttu-id="435f9-128">{{Dolgu geçiş açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="435f9-128">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="435f9-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="435f9-129">-ResourceGroupName</span></span>
<span data-ttu-id="435f9-130">Kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="435f9-130">The resource group.</span></span>

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

### <span data-ttu-id="435f9-131">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="435f9-131">-ResourceId</span></span>
<span data-ttu-id="435f9-132">Kaynak tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="435f9-132">The resource identifier.</span></span>

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

### <span data-ttu-id="435f9-133">-Onay</span><span class="sxs-lookup"><span data-stu-id="435f9-133">-Confirm</span></span>
<span data-ttu-id="435f9-134">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="435f9-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="435f9-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="435f9-135">-WhatIf</span></span>
<span data-ttu-id="435f9-136">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="435f9-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="435f9-137">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="435f9-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="435f9-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="435f9-138">CommonParameters</span></span>
<span data-ttu-id="435f9-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="435f9-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="435f9-140">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="435f9-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="435f9-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="435f9-141">INPUTS</span></span>

### <span data-ttu-id="435f9-142">System. String</span><span class="sxs-lookup"><span data-stu-id="435f9-142">System.String</span></span>

### <span data-ttu-id="435f9-143">Microsoft. Azure. Commands. DeploymentManager. modeller. PSServiceTopologyResource</span><span class="sxs-lookup"><span data-stu-id="435f9-143">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span></span>

## <span data-ttu-id="435f9-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="435f9-144">OUTPUTS</span></span>

### <span data-ttu-id="435f9-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="435f9-145">System.Boolean</span></span>

## <span data-ttu-id="435f9-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="435f9-146">NOTES</span></span>

## <span data-ttu-id="435f9-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="435f9-147">RELATED LINKS</span></span>
