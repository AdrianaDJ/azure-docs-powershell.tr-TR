---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/remove-azdeploymentmanagerartifactsource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerArtifactSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerArtifactSource.md
ms.openlocfilehash: fa9dc4f8234e9c6e709d59f3945b05eeceef4316
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94320122"
---
# <span data-ttu-id="b7dc6-101">Remove-AzDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="b7dc6-101">Remove-AzDeploymentManagerArtifactSource</span></span>

## <span data-ttu-id="b7dc6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b7dc6-102">SYNOPSIS</span></span>
<span data-ttu-id="b7dc6-103">Belirtilen yapıt kaynağını siler.</span><span class="sxs-lookup"><span data-stu-id="b7dc6-103">Deletes the specified artifact source.</span></span>

## <span data-ttu-id="b7dc6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b7dc6-104">SYNTAX</span></span>

### <span data-ttu-id="b7dc6-105">Etkileşimli (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="b7dc6-105">Interactive (Default)</span></span>
```
Remove-AzDeploymentManagerArtifactSource [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b7dc6-106">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="b7dc6-106">ResourceId</span></span>
```
Remove-AzDeploymentManagerArtifactSource [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b7dc6-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="b7dc6-107">InputObject</span></span>
```
Remove-AzDeploymentManagerArtifactSource [-InputObject] <PSArtifactSource> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b7dc6-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="b7dc6-108">DESCRIPTION</span></span>
<span data-ttu-id="b7dc6-109">**Remove-AzDeploymentManagerArtifactSource** cmdlet 'i bir yapıt kaynağını siler yapıt kaynağını adına ve kaynak grup adına göre belirtin.</span><span class="sxs-lookup"><span data-stu-id="b7dc6-109">The **Remove-AzDeploymentManagerArtifactSource** cmdlet deletes an artifact source Specify the artifact source by its name and resource group name.</span></span> <span data-ttu-id="b7dc6-110">Alternatif olarak, ArtifactSource nesnesini veya RESOURCEID 'yi de sağlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b7dc6-110">Alternately, you can provide the ArtifactSource object or the ResourceId.</span></span>

## <span data-ttu-id="b7dc6-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b7dc6-111">EXAMPLES</span></span>

### <span data-ttu-id="b7dc6-112">Örnek 1: yapıt kaynağını silme</span><span class="sxs-lookup"><span data-stu-id="b7dc6-112">Example 1: Delete an artifact source</span></span>
### <span data-ttu-id="b7dc6-113">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="b7dc6-113">Example 1</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerArtifactSource -ResourceGroupName "ContosoResourceGroup" -Name "ContosoArtifactSource"
```

<span data-ttu-id="b7dc6-114">Bu komut, ContosoResourceGroup 'ta ContosoArtifactSource adlı bir yapıt kaynağını siler.</span><span class="sxs-lookup"><span data-stu-id="b7dc6-114">This command deletes an artifact source named ContosoArtifactSource in ContosoResourceGroup.</span></span>

### <span data-ttu-id="b7dc6-115">Örnek 2: kaynak tanımlayıcısını kullanarak yapıt kaynağını silme</span><span class="sxs-lookup"><span data-stu-id="b7dc6-115">Example 2: Delete an artifact source using the resource identifier</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerArtifactSource -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/artifactSources/ContosoArtifactSource"
```

<span data-ttu-id="b7dc6-116">Bu komut, ContosoResourceGroup 'ta ContosoArtifactSource adlı bir yapıt kaynağını siler.</span><span class="sxs-lookup"><span data-stu-id="b7dc6-116">This command deletes an artifact source named ContosoArtifactSource in ContosoResourceGroup.</span></span>

### <span data-ttu-id="b7dc6-117">Örnek 3: nesne kullanarak yapıt kaynağını silme</span><span class="sxs-lookup"><span data-stu-id="b7dc6-117">Example 3: Delete an artifact source using an object</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerArtifactSource -InputObject $artifactSourceObject
```

<span data-ttu-id="b7dc6-118">Bu komut, adı ve ResourceGroup 'in sırasıyla $artifactSourceObject Name ve ResourceGroupName özellikleriyle eşleşen bir yapıt kaynağını siler.</span><span class="sxs-lookup"><span data-stu-id="b7dc6-118">This command deletes an artifact source whose name and ResourceGroup match the Name and ResourceGroupName properties of the $artifactSourceObject, respectively.</span></span>

## <span data-ttu-id="b7dc6-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b7dc6-119">PARAMETERS</span></span>

### <span data-ttu-id="b7dc6-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7dc6-120">-DefaultProfile</span></span>
<span data-ttu-id="b7dc6-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b7dc6-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b7dc6-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b7dc6-122">-InputObject</span></span>
<span data-ttu-id="b7dc6-123">Kaldırılacak yapıt kaynağı.</span><span class="sxs-lookup"><span data-stu-id="b7dc6-123">The artifact source to be removed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b7dc6-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="b7dc6-124">-Name</span></span>
<span data-ttu-id="b7dc6-125">Yapıt kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="b7dc6-125">The name of the artifact source.</span></span>

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

### <span data-ttu-id="b7dc6-126">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="b7dc6-126">-PassThru</span></span>
<span data-ttu-id="b7dc6-127">{{Dolgu geçiş açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="b7dc6-127">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="b7dc6-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7dc6-128">-ResourceGroupName</span></span>
<span data-ttu-id="b7dc6-129">Kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="b7dc6-129">The resource group.</span></span>

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

### <span data-ttu-id="b7dc6-130">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="b7dc6-130">-ResourceId</span></span>
<span data-ttu-id="b7dc6-131">Kaynak tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="b7dc6-131">The resource identifier.</span></span>

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

### <span data-ttu-id="b7dc6-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="b7dc6-132">-Confirm</span></span>
<span data-ttu-id="b7dc6-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b7dc6-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b7dc6-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b7dc6-134">-WhatIf</span></span>
<span data-ttu-id="b7dc6-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b7dc6-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b7dc6-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b7dc6-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b7dc6-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7dc6-137">CommonParameters</span></span>
<span data-ttu-id="b7dc6-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b7dc6-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7dc6-139">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="b7dc6-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7dc6-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b7dc6-140">INPUTS</span></span>

### <span data-ttu-id="b7dc6-141">System. String</span><span class="sxs-lookup"><span data-stu-id="b7dc6-141">System.String</span></span>

### <span data-ttu-id="b7dc6-142">Microsoft. Azure. Commands. DeploymentManager. modeller. PSArtifactSource</span><span class="sxs-lookup"><span data-stu-id="b7dc6-142">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="b7dc6-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b7dc6-143">OUTPUTS</span></span>

### <span data-ttu-id="b7dc6-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b7dc6-144">System.Boolean</span></span>

## <span data-ttu-id="b7dc6-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b7dc6-145">NOTES</span></span>

## <span data-ttu-id="b7dc6-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b7dc6-146">RELATED LINKS</span></span>
