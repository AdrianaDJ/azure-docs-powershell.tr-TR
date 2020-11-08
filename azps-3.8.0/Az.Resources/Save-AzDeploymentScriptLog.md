---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/save-azdeploymentscriptlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzDeploymentScriptLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzDeploymentScriptLog.md
ms.openlocfilehash: 4e32726b3e7af6608092d29fd52f7a41be042d42
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94097265"
---
# <span data-ttu-id="0c1d3-101">Save-AzDeploymentScriptLog</span><span class="sxs-lookup"><span data-stu-id="0c1d3-101">Save-AzDeploymentScriptLog</span></span>

## <span data-ttu-id="0c1d3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0c1d3-102">SYNOPSIS</span></span>
<span data-ttu-id="0c1d3-103">Dağıtım betiği yürütme günlüğünü diske kaydeder.</span><span class="sxs-lookup"><span data-stu-id="0c1d3-103">Saves the log of a deployment script execution to disk.</span></span>

## <span data-ttu-id="0c1d3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0c1d3-104">SYNTAX</span></span>

### <span data-ttu-id="0c1d3-105">SaveDeploymentScriptLogByName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="0c1d3-105">SaveDeploymentScriptLogByName (Default)</span></span>
```
Save-AzDeploymentScriptLog [-ResourceGroupName] <String> [-Name] <String> [-OutputPath] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0c1d3-106">Savedeploymentscriptlogbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="0c1d3-106">SaveDeploymentScriptLogByResourceId</span></span>
```
Save-AzDeploymentScriptLog [-DeploymentScriptResourceId] <String> [-OutputPath] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0c1d3-107">SaveDeploymentScriptLogByInputObject</span><span class="sxs-lookup"><span data-stu-id="0c1d3-107">SaveDeploymentScriptLogByInputObject</span></span>
```
Save-AzDeploymentScriptLog [-DeploymentScriptInputObject] <PsDeploymentScript> [-OutputPath] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0c1d3-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="0c1d3-108">DESCRIPTION</span></span>
<span data-ttu-id="0c1d3-109">**Save-AzDeploymentScriptLog** , dağıtım betiği yürütme günlüğünü diske kaydeder.</span><span class="sxs-lookup"><span data-stu-id="0c1d3-109">The **Save-AzDeploymentScriptLog** saves the log of a deployment script execution to disk.</span></span>

## <span data-ttu-id="0c1d3-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0c1d3-110">EXAMPLES</span></span>

### <span data-ttu-id="0c1d3-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="0c1d3-111">Example 1</span></span>
```powershell
PS C:\> Save-AzDeploymentScriptLog -Name MyDeploymentScript -ResourceGroupName DS-TestRg -OutputPath C:\Workspace
```

<span data-ttu-id="0c1d3-112">Bir dağıtım komut dosyasının günlüğünü verilen ad ve kaynak grubuyla kaydeder.</span><span class="sxs-lookup"><span data-stu-id="0c1d3-112">Saves the log of a deployment script with the given name and resource group.</span></span>

## <span data-ttu-id="0c1d3-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0c1d3-113">PARAMETERS</span></span>

### <span data-ttu-id="0c1d3-114">-Onay</span><span class="sxs-lookup"><span data-stu-id="0c1d3-114">-Confirm</span></span>
<span data-ttu-id="0c1d3-115">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="0c1d3-115">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c1d3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c1d3-116">-DefaultProfile</span></span>
<span data-ttu-id="0c1d3-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0c1d3-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c1d3-118">-DeploymentScriptInputObject</span><span class="sxs-lookup"><span data-stu-id="0c1d3-118">-DeploymentScriptInputObject</span></span>
<span data-ttu-id="0c1d3-119">Dağıtım betiği PowerShell nesnesi.</span><span class="sxs-lookup"><span data-stu-id="0c1d3-119">The deployment script PowerShell object.</span></span>

```yaml
Type: PsDeploymentScript
Parameter Sets: SaveDeploymentScriptLogByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c1d3-120">-Deploymentscriptresourceıd</span><span class="sxs-lookup"><span data-stu-id="0c1d3-120">-DeploymentScriptResourceId</span></span>
<span data-ttu-id="0c1d3-121">Dağıtım komut dosyasının tam nitelikli kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="0c1d3-121">The fully qualified resource Id of the deployment script.</span></span>
<span data-ttu-id="0c1d3-122">Örnek:/subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span><span class="sxs-lookup"><span data-stu-id="0c1d3-122">Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span></span>

```yaml
Type: String
Parameter Sets: SaveDeploymentScriptLogByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c1d3-123">-Force</span><span class="sxs-lookup"><span data-stu-id="0c1d3-123">-Force</span></span>
<span data-ttu-id="0c1d3-124">Var olan dosyanın üzerine yazmayı zorlar.</span><span class="sxs-lookup"><span data-stu-id="0c1d3-124">Forces the overwrite of the existing file.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c1d3-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="0c1d3-125">-Name</span></span>
<span data-ttu-id="0c1d3-126">Dağıtım komut dosyasının adı.</span><span class="sxs-lookup"><span data-stu-id="0c1d3-126">The name of the deployment script.</span></span>

```yaml
Type: String
Parameter Sets: SaveDeploymentScriptLogByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c1d3-127">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="0c1d3-127">-OutputPath</span></span>
<span data-ttu-id="0c1d3-128">Dağıtım komut dosyası günlüğünün kaydedileceği dizin yolu.</span><span class="sxs-lookup"><span data-stu-id="0c1d3-128">The directory path to save deployment script log.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c1d3-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0c1d3-129">-ResourceGroupName</span></span>
<span data-ttu-id="0c1d3-130">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="0c1d3-130">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: SaveDeploymentScriptLogByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c1d3-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0c1d3-131">-WhatIf</span></span>
<span data-ttu-id="0c1d3-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="0c1d3-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0c1d3-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="0c1d3-133">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c1d3-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c1d3-134">CommonParameters</span></span>
<span data-ttu-id="0c1d3-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0c1d3-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="0c1d3-136">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0c1d3-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c1d3-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0c1d3-137">INPUTS</span></span>

### <span data-ttu-id="0c1d3-138">System. String</span><span class="sxs-lookup"><span data-stu-id="0c1d3-138">System.String</span></span>

## <span data-ttu-id="0c1d3-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0c1d3-139">OUTPUTS</span></span>

### <span data-ttu-id="0c1d3-140">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScriptLogPath</span><span class="sxs-lookup"><span data-stu-id="0c1d3-140">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScriptLogPath</span></span>

## <span data-ttu-id="0c1d3-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0c1d3-141">NOTES</span></span>

## <span data-ttu-id="0c1d3-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0c1d3-142">RELATED LINKS</span></span>
