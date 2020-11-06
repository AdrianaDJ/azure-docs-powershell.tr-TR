---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/remove-azurermdeploymentmanagerartifactsource
schema: 2.0.0
ms.openlocfilehash: 7473f125511995efb1f6273d3b8adb675a58d06d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93571429"
---
# <span data-ttu-id="372a3-101">Remove-AzureRmDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="372a3-101">Remove-AzureRmDeploymentManagerArtifactSource</span></span>

## <span data-ttu-id="372a3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="372a3-102">SYNOPSIS</span></span>
<span data-ttu-id="372a3-103">Yapıt kaynağını siler.</span><span class="sxs-lookup"><span data-stu-id="372a3-103">Deletes an artifact source.</span></span>

## <span data-ttu-id="372a3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="372a3-104">SYNTAX</span></span>

### <span data-ttu-id="372a3-105">Etkileşimli (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="372a3-105">Interactive (Default)</span></span>
```
Remove-AzureRmDeploymentManagerArtifactSource [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="372a3-106">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="372a3-106">ResourceId</span></span>
```
Remove-AzureRmDeploymentManagerArtifactSource [-ResourceId] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="372a3-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="372a3-107">InputObject</span></span>
```
Remove-AzureRmDeploymentManagerArtifactSource [-ArtifactSource] <PSArtifactSource> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="372a3-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="372a3-108">DESCRIPTION</span></span>
<span data-ttu-id="372a3-109">**Remove-AzureRmDeploymentManagerArtifactSource** cmdlet 'i bir yapıt kaynağını siler yapıt kaynağını adına ve kaynak grup adına göre belirtir.</span><span class="sxs-lookup"><span data-stu-id="372a3-109">The **Remove-AzureRmDeploymentManagerArtifactSource** cmdlet deletes an artifact source Specify the artifact source by its name and resource group name.</span></span> <span data-ttu-id="372a3-110">Alternatif olarak, ArtifactSource nesnesini veya RESOURCEID 'yi de sağlayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="372a3-110">Alternately, you can provide the ArtifactSource object or the ResourceId.</span></span>

## <span data-ttu-id="372a3-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="372a3-111">EXAMPLES</span></span>

### <span data-ttu-id="372a3-112">Örnek 1: yapıt kaynağını silme</span><span class="sxs-lookup"><span data-stu-id="372a3-112">Example 1: Delete an artifact source</span></span>
```powershell
PS C:\> Remove-AzureRmDeploymentManagerArtifactSource -ResourceGroupName "ContosoResourceGroup" -Name "ContosoArtifactSource"
```

<span data-ttu-id="372a3-113">Bu komut, ContosoResourceGroup 'ta ContosoArtifactSource adlı bir yapıt kaynağını siler.</span><span class="sxs-lookup"><span data-stu-id="372a3-113">This command deletes an artifact source named ContosoArtifactSource in ContosoResourceGroup.</span></span>

### <span data-ttu-id="372a3-114">Örnek 2: kaynak tanımlayıcısını kullanarak yapıt kaynağını silme</span><span class="sxs-lookup"><span data-stu-id="372a3-114">Example 2: Delete an artifact source using the resource identifier</span></span>
```powershell
PS C:\> Remove-AzureRmDeploymentManagerArtifactSource -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/artifactSources/ContosoArtifactSource"
```

<span data-ttu-id="372a3-115">Bu komut, ContosoResourceGroup 'ta ContosoArtifactSource adlı bir yapıt kaynağını siler.</span><span class="sxs-lookup"><span data-stu-id="372a3-115">This command deletes an artifact source named ContosoArtifactSource in ContosoResourceGroup.</span></span>

### <span data-ttu-id="372a3-116">Örnek 3: nesne kullanarak yapıt kaynağını silme</span><span class="sxs-lookup"><span data-stu-id="372a3-116">Example 3: Delete an artifact source using an object</span></span>
```powershell
PS C:\> Remove-AzureRmDeploymentManagerArtifactSource -ArtifactSource $artifactSourceObject
```

<span data-ttu-id="372a3-117">Bu komut, adı ve ResourceGroup 'in sırasıyla $artifactSourceObject Name ve ResourceGroupName özellikleriyle eşleşen bir yapıt kaynağını siler.</span><span class="sxs-lookup"><span data-stu-id="372a3-117">This command deletes an artifact source whose name and ResourceGroup match the Name and ResourceGroupName properties of the $artifactSourceObject, respectively.</span></span>

## <span data-ttu-id="372a3-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="372a3-118">PARAMETERS</span></span>

### <span data-ttu-id="372a3-119">-ArtifactSource</span><span class="sxs-lookup"><span data-stu-id="372a3-119">-ArtifactSource</span></span>
<span data-ttu-id="372a3-120">Kaldırılacak yapıt deposu.</span><span class="sxs-lookup"><span data-stu-id="372a3-120">The artifact store to be removed.</span></span>

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

### <span data-ttu-id="372a3-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="372a3-121">-DefaultProfile</span></span>
<span data-ttu-id="372a3-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="372a3-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="372a3-123">-Force</span><span class="sxs-lookup"><span data-stu-id="372a3-123">-Force</span></span>
<span data-ttu-id="372a3-124">Onay sorma.</span><span class="sxs-lookup"><span data-stu-id="372a3-124">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="372a3-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="372a3-125">-Name</span></span>
<span data-ttu-id="372a3-126">Yapıt kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="372a3-126">The name of the artifact source.</span></span>

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

### <span data-ttu-id="372a3-127">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="372a3-127">-PassThru</span></span>
<span data-ttu-id="372a3-128">{{Dolgu geçiş açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="372a3-128">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="372a3-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="372a3-129">-ResourceGroupName</span></span>
<span data-ttu-id="372a3-130">Kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="372a3-130">The resource group.</span></span>

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

### <span data-ttu-id="372a3-131">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="372a3-131">-ResourceId</span></span>
<span data-ttu-id="372a3-132">Kaynak tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="372a3-132">The resource identifier.</span></span>

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

### <span data-ttu-id="372a3-133">-Onay</span><span class="sxs-lookup"><span data-stu-id="372a3-133">-Confirm</span></span>
<span data-ttu-id="372a3-134">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="372a3-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="372a3-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="372a3-135">-WhatIf</span></span>
<span data-ttu-id="372a3-136">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="372a3-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="372a3-137">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="372a3-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="372a3-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="372a3-138">CommonParameters</span></span>
<span data-ttu-id="372a3-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="372a3-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="372a3-140">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="372a3-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="372a3-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="372a3-141">INPUTS</span></span>

### <span data-ttu-id="372a3-142">Microsoft. Azure. Commands. DeploymentManager. modeller. PSArtifactSource</span><span class="sxs-lookup"><span data-stu-id="372a3-142">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="372a3-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="372a3-143">OUTPUTS</span></span>

### <span data-ttu-id="372a3-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="372a3-144">System.Boolean</span></span>

## <span data-ttu-id="372a3-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="372a3-145">NOTES</span></span>

## <span data-ttu-id="372a3-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="372a3-146">RELATED LINKS</span></span>

[<span data-ttu-id="372a3-147">Yeni-AzureRmDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="372a3-147">New-AzureRmDeploymentManagerArtifactSource</span></span>](./New-AzureRmDeploymentManagerArtifactSource.md)

[<span data-ttu-id="372a3-148">Get-AzureRmDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="372a3-148">Get-AzureRmDeploymentManagerArtifactSource</span></span>](./Get-AzureRmDeploymentManagerArtifactSource.md)

[<span data-ttu-id="372a3-149">Set-AzureRmDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="372a3-149">Set-AzureRmDeploymentManagerArtifactSource</span></span>](./Set-AzureRmDeploymentManagerArtifactSource.md)