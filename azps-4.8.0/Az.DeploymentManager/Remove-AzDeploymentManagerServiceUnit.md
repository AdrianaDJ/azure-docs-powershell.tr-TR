---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/remove-azdeploymentmanagerserviceunit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerServiceUnit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerServiceUnit.md
ms.openlocfilehash: d4248a13282824c60e698b2257b3e38a78ce3a6f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94107794"
---
# <span data-ttu-id="34403-101">Remove-AzDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="34403-101">Remove-AzDeploymentManagerServiceUnit</span></span>

## <span data-ttu-id="34403-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="34403-102">SYNOPSIS</span></span>
<span data-ttu-id="34403-103">Hizmet birimini siler.</span><span class="sxs-lookup"><span data-stu-id="34403-103">Deletes the service unit.</span></span>

## <span data-ttu-id="34403-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="34403-104">SYNTAX</span></span>

### <span data-ttu-id="34403-105">Etkileşimli (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="34403-105">Interactive (Default)</span></span>
```
Remove-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceTopologyName] <String>
 [-ServiceName] <String> [-Name] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="34403-106">ByTopologyObjectAndServiceName</span><span class="sxs-lookup"><span data-stu-id="34403-106">ByTopologyObjectAndServiceName</span></span>
```
Remove-AzDeploymentManagerServiceUnit [-ServiceName] <String> [-Name] <String>
 [-ServiceTopologyObject] <PSServiceTopologyResource> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="34403-107">ByTopologyResourceAndServiceName</span><span class="sxs-lookup"><span data-stu-id="34403-107">ByTopologyResourceAndServiceName</span></span>
```
Remove-AzDeploymentManagerServiceUnit [-ServiceName] <String> [-Name] <String>
 [-ServiceTopologyResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="34403-108">ByServiceObject</span><span class="sxs-lookup"><span data-stu-id="34403-108">ByServiceObject</span></span>
```
Remove-AzDeploymentManagerServiceUnit [-Name] <String> [-ServiceObject] <PSServiceResource> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="34403-109">ByServiceResourceId</span><span class="sxs-lookup"><span data-stu-id="34403-109">ByServiceResourceId</span></span>
```
Remove-AzDeploymentManagerServiceUnit [-Name] <String> [-ServiceResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="34403-110">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="34403-110">ResourceId</span></span>
```
Remove-AzDeploymentManagerServiceUnit [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="34403-111">InputObject</span><span class="sxs-lookup"><span data-stu-id="34403-111">InputObject</span></span>
```
Remove-AzDeploymentManagerServiceUnit [-InputObject] <PSServiceUnitResource> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="34403-112">Tanım</span><span class="sxs-lookup"><span data-stu-id="34403-112">DESCRIPTION</span></span>
<span data-ttu-id="34403-113">**Remove-AzDeploymentManagerServiceUnit** cmdlet 'i, bir hizmette hizmet birimini siler.</span><span class="sxs-lookup"><span data-stu-id="34403-113">The **Remove-AzDeploymentManagerServiceUnit** cmdlet deletes a service unit in a service.</span></span>

<span data-ttu-id="34403-114">Hizmet birimini adına, tanımladığı hizmete, hizmet topolojisi adına ve kaynak grubu adına göre belirtin.</span><span class="sxs-lookup"><span data-stu-id="34403-114">Specify the service unit by its name, the service under which it was defined, the service topology name and the resource group name.</span></span> <span data-ttu-id="34403-115">Alternatif olarak, ServiceUnit nesnesini veya RESOURCEID 'yi de sağlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="34403-115">Alternately, you can provide the ServiceUnit object or the ResourceId.</span></span>

## <span data-ttu-id="34403-116">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="34403-116">EXAMPLES</span></span>

### <span data-ttu-id="34403-117">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="34403-117">Example 1</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerServiceUnit -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology -ServiceName ContosoService1  -Name ContosoService1Storage
```

<span data-ttu-id="34403-118">Bu komut, ContosoService1Storage adlı bir hizmet biriminin altında, ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="34403-118">This command deletes a service unit named ContosoService1Storage under a service ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="34403-119">Örnek 2: kaynak tanımlayıcısını kullanarak hizmet birimini silme.</span><span class="sxs-lookup"><span data-stu-id="34403-119">Example 2: Delete a service unit using the resource identifier.</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerServiceUnit -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology/services/ContosoService1/serviceUnits/ContosoService1Storage"
```

<span data-ttu-id="34403-120">Bu komut, ContosoService1Storage adlı bir hizmet biriminin altında, ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="34403-120">This command gets a service unit named ContosoService1Storage under a service ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="34403-121">Örnek 3: hizmet birimi nesnesini kullanarak hizmet birimini silme.</span><span class="sxs-lookup"><span data-stu-id="34403-121">Example 3: Delete a service unit using the service unit object.</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerServiceUnit -InputObject $serviceUnitObject
```

<span data-ttu-id="34403-122">Bu komut adı, hizmet adı, hizmet topolojisi adı ve ResourceGroup, sırasıyla adı, HizmetAdı, ServiceTopologyName ve ResourceGroupName $serviceUnitObject özellikleriyle eşleşen bir hizmet birimini siler.</span><span class="sxs-lookup"><span data-stu-id="34403-122">This command deletes a service unit whose name, service name, service topology name and ResourceGroup match the Name, ServiceName, ServiceTopologyName and ResourceGroupName properties of the $serviceUnitObject, respectively.</span></span>

## <span data-ttu-id="34403-123">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="34403-123">PARAMETERS</span></span>

### <span data-ttu-id="34403-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34403-124">-DefaultProfile</span></span>
<span data-ttu-id="34403-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="34403-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="34403-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="34403-126">-InputObject</span></span>
<span data-ttu-id="34403-127">Hizmet birimi kaynak nesnesi.</span><span class="sxs-lookup"><span data-stu-id="34403-127">Service unit resource object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="34403-128">-Ad</span><span class="sxs-lookup"><span data-stu-id="34403-128">-Name</span></span>
<span data-ttu-id="34403-129">Hizmet biriminin adı.</span><span class="sxs-lookup"><span data-stu-id="34403-129">The name of the service unit.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive, ByTopologyObjectAndServiceName, ByTopologyResourceAndServiceName, ByServiceObject, ByServiceResourceId
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34403-130">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="34403-130">-PassThru</span></span>
<span data-ttu-id="34403-131">{{Dolgu geçiş açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="34403-131">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="34403-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34403-132">-ResourceGroupName</span></span>
<span data-ttu-id="34403-133">Kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="34403-133">The resource group.</span></span>

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

### <span data-ttu-id="34403-134">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="34403-134">-ResourceId</span></span>
<span data-ttu-id="34403-135">Kaynak tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="34403-135">The resource identifier.</span></span>

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

### <span data-ttu-id="34403-136">-HizmetAdı</span><span class="sxs-lookup"><span data-stu-id="34403-136">-ServiceName</span></span>
<span data-ttu-id="34403-137">Hizmet biriminin parçası olduğu hizmetin adı.</span><span class="sxs-lookup"><span data-stu-id="34403-137">The name of the service the service unit is part of.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive, ByTopologyObjectAndServiceName, ByTopologyResourceAndServiceName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34403-138">-ServiceObject</span><span class="sxs-lookup"><span data-stu-id="34403-138">-ServiceObject</span></span>
<span data-ttu-id="34403-139">Hizmet biriminin oluşturulması gereken servis nesnesi.</span><span class="sxs-lookup"><span data-stu-id="34403-139">The service object in which the service unit should be created.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource
Parameter Sets: ByServiceObject
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34403-140">-ServiceResourceId</span><span class="sxs-lookup"><span data-stu-id="34403-140">-ServiceResourceId</span></span>
<span data-ttu-id="34403-141">Hizmet biriminin oluşturulması gereken hizmet kaynak tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="34403-141">The service resource identifier in which the service unit should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: ByServiceResourceId
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34403-142">-ServiceTopologyName</span><span class="sxs-lookup"><span data-stu-id="34403-142">-ServiceTopologyName</span></span>
<span data-ttu-id="34403-143">Hizmet biriminin parçası olan hizmet topolojisinin adı.</span><span class="sxs-lookup"><span data-stu-id="34403-143">The name of the service topology the service unit is part of.</span></span>

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

### <span data-ttu-id="34403-144">-ServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="34403-144">-ServiceTopologyObject</span></span>
<span data-ttu-id="34403-145">Hizmet biriminin oluşturulması gereken hizmet topolojisi nesnesi.</span><span class="sxs-lookup"><span data-stu-id="34403-145">The service topology object in which the service unit should be created.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource
Parameter Sets: ByTopologyObjectAndServiceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34403-146">-Servicetopologyresourceıd</span><span class="sxs-lookup"><span data-stu-id="34403-146">-ServiceTopologyResourceId</span></span>
<span data-ttu-id="34403-147">Hizmet biriminin oluşturulması gereken hizmet topolojisi kaynak tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="34403-147">The service topology resource identifier in which the service unit should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTopologyResourceAndServiceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34403-148">-Onay</span><span class="sxs-lookup"><span data-stu-id="34403-148">-Confirm</span></span>
<span data-ttu-id="34403-149">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="34403-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="34403-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="34403-150">-WhatIf</span></span>
<span data-ttu-id="34403-151">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="34403-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="34403-152">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="34403-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="34403-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34403-153">CommonParameters</span></span>
<span data-ttu-id="34403-154">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="34403-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34403-155">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="34403-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34403-156">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="34403-156">INPUTS</span></span>

### <span data-ttu-id="34403-157">System. String</span><span class="sxs-lookup"><span data-stu-id="34403-157">System.String</span></span>

### <span data-ttu-id="34403-158">Microsoft. Azure. Commands. DeploymentManager. modeller. PSServiceUnitResource</span><span class="sxs-lookup"><span data-stu-id="34403-158">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span></span>

## <span data-ttu-id="34403-159">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="34403-159">OUTPUTS</span></span>

### <span data-ttu-id="34403-160">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="34403-160">System.Boolean</span></span>

## <span data-ttu-id="34403-161">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="34403-161">NOTES</span></span>

## <span data-ttu-id="34403-162">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="34403-162">RELATED LINKS</span></span>
