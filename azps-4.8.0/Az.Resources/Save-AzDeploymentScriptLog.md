---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/save-azdeploymentscriptlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzDeploymentScriptLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzDeploymentScriptLog.md
ms.openlocfilehash: 25f20b56ef7da59851d4726ad573c07d4da259e1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94266412"
---
# <span data-ttu-id="91b17-101">Save-AzDeploymentScriptLog</span><span class="sxs-lookup"><span data-stu-id="91b17-101">Save-AzDeploymentScriptLog</span></span>

## <span data-ttu-id="91b17-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="91b17-102">SYNOPSIS</span></span>
<span data-ttu-id="91b17-103">Dağıtım betiği yürütme günlüğünü diske kaydeder.</span><span class="sxs-lookup"><span data-stu-id="91b17-103">Saves the log of a deployment script execution to disk.</span></span>

## <span data-ttu-id="91b17-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="91b17-104">SYNTAX</span></span>

### <span data-ttu-id="91b17-105">SaveDeploymentScriptLogByName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="91b17-105">SaveDeploymentScriptLogByName (Default)</span></span>
```
Save-AzDeploymentScriptLog [-ResourceGroupName] <String> [-Name] <String> [-OutputPath] <String>
 [[-Tail] <Int32>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="91b17-106">Savedeploymentscriptlogbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="91b17-106">SaveDeploymentScriptLogByResourceId</span></span>
```
Save-AzDeploymentScriptLog [-DeploymentScriptResourceId] <String> [-OutputPath] <String> [[-Tail] <Int32>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="91b17-107">SaveDeploymentScriptLogByInputObject</span><span class="sxs-lookup"><span data-stu-id="91b17-107">SaveDeploymentScriptLogByInputObject</span></span>
```
Save-AzDeploymentScriptLog [-DeploymentScriptObject] <PsDeploymentScript> [-OutputPath] <String>
 [[-Tail] <Int32>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="91b17-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="91b17-108">DESCRIPTION</span></span>
<span data-ttu-id="91b17-109">**Save-AzDeploymentScriptLog** , dağıtım betiği yürütme günlüğünü diske kaydeder.</span><span class="sxs-lookup"><span data-stu-id="91b17-109">The **Save-AzDeploymentScriptLog** saves the log of a deployment script execution to disk.</span></span>

## <span data-ttu-id="91b17-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="91b17-110">EXAMPLES</span></span>

### <span data-ttu-id="91b17-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="91b17-111">Example 1</span></span>
```powershell
PS C:\> Save-AzDeploymentScriptLog -Name MyDeploymentScript -ResourceGroupName DS-TestRg -OutputPath C:\Workspace
```

<span data-ttu-id="91b17-112">Bir dağıtım komut dosyasının günlüğünü verilen ad ve kaynak grubuyla kaydeder.</span><span class="sxs-lookup"><span data-stu-id="91b17-112">Saves the log of a deployment script with the given name and resource group.</span></span>

### <span data-ttu-id="91b17-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="91b17-113">Example 2</span></span>
```powershell
PS C:\> Save-AzDeploymentScriptLog -Name MyDeploymentScript -ResourceGroupName DS-TestRg -OutputPath C:\Workspace -Tail 3
```

<span data-ttu-id="91b17-114">Verilen ad ve kaynak grubuyla bir dağıtım betiği günlüğünün son 3 satırını kaydeder.</span><span class="sxs-lookup"><span data-stu-id="91b17-114">Saves the last 3 lines of the log of a deployment script with the given name and resource group.</span></span>

## <span data-ttu-id="91b17-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="91b17-115">PARAMETERS</span></span>

### <span data-ttu-id="91b17-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91b17-116">-DefaultProfile</span></span>
<span data-ttu-id="91b17-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="91b17-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="91b17-118">-DeploymentScriptObject</span><span class="sxs-lookup"><span data-stu-id="91b17-118">-DeploymentScriptObject</span></span>
<span data-ttu-id="91b17-119">Dağıtım betiği PowerShell nesnesi.</span><span class="sxs-lookup"><span data-stu-id="91b17-119">The deployment script PowerShell object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript
Parameter Sets: SaveDeploymentScriptLogByInputObject
Aliases: DeploymentScriptInputObject

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="91b17-120">-Deploymentscriptresourceıd</span><span class="sxs-lookup"><span data-stu-id="91b17-120">-DeploymentScriptResourceId</span></span>
<span data-ttu-id="91b17-121">Dağıtım komut dosyasının tam nitelikli kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="91b17-121">The fully qualified resource Id of the deployment script.</span></span>
<span data-ttu-id="91b17-122">Örnek:/subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span><span class="sxs-lookup"><span data-stu-id="91b17-122">Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span></span>

```yaml
Type: System.String
Parameter Sets: SaveDeploymentScriptLogByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91b17-123">-Force</span><span class="sxs-lookup"><span data-stu-id="91b17-123">-Force</span></span>
<span data-ttu-id="91b17-124">Var olan dosyanın üzerine yazmayı zorlar.</span><span class="sxs-lookup"><span data-stu-id="91b17-124">Forces the overwrite of the existing file.</span></span>

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

### <span data-ttu-id="91b17-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="91b17-125">-Name</span></span>
<span data-ttu-id="91b17-126">Dağıtım komut dosyasının adı.</span><span class="sxs-lookup"><span data-stu-id="91b17-126">The name of the deployment script.</span></span>

```yaml
Type: System.String
Parameter Sets: SaveDeploymentScriptLogByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91b17-127">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="91b17-127">-OutputPath</span></span>
<span data-ttu-id="91b17-128">Dağıtım komut dosyası günlüğünün kaydedileceği dizin yolu.</span><span class="sxs-lookup"><span data-stu-id="91b17-128">The directory path to save deployment script log.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91b17-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91b17-129">-ResourceGroupName</span></span>
<span data-ttu-id="91b17-130">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="91b17-130">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: SaveDeploymentScriptLogByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91b17-131">Kuyruklu</span><span class="sxs-lookup"><span data-stu-id="91b17-131">-Tail</span></span>
<span data-ttu-id="91b17-132">Çıktıyı son n satırla sınırla</span><span class="sxs-lookup"><span data-stu-id="91b17-132">Limit output to last n lines</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91b17-133">-Onay</span><span class="sxs-lookup"><span data-stu-id="91b17-133">-Confirm</span></span>
<span data-ttu-id="91b17-134">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="91b17-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="91b17-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="91b17-135">-WhatIf</span></span>
<span data-ttu-id="91b17-136">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="91b17-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="91b17-137">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="91b17-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="91b17-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91b17-138">CommonParameters</span></span>
<span data-ttu-id="91b17-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="91b17-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91b17-140">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="91b17-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91b17-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="91b17-141">INPUTS</span></span>

### <span data-ttu-id="91b17-142">System. String</span><span class="sxs-lookup"><span data-stu-id="91b17-142">System.String</span></span>

## <span data-ttu-id="91b17-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="91b17-143">OUTPUTS</span></span>

### <span data-ttu-id="91b17-144">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScriptLogPath</span><span class="sxs-lookup"><span data-stu-id="91b17-144">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScriptLogPath</span></span>

## <span data-ttu-id="91b17-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="91b17-145">NOTES</span></span>

## <span data-ttu-id="91b17-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="91b17-146">RELATED LINKS</span></span>
