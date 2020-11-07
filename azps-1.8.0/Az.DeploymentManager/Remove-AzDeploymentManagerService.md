---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/remove-azdeploymentmanagerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerService.md
ms.openlocfilehash: ee0f1f855f4f24e3672606bfedc000452ce6040d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93760986"
---
# <span data-ttu-id="e8f03-101">Remove-AzDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="e8f03-101">Remove-AzDeploymentManagerService</span></span>

## <span data-ttu-id="e8f03-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e8f03-102">SYNOPSIS</span></span>
<span data-ttu-id="e8f03-103">Hizmeti siler...</span><span class="sxs-lookup"><span data-stu-id="e8f03-103">Deletes the service..</span></span> <span data-ttu-id="e8f03-104">Hizmet altında oluşturulan tüm hizmet birimlerinin, hizmet silinmeden önce silinmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="e8f03-104">All service units created under a service need to be deleted before deleting the service.</span></span>

## <span data-ttu-id="e8f03-105">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e8f03-105">SYNTAX</span></span>

### <span data-ttu-id="e8f03-106">Etkileşimli (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="e8f03-106">Interactive (Default)</span></span>
```
Remove-AzDeploymentManagerService [-ResourceGroupName] <String> [-ServiceTopologyName] <String>
 [-Name] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e8f03-107">ByServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="e8f03-107">ByServiceTopologyObject</span></span>
```
Remove-AzDeploymentManagerService [-Name] <String> [-ServiceTopologyObject] <PSServiceTopologyResource>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e8f03-108">Byservicetopologyresourceıd</span><span class="sxs-lookup"><span data-stu-id="e8f03-108">ByServiceTopologyResourceId</span></span>
```
Remove-AzDeploymentManagerService [-Name] <String> [-ServiceTopologyResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e8f03-109">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="e8f03-109">ResourceId</span></span>
```
Remove-AzDeploymentManagerService [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e8f03-110">InputObject</span><span class="sxs-lookup"><span data-stu-id="e8f03-110">InputObject</span></span>
```
Remove-AzDeploymentManagerService [-InputObject] <PSServiceResource> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e8f03-111">Tanım</span><span class="sxs-lookup"><span data-stu-id="e8f03-111">DESCRIPTION</span></span>
<span data-ttu-id="e8f03-112">**Remove-AzDeploymentManagerService** cmdlet 'i hizmet topolojisi altında bir hizmeti siler.</span><span class="sxs-lookup"><span data-stu-id="e8f03-112">The **Remove-AzDeploymentManagerService** cmdlet deletes a service under a service topology.</span></span>
<span data-ttu-id="e8f03-113">Hizmeti adına, hizmet topolojisine ve kaynak grubu adına göre belirtin.</span><span class="sxs-lookup"><span data-stu-id="e8f03-113">Specify the service by its name, service topology it is in and the resource group name.</span></span> <span data-ttu-id="e8f03-114">Alternatif olarak, servis nesnesini veya RESOURCEID 'yi de sağlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e8f03-114">Alternately, you can provide the Service object or the ResourceId.</span></span>

## <span data-ttu-id="e8f03-115">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e8f03-115">EXAMPLES</span></span>

### <span data-ttu-id="e8f03-116">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="e8f03-116">Example 1</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerService -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology -Name ContosoService1
```

<span data-ttu-id="e8f03-117">Bu komut, ContosoService1 adlı bir hizmeti, ContosoResourceGroup 'ta ContosoServiceTopology adındaki bir hizmet topolojisinde siler.</span><span class="sxs-lookup"><span data-stu-id="e8f03-117">This command deletes a service named ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="e8f03-118">Örnek 2: kaynak tanımlayıcısını kullanarak hizmeti silme.</span><span class="sxs-lookup"><span data-stu-id="e8f03-118">Example 2: Delete a service using the resource identifier.</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerService -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology/services/ContosoService1"
```

<span data-ttu-id="e8f03-119">Bu komut, ContosoService1 adlı bir hizmeti, ContosoResourceGroup 'ta ContosoServiceTopology adındaki bir hizmet topolojisinde siler.</span><span class="sxs-lookup"><span data-stu-id="e8f03-119">This command deletes a service named ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="e8f03-120">Örnek 3: hizmet nesnesini kullanarak hizmet silme.</span><span class="sxs-lookup"><span data-stu-id="e8f03-120">Example 3: Delete a service using the service object.</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerService -InputObject $serviceObject
```

<span data-ttu-id="e8f03-121">Bu komut, adı, hizmet topolojisi adı ve ResourceGroup, sırasıyla $serviceObject adı, ServiceTopologyName ve ResourceGroupName özellikleriyle eşleşen bir hizmeti siler.</span><span class="sxs-lookup"><span data-stu-id="e8f03-121">This command deletes a service whose name, service topology name and ResourceGroup match the Name, ServiceTopologyName and ResourceGroupName properties of the $serviceObject, respectively.</span></span>

## <span data-ttu-id="e8f03-122">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e8f03-122">PARAMETERS</span></span>

### <span data-ttu-id="e8f03-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8f03-123">-DefaultProfile</span></span>
<span data-ttu-id="e8f03-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e8f03-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e8f03-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e8f03-125">-InputObject</span></span>
<span data-ttu-id="e8f03-126">Hizmet nesnesi.</span><span class="sxs-lookup"><span data-stu-id="e8f03-126">Service object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e8f03-127">-Ad</span><span class="sxs-lookup"><span data-stu-id="e8f03-127">-Name</span></span>
<span data-ttu-id="e8f03-128">Hizmetin adı.</span><span class="sxs-lookup"><span data-stu-id="e8f03-128">The name of the service.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive, ByServiceTopologyObject, ByServiceTopologyResourceId
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8f03-129">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="e8f03-129">-PassThru</span></span>
<span data-ttu-id="e8f03-130">{{Dolgu geçiş açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="e8f03-130">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="e8f03-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8f03-131">-ResourceGroupName</span></span>
<span data-ttu-id="e8f03-132">Kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="e8f03-132">The resource group.</span></span>

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

### <span data-ttu-id="e8f03-133">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="e8f03-133">-ResourceId</span></span>
<span data-ttu-id="e8f03-134">Kaynak tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="e8f03-134">The resource identifier.</span></span>

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

### <span data-ttu-id="e8f03-135">-ServiceTopologyName</span><span class="sxs-lookup"><span data-stu-id="e8f03-135">-ServiceTopologyName</span></span>
<span data-ttu-id="e8f03-136">Hizmet topolojisinin adı.</span><span class="sxs-lookup"><span data-stu-id="e8f03-136">The name of the service topology.</span></span>

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

### <span data-ttu-id="e8f03-137">-ServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="e8f03-137">-ServiceTopologyObject</span></span>
<span data-ttu-id="e8f03-138">Hizmetin oluşturulması gereken hizmet topolojisi nesnesi.</span><span class="sxs-lookup"><span data-stu-id="e8f03-138">The service topology object in which the service should be created.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource
Parameter Sets: ByServiceTopologyObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8f03-139">-Servicetopologyresourceıd</span><span class="sxs-lookup"><span data-stu-id="e8f03-139">-ServiceTopologyResourceId</span></span>
<span data-ttu-id="e8f03-140">Hizmetin oluşturulması gereken hizmet topolojisi kaynak tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="e8f03-140">The service topology resource identifier in which the service should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: ByServiceTopologyResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8f03-141">-Onay</span><span class="sxs-lookup"><span data-stu-id="e8f03-141">-Confirm</span></span>
<span data-ttu-id="e8f03-142">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e8f03-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e8f03-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e8f03-143">-WhatIf</span></span>
<span data-ttu-id="e8f03-144">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e8f03-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e8f03-145">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e8f03-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e8f03-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8f03-146">CommonParameters</span></span>
<span data-ttu-id="e8f03-147">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e8f03-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8f03-148">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e8f03-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8f03-149">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e8f03-149">INPUTS</span></span>

### <span data-ttu-id="e8f03-150">System. String</span><span class="sxs-lookup"><span data-stu-id="e8f03-150">System.String</span></span>

### <span data-ttu-id="e8f03-151">Microsoft. Azure. Commands. DeploymentManager. modeller. PSServiceResource</span><span class="sxs-lookup"><span data-stu-id="e8f03-151">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span></span>

## <span data-ttu-id="e8f03-152">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e8f03-152">OUTPUTS</span></span>

### <span data-ttu-id="e8f03-153">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e8f03-153">System.Boolean</span></span>

## <span data-ttu-id="e8f03-154">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e8f03-154">NOTES</span></span>

## <span data-ttu-id="e8f03-155">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e8f03-155">RELATED LINKS</span></span>
