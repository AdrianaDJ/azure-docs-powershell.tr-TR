---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/remove-azurermdeploymentmanagerservicetopology
schema: 2.0.0
ms.openlocfilehash: be95f5fffe4483c74d8b1438819cf084eaa0693b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93571509"
---
# <span data-ttu-id="1ea3f-101">Remove-AzureRmDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="1ea3f-101">Remove-AzureRmDeploymentManagerServiceTopology</span></span>

## <span data-ttu-id="1ea3f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1ea3f-102">SYNOPSIS</span></span>
<span data-ttu-id="1ea3f-103">Hizmet topolojisini ve tüm kaynaklarını siler.</span><span class="sxs-lookup"><span data-stu-id="1ea3f-103">Deletes a service topology and all its resources.</span></span>

## <span data-ttu-id="1ea3f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1ea3f-104">SYNTAX</span></span>

### <span data-ttu-id="1ea3f-105">Etkileşimli (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="1ea3f-105">Interactive (Default)</span></span>
```
Remove-AzureRmDeploymentManagerServiceTopology [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1ea3f-106">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="1ea3f-106">ResourceId</span></span>
```
Remove-AzureRmDeploymentManagerServiceTopology [-ResourceId] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1ea3f-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="1ea3f-107">InputObject</span></span>
```
Remove-AzureRmDeploymentManagerServiceTopology [-ServiceTopology] <PSServiceTopologyResource> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1ea3f-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="1ea3f-108">DESCRIPTION</span></span>
<span data-ttu-id="1ea3f-109">**Remove-AzureRmDeploymentManagerServiceTopology** cmdlet 'i bir hizmet topolojisini siler.</span><span class="sxs-lookup"><span data-stu-id="1ea3f-109">The **Remove-AzureRmDeploymentManagerServiceTopology** cmdlet deletes a service topology.</span></span>

<span data-ttu-id="1ea3f-110">Hizmet topolojisini adına ve kaynak grubu adına göre belirtin.</span><span class="sxs-lookup"><span data-stu-id="1ea3f-110">Specify the service topology by its name and the resource group name.</span></span> <span data-ttu-id="1ea3f-111">Alternatif olarak, ServiceTopology nesnesini veya RESOURCEID 'yi de sağlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1ea3f-111">Alternately, you can provide the ServiceTopology object or the ResourceId.</span></span>

## <span data-ttu-id="1ea3f-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1ea3f-112">EXAMPLES</span></span>

### <span data-ttu-id="1ea3f-113">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="1ea3f-113">Example 1</span></span>
```powershell
PS C:\> Remove-AzureRmDeploymentManagerServiceTopology -ResourceGroupName ContosoResourceGroup -Name ContosoServiceTopology
```

<span data-ttu-id="1ea3f-114">Bu komut, ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="1ea3f-114">This command deletes a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="1ea3f-115">Örnek 2: kaynak tanımlayıcısını kullanarak hizmet topolojisini silme.</span><span class="sxs-lookup"><span data-stu-id="1ea3f-115">Example 2: Delete a service topology using the resource identifier.</span></span>
```powershell
PS C:\> Remove-AzureRmDeploymentManagerServiceTopology -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology"
```

<span data-ttu-id="1ea3f-116">Bu komut, ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="1ea3f-116">This command deletes a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="1ea3f-117">Örnek 3: hizmet topolojisi nesnesini kullanarak hizmet topolojisini silme.</span><span class="sxs-lookup"><span data-stu-id="1ea3f-117">Example 3: Delete a service topology using the service topology object.</span></span>
```powershell
PS C:\> Remove-AzureRmDeploymentManagerService -ServiceTopology $serviceTopologyObject
```

<span data-ttu-id="1ea3f-118">Bu komut, adı ve ResourceGroup 'in sırasıyla $serviceTopologyObject Name ve ResourceGroupName özellikleriyle eşleşen bir hizmet topolojisini siler.</span><span class="sxs-lookup"><span data-stu-id="1ea3f-118">This command deletes a service topology whose name and ResourceGroup match the Name and ResourceGroupName properties of the $serviceTopologyObject, respectively.</span></span>

## <span data-ttu-id="1ea3f-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1ea3f-119">PARAMETERS</span></span>

### <span data-ttu-id="1ea3f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ea3f-120">-DefaultProfile</span></span>
<span data-ttu-id="1ea3f-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1ea3f-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1ea3f-122">-Force</span><span class="sxs-lookup"><span data-stu-id="1ea3f-122">-Force</span></span>
<span data-ttu-id="1ea3f-123">Onay sorma.</span><span class="sxs-lookup"><span data-stu-id="1ea3f-123">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="1ea3f-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="1ea3f-124">-Name</span></span>
<span data-ttu-id="1ea3f-125">Hizmet topolojisinin adı.</span><span class="sxs-lookup"><span data-stu-id="1ea3f-125">The name of the service topology.</span></span>

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

### <span data-ttu-id="1ea3f-126">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="1ea3f-126">-PassThru</span></span>
<span data-ttu-id="1ea3f-127">{{Dolgu geçiş açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="1ea3f-127">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="1ea3f-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1ea3f-128">-ResourceGroupName</span></span>
<span data-ttu-id="1ea3f-129">Kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="1ea3f-129">The resource group.</span></span>

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

### <span data-ttu-id="1ea3f-130">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="1ea3f-130">-ResourceId</span></span>
<span data-ttu-id="1ea3f-131">Kaynak tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="1ea3f-131">The resource identifier.</span></span>

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

### <span data-ttu-id="1ea3f-132">-ServiceTopology</span><span class="sxs-lookup"><span data-stu-id="1ea3f-132">-ServiceTopology</span></span>
<span data-ttu-id="1ea3f-133">Kaldırılacak kaynak.</span><span class="sxs-lookup"><span data-stu-id="1ea3f-133">The resource to be removed.</span></span>

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

### <span data-ttu-id="1ea3f-134">-Onay</span><span class="sxs-lookup"><span data-stu-id="1ea3f-134">-Confirm</span></span>
<span data-ttu-id="1ea3f-135">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="1ea3f-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1ea3f-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1ea3f-136">-WhatIf</span></span>
<span data-ttu-id="1ea3f-137">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="1ea3f-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1ea3f-138">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="1ea3f-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1ea3f-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ea3f-139">CommonParameters</span></span>
<span data-ttu-id="1ea3f-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1ea3f-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ea3f-141">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1ea3f-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ea3f-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1ea3f-142">INPUTS</span></span>

### <span data-ttu-id="1ea3f-143">Microsoft. Azure. Commands. DeploymentManager. modeller. PSServiceTopologyResource</span><span class="sxs-lookup"><span data-stu-id="1ea3f-143">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span></span>

## <span data-ttu-id="1ea3f-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1ea3f-144">OUTPUTS</span></span>

### <span data-ttu-id="1ea3f-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1ea3f-145">System.Boolean</span></span>

## <span data-ttu-id="1ea3f-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1ea3f-146">NOTES</span></span>

## <span data-ttu-id="1ea3f-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1ea3f-147">RELATED LINKS</span></span>

[<span data-ttu-id="1ea3f-148">New-AzureRmDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="1ea3f-148">New-AzureRmDeploymentManagerServiceTopology</span></span>](./New-AzureRmDeploymentManagerServiceTopology.md)

[<span data-ttu-id="1ea3f-149">Get-AzureRmDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="1ea3f-149">Get-AzureRmDeploymentManagerServiceTopology</span></span>](./Get-AzureRmDeploymentManagerServiceTopology.md)

[<span data-ttu-id="1ea3f-150">Set-AzureRmDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="1ea3f-150">Set-AzureRmDeploymentManagerServiceTopology</span></span>](./Set-AzureRmDeploymentManagerServiceTopology.md)