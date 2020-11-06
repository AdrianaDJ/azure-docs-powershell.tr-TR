---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/remove-azurermdeploymentmanagerservice
schema: 2.0.0
ms.openlocfilehash: 4b2cd4ef2dde674b10d51dc378578acbd13c4a7b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93571425"
---
# <span data-ttu-id="cb76a-101">Remove-AzureRmDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="cb76a-101">Remove-AzureRmDeploymentManagerService</span></span>

## <span data-ttu-id="cb76a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cb76a-102">SYNOPSIS</span></span>
<span data-ttu-id="cb76a-103">Hizmet topolojisinde bir hizmeti siler.</span><span class="sxs-lookup"><span data-stu-id="cb76a-103">Deletes a service in a service topology.</span></span>

## <span data-ttu-id="cb76a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="cb76a-104">SYNTAX</span></span>

### <span data-ttu-id="cb76a-105">Etkileşimli (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="cb76a-105">Interactive (Default)</span></span>
```
Remove-AzureRmDeploymentManagerService [-ResourceGroupName] <String> [-ServiceTopologyName] <String>
 [-Name] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cb76a-106">ByServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="cb76a-106">ByServiceTopologyObject</span></span>
```
Remove-AzureRmDeploymentManagerService [-Name] <String> [-ServiceTopology] <PSServiceTopologyResource> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb76a-107">Byservicetopologyresourceıd</span><span class="sxs-lookup"><span data-stu-id="cb76a-107">ByServiceTopologyResourceId</span></span>
```
Remove-AzureRmDeploymentManagerService [-Name] <String> [-ServiceTopologyResourceId] <String> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb76a-108">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="cb76a-108">ResourceId</span></span>
```
Remove-AzureRmDeploymentManagerService [-ResourceId] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb76a-109">InputObject</span><span class="sxs-lookup"><span data-stu-id="cb76a-109">InputObject</span></span>
```
Remove-AzureRmDeploymentManagerService [-Service] <PSServiceResource> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cb76a-110">Tanım</span><span class="sxs-lookup"><span data-stu-id="cb76a-110">DESCRIPTION</span></span>
<span data-ttu-id="cb76a-111">**Remove-AzureRmDeploymentManagerService** cmdlet 'i hizmet topolojisi altında bir hizmeti siler.</span><span class="sxs-lookup"><span data-stu-id="cb76a-111">The **Remove-AzureRmDeploymentManagerService** cmdlet deletes a service under a service topology.</span></span>
<span data-ttu-id="cb76a-112">Hizmeti adına, hizmet topolojisine ve kaynak grubu adına göre belirtin.</span><span class="sxs-lookup"><span data-stu-id="cb76a-112">Specify the service by its name, service topology it is in and the resource group name.</span></span> <span data-ttu-id="cb76a-113">Alternatif olarak, servis nesnesini veya RESOURCEID 'yi de sağlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="cb76a-113">Alternately, you can provide the Service object or the ResourceId.</span></span>

## <span data-ttu-id="cb76a-114">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="cb76a-114">EXAMPLES</span></span>

### <span data-ttu-id="cb76a-115">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="cb76a-115">Example 1</span></span>
```powershell
PS C:\> Remove-AzureRmDeploymentManagerService -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology -Name ContosoService1
```

<span data-ttu-id="cb76a-116">Bu komut, ContosoService1 adlı bir hizmeti, ContosoResourceGroup 'ta ContosoServiceTopology adındaki bir hizmet topolojisinde siler.</span><span class="sxs-lookup"><span data-stu-id="cb76a-116">This command deletes a service named ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="cb76a-117">Örnek 2: kaynak tanımlayıcısını kullanarak hizmeti silme.</span><span class="sxs-lookup"><span data-stu-id="cb76a-117">Example 2: Delete a service using the resource identifier.</span></span>
```powershell
PS C:\> Remove-AzureRmDeploymentManagerService -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology/services/ContosoService1"
```

<span data-ttu-id="cb76a-118">Bu komut, ContosoService1 adlı bir hizmeti, ContosoResourceGroup 'ta ContosoServiceTopology adındaki bir hizmet topolojisinde siler.</span><span class="sxs-lookup"><span data-stu-id="cb76a-118">This command deletes a service named ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="cb76a-119">Örnek 3: hizmet nesnesini kullanarak hizmet silme.</span><span class="sxs-lookup"><span data-stu-id="cb76a-119">Example 3: Delete a service using the service object.</span></span>
```powershell
PS C:\> Remove-AzureRmDeploymentManagerService -Service $serviceObject
```

<span data-ttu-id="cb76a-120">Bu komut, adı, hizmet topolojisi adı ve ResourceGroup, sırasıyla $serviceObject adı, ServiceTopologyName ve ResourceGroupName özellikleriyle eşleşen bir hizmeti siler.</span><span class="sxs-lookup"><span data-stu-id="cb76a-120">This command deletes a service whose name, service topology name and ResourceGroup match the Name, ServiceTopologyName and ResourceGroupName properties of the $serviceObject, respectively.</span></span>

## <span data-ttu-id="cb76a-121">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="cb76a-121">PARAMETERS</span></span>

### <span data-ttu-id="cb76a-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb76a-122">-DefaultProfile</span></span>
<span data-ttu-id="cb76a-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="cb76a-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cb76a-124">-Force</span><span class="sxs-lookup"><span data-stu-id="cb76a-124">-Force</span></span>
<span data-ttu-id="cb76a-125">Onay sorma.</span><span class="sxs-lookup"><span data-stu-id="cb76a-125">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="cb76a-126">-Ad</span><span class="sxs-lookup"><span data-stu-id="cb76a-126">-Name</span></span>
<span data-ttu-id="cb76a-127">Hizmetin adı.</span><span class="sxs-lookup"><span data-stu-id="cb76a-127">The name of the service.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive, ByServiceTopologyObject, ByServiceTopologyResourceId
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb76a-128">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="cb76a-128">-PassThru</span></span>
<span data-ttu-id="cb76a-129">{{Dolgu geçiş açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="cb76a-129">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="cb76a-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb76a-130">-ResourceGroupName</span></span>
<span data-ttu-id="cb76a-131">Kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="cb76a-131">The resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb76a-132">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="cb76a-132">-ResourceId</span></span>
<span data-ttu-id="cb76a-133">Kaynak tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="cb76a-133">The resource identifier.</span></span>

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

### <span data-ttu-id="cb76a-134">-Hizmet</span><span class="sxs-lookup"><span data-stu-id="cb76a-134">-Service</span></span>
<span data-ttu-id="cb76a-135">Kaldırılacak kaynak.</span><span class="sxs-lookup"><span data-stu-id="cb76a-135">The resource to be removed.</span></span>

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

### <span data-ttu-id="cb76a-136">-ServiceTopology</span><span class="sxs-lookup"><span data-stu-id="cb76a-136">-ServiceTopology</span></span>
<span data-ttu-id="cb76a-137">Hizmetin oluşturulması gereken hizmet topolojisi nesnesi.</span><span class="sxs-lookup"><span data-stu-id="cb76a-137">The service topology object in which the service should be created.</span></span>

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

### <span data-ttu-id="cb76a-138">-ServiceTopologyName</span><span class="sxs-lookup"><span data-stu-id="cb76a-138">-ServiceTopologyName</span></span>
<span data-ttu-id="cb76a-139">Hizmetin ait olduğu hizmet topolojisinin adı.</span><span class="sxs-lookup"><span data-stu-id="cb76a-139">The name of the service topology the service belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb76a-140">-Servicetopologyresourceıd</span><span class="sxs-lookup"><span data-stu-id="cb76a-140">-ServiceTopologyResourceId</span></span>
<span data-ttu-id="cb76a-141">Hizmetin oluşturulması gereken hizmet topolojisi kaynak tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="cb76a-141">The service topology resource identifier in which the service should be created.</span></span>

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

### <span data-ttu-id="cb76a-142">-Onay</span><span class="sxs-lookup"><span data-stu-id="cb76a-142">-Confirm</span></span>
<span data-ttu-id="cb76a-143">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="cb76a-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cb76a-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cb76a-144">-WhatIf</span></span>
<span data-ttu-id="cb76a-145">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="cb76a-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cb76a-146">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="cb76a-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cb76a-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb76a-147">CommonParameters</span></span>
<span data-ttu-id="cb76a-148">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="cb76a-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb76a-149">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cb76a-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb76a-150">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="cb76a-150">INPUTS</span></span>

### <span data-ttu-id="cb76a-151">Microsoft. Azure. Commands. DeploymentManager. modeller. PSServiceResource</span><span class="sxs-lookup"><span data-stu-id="cb76a-151">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span></span>

## <span data-ttu-id="cb76a-152">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="cb76a-152">OUTPUTS</span></span>

### <span data-ttu-id="cb76a-153">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="cb76a-153">System.Boolean</span></span>

## <span data-ttu-id="cb76a-154">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="cb76a-154">NOTES</span></span>

## <span data-ttu-id="cb76a-155">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="cb76a-155">RELATED LINKS</span></span>

[<span data-ttu-id="cb76a-156">Yeni-AzureRmDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="cb76a-156">New-AzureRmDeploymentManagerService</span></span>](./New-AzureRmDeploymentManagerService.md)

[<span data-ttu-id="cb76a-157">Get-AzureRmDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="cb76a-157">Get-AzureRmDeploymentManagerService</span></span>](./Get-AzureRmDeploymentManagerService.md)

[<span data-ttu-id="cb76a-158">Set-AzureRmDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="cb76a-158">Set-AzureRmDeploymentManagerService</span></span>](./Set-AzureRmDeploymentManagerService.md)