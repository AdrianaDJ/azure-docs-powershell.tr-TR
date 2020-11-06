---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/remove-azurermdeploymentmanagerserviceunit
schema: 2.0.0
ms.openlocfilehash: 993b250b0c49efc448c0198c4e9a3aea29f77714
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93572202"
---
# <span data-ttu-id="791e3-101">Remove-AzureRmDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="791e3-101">Remove-AzureRmDeploymentManagerServiceUnit</span></span>

## <span data-ttu-id="791e3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="791e3-102">SYNOPSIS</span></span>
<span data-ttu-id="791e3-103">Hizmet topolojisinde hizmetin hizmet birimini siler.</span><span class="sxs-lookup"><span data-stu-id="791e3-103">Deletes the service unit of a service in a service topology.</span></span>

## <span data-ttu-id="791e3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="791e3-104">SYNTAX</span></span>

### <span data-ttu-id="791e3-105">Etkileşimli (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="791e3-105">Interactive (Default)</span></span>
```
Remove-AzureRmDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceTopologyName] <String>
 [-ServiceName] <String> [-Name] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="791e3-106">ByTopologyObjectAndServiceName</span><span class="sxs-lookup"><span data-stu-id="791e3-106">ByTopologyObjectAndServiceName</span></span>
```
Remove-AzureRmDeploymentManagerServiceUnit [-ServiceName] <String> [-Name] <String>
 [-ServiceTopology] <PSServiceTopologyResource> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="791e3-107">ByTopologyResourceAndServiceName</span><span class="sxs-lookup"><span data-stu-id="791e3-107">ByTopologyResourceAndServiceName</span></span>
```
Remove-AzureRmDeploymentManagerServiceUnit [-ServiceName] <String> [-Name] <String>
 [-ServiceTopologyResourceId] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="791e3-108">ByServiceObject</span><span class="sxs-lookup"><span data-stu-id="791e3-108">ByServiceObject</span></span>
```
Remove-AzureRmDeploymentManagerServiceUnit [-Name] <String> [-Service] <PSServiceResource> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="791e3-109">ByServiceResourceId</span><span class="sxs-lookup"><span data-stu-id="791e3-109">ByServiceResourceId</span></span>
```
Remove-AzureRmDeploymentManagerServiceUnit [-Name] <String> [-ServiceResourceId] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="791e3-110">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="791e3-110">ResourceId</span></span>
```
Remove-AzureRmDeploymentManagerServiceUnit [-ResourceId] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="791e3-111">InputObject</span><span class="sxs-lookup"><span data-stu-id="791e3-111">InputObject</span></span>
```
Remove-AzureRmDeploymentManagerServiceUnit [-ServiceUnit] <PSServiceUnitResource> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="791e3-112">Tanım</span><span class="sxs-lookup"><span data-stu-id="791e3-112">DESCRIPTION</span></span>
<span data-ttu-id="791e3-113">**Remove-AzureRmDeploymentManagerServiceUnit** cmdlet 'i, bir hizmette hizmet birimini siler.</span><span class="sxs-lookup"><span data-stu-id="791e3-113">The **Remove-AzureRmDeploymentManagerServiceUnit** cmdlet deletes a service unit in a service.</span></span>

<span data-ttu-id="791e3-114">Hizmet birimini adına, tanımladığı hizmete, hizmet topolojisi adına ve kaynak grubu adına göre belirtin.</span><span class="sxs-lookup"><span data-stu-id="791e3-114">Specify the service unit by its name, the service under which it was defined, the service topology name and the resource group name.</span></span> <span data-ttu-id="791e3-115">Alternatif olarak, ServiceUnit nesnesini veya RESOURCEID 'yi de sağlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="791e3-115">Alternately, you can provide the ServiceUnit object or the ResourceId.</span></span>

## <span data-ttu-id="791e3-116">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="791e3-116">EXAMPLES</span></span>

### <span data-ttu-id="791e3-117">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="791e3-117">Example 1</span></span>
```powershell
PS C:\> Remove-AzureRmDeploymentManagerServiceUnit -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology -ServiceName ContosoService1  -Name ContosoService1Storage
```

<span data-ttu-id="791e3-118">Bu komut, ContosoService1Storage adlı bir hizmet biriminin altında, ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="791e3-118">This command deletes a service unit named ContosoService1Storage under a service ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="791e3-119">Örnek 2: kaynak tanımlayıcısını kullanarak hizmet birimini silme.</span><span class="sxs-lookup"><span data-stu-id="791e3-119">Example 2: Delete a service unit using the resource identifier.</span></span>
```powershell
PS C:\> Remove-AzureRmDeploymentManagerServiceUnit -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology/services/ContosoService1/serviceUnits/ContosoService1Storage"
```

<span data-ttu-id="791e3-120">Bu komut, ContosoService1Storage adlı bir hizmet biriminin altında, ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="791e3-120">This command gets a service unit named ContosoService1Storage under a service ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="791e3-121">Örnek 3: hizmet birimi nesnesini kullanarak hizmet birimini silme.</span><span class="sxs-lookup"><span data-stu-id="791e3-121">Example 3: Delete a service unit using the service unit object.</span></span>
```powershell
PS C:\> Remove-AzureRmDeploymentManagerServiceUnit -ServiceUnit $serviceUnitObject
```

<span data-ttu-id="791e3-122">Bu komut adı, hizmet adı, hizmet topolojisi adı ve ResourceGroup, sırasıyla adı, HizmetAdı, ServiceTopologyName ve ResourceGroupName $serviceUnitObject özellikleriyle eşleşen bir hizmet birimini siler.</span><span class="sxs-lookup"><span data-stu-id="791e3-122">This command deletes a service unit whose name, service name, service topology name and ResourceGroup match the Name, ServiceName, ServiceTopologyName and ResourceGroupName properties of the $serviceUnitObject, respectively.</span></span>

## <span data-ttu-id="791e3-123">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="791e3-123">PARAMETERS</span></span>

### <span data-ttu-id="791e3-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="791e3-124">-DefaultProfile</span></span>
<span data-ttu-id="791e3-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="791e3-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="791e3-126">-Force</span><span class="sxs-lookup"><span data-stu-id="791e3-126">-Force</span></span>
<span data-ttu-id="791e3-127">Onay sorma.</span><span class="sxs-lookup"><span data-stu-id="791e3-127">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="791e3-128">-Ad</span><span class="sxs-lookup"><span data-stu-id="791e3-128">-Name</span></span>
<span data-ttu-id="791e3-129">Silinecek hizmet biriminin adı.</span><span class="sxs-lookup"><span data-stu-id="791e3-129">The name of the service unit to delete.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive, ByTopologyObjectAndServiceName, ByTopologyResourceAndServiceName, ByServiceObject, ByServiceResourceId
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="791e3-130">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="791e3-130">-PassThru</span></span>
<span data-ttu-id="791e3-131">{{Dolgu geçiş açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="791e3-131">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="791e3-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="791e3-132">-ResourceGroupName</span></span>
<span data-ttu-id="791e3-133">Kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="791e3-133">The resource group.</span></span>

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

### <span data-ttu-id="791e3-134">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="791e3-134">-ResourceId</span></span>
<span data-ttu-id="791e3-135">Kaynak tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="791e3-135">The resource identifier.</span></span>

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

### <span data-ttu-id="791e3-136">-Hizmet</span><span class="sxs-lookup"><span data-stu-id="791e3-136">-Service</span></span>
<span data-ttu-id="791e3-137">Hizmet biriminin oluşturulması gereken servis nesnesi.</span><span class="sxs-lookup"><span data-stu-id="791e3-137">The service object in which the service unit should be created.</span></span>

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

### <span data-ttu-id="791e3-138">-HizmetAdı</span><span class="sxs-lookup"><span data-stu-id="791e3-138">-ServiceName</span></span>
<span data-ttu-id="791e3-139">Hizmet biriminin ait olduğu hizmetin adı.</span><span class="sxs-lookup"><span data-stu-id="791e3-139">The name of the service the service unit belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive, ByTopologyObjectAndServiceName, ByTopologyResourceAndServiceName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="791e3-140">-ServiceResourceId</span><span class="sxs-lookup"><span data-stu-id="791e3-140">-ServiceResourceId</span></span>
<span data-ttu-id="791e3-141">Hizmet biriminin oluşturulması gereken hizmet kaynak tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="791e3-141">The service resource identifier in which the service unit should be created.</span></span>

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

### <span data-ttu-id="791e3-142">-ServiceTopology</span><span class="sxs-lookup"><span data-stu-id="791e3-142">-ServiceTopology</span></span>
<span data-ttu-id="791e3-143">Hizmet biriminin oluşturulması gereken hizmet topolojisi nesnesi.</span><span class="sxs-lookup"><span data-stu-id="791e3-143">The service topology object in which the service unit should be created.</span></span>

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

### <span data-ttu-id="791e3-144">-ServiceTopologyName</span><span class="sxs-lookup"><span data-stu-id="791e3-144">-ServiceTopologyName</span></span>
<span data-ttu-id="791e3-145">Hizmet biriminin ait olduğu hizmet topolojisinin adı.</span><span class="sxs-lookup"><span data-stu-id="791e3-145">The name of the service topology the service unit belongs to.</span></span>

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

### <span data-ttu-id="791e3-146">-Servicetopologyresourceıd</span><span class="sxs-lookup"><span data-stu-id="791e3-146">-ServiceTopologyResourceId</span></span>
<span data-ttu-id="791e3-147">Hizmet biriminin oluşturulması gereken hizmet topolojisi kaynak tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="791e3-147">The service topology resource identifier in which the service unit should be created.</span></span>

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

### <span data-ttu-id="791e3-148">-ServiceUnit</span><span class="sxs-lookup"><span data-stu-id="791e3-148">-ServiceUnit</span></span>
<span data-ttu-id="791e3-149">Kaldırılacak kaynak.</span><span class="sxs-lookup"><span data-stu-id="791e3-149">The resource to be removed.</span></span>

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

### <span data-ttu-id="791e3-150">-Onay</span><span class="sxs-lookup"><span data-stu-id="791e3-150">-Confirm</span></span>
<span data-ttu-id="791e3-151">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="791e3-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="791e3-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="791e3-152">-WhatIf</span></span>
<span data-ttu-id="791e3-153">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="791e3-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="791e3-154">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="791e3-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="791e3-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="791e3-155">CommonParameters</span></span>
<span data-ttu-id="791e3-156">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="791e3-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="791e3-157">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="791e3-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="791e3-158">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="791e3-158">INPUTS</span></span>

### <span data-ttu-id="791e3-159">Microsoft. Azure. Commands. DeploymentManager. modeller. PSServiceUnitResource</span><span class="sxs-lookup"><span data-stu-id="791e3-159">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span></span>

## <span data-ttu-id="791e3-160">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="791e3-160">OUTPUTS</span></span>

### <span data-ttu-id="791e3-161">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="791e3-161">System.Boolean</span></span>

## <span data-ttu-id="791e3-162">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="791e3-162">NOTES</span></span>

## <span data-ttu-id="791e3-163">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="791e3-163">RELATED LINKS</span></span>

[<span data-ttu-id="791e3-164">Yeni-AzureRmDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="791e3-164">New-AzureRmDeploymentManagerServiceUnit</span></span>](./New-AzureRmDeploymentManagerServiceUnit.md)

[<span data-ttu-id="791e3-165">Get-AzureRmDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="791e3-165">Get-AzureRmDeploymentManagerServiceUnit</span></span>](./Get-AzureRmDeploymentManagerServiceUnit.md)

[<span data-ttu-id="791e3-166">Set-AzureRmDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="791e3-166">Set-AzureRmDeploymentManagerServiceUnit</span></span>](./Set-AzureRmDeploymentManagerServiceUnit.md)