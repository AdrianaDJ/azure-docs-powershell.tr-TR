---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azdeploymentscript
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzDeploymentScript.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzDeploymentScript.md
ms.openlocfilehash: 647fd1f2f36d052d4d116f090fc438aa22dcc862
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94279842"
---
# <span data-ttu-id="f2947-101">Remove-AzDeploymentScript</span><span class="sxs-lookup"><span data-stu-id="f2947-101">Remove-AzDeploymentScript</span></span>

## <span data-ttu-id="f2947-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f2947-102">SYNOPSIS</span></span>
<span data-ttu-id="f2947-103">Dağıtım betiğini ve ilişkili kaynaklarını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="f2947-103">Removes a deployment script and its associated resources.</span></span>


## <span data-ttu-id="f2947-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f2947-104">SYNTAX</span></span>

### <span data-ttu-id="f2947-105">RemoveDeploymentScriptLogByName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="f2947-105">RemoveDeploymentScriptLogByName (Default)</span></span>
```
Remove-AzDeploymentScript [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f2947-106">Removedeploymentscriptlogbyresourceıd</span><span class="sxs-lookup"><span data-stu-id="f2947-106">RemoveDeploymentScriptLogByResourceId</span></span>
```
Remove-AzDeploymentScript [-Id] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f2947-107">RemoveDeploymentScriptLogByInputObject</span><span class="sxs-lookup"><span data-stu-id="f2947-107">RemoveDeploymentScriptLogByInputObject</span></span>
```
Remove-AzDeploymentScript [-InputObject] <PsDeploymentScript> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f2947-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="f2947-108">DESCRIPTION</span></span>
<span data-ttu-id="f2947-109">**Remove-Azdeploymentscrıpt** cmdlet 'i, dağıtım betiğini ve ilişkili kaynaklarını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="f2947-109">The **Remove-AzDeploymentScript** cmdlet removes a deployment script and its associated resources.</span></span>

## <span data-ttu-id="f2947-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f2947-110">EXAMPLES</span></span>

### <span data-ttu-id="f2947-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="f2947-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDeploymentScript -Name MyDeploymentScript -ResourceGroupName DS-TestRg
```

<span data-ttu-id="f2947-112">Kaynak Grup DS-TestRG 'daki Mydeploymentscrıpt adıyla bir dağıtım betiği siler.</span><span class="sxs-lookup"><span data-stu-id="f2947-112">Deletes a deployment script with the name MyDeploymentScript in resource group DS-TestRG.</span></span>

## <span data-ttu-id="f2947-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f2947-113">PARAMETERS</span></span>

### <span data-ttu-id="f2947-114">-Onay</span><span class="sxs-lookup"><span data-stu-id="f2947-114">-Confirm</span></span>
<span data-ttu-id="f2947-115">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f2947-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f2947-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2947-116">-DefaultProfile</span></span>
<span data-ttu-id="f2947-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f2947-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f2947-118">-ID</span><span class="sxs-lookup"><span data-stu-id="f2947-118">-Id</span></span>
<span data-ttu-id="f2947-119">Dağıtım komut dosyasının tam nitelikli kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="f2947-119">The fully qualified resource Id of the deployment script.</span></span>
<span data-ttu-id="f2947-120">Örnek:/subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span><span class="sxs-lookup"><span data-stu-id="f2947-120">Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span></span>

```yaml
Type: String
Parameter Sets: RemoveDeploymentScriptLogByResourceId
Aliases: ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2947-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f2947-121">-InputObject</span></span>
<span data-ttu-id="f2947-122">Dağıtım betiği PowerShell nesnesi.</span><span class="sxs-lookup"><span data-stu-id="f2947-122">The deployment script PowerShell object.</span></span>

```yaml
Type: PsDeploymentScript
Parameter Sets: RemoveDeploymentScriptLogByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f2947-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="f2947-123">-Name</span></span>
<span data-ttu-id="f2947-124">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="f2947-124">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: RemoveDeploymentScriptLogByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2947-125">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="f2947-125">-PassThru</span></span>
<span data-ttu-id="f2947-126">{{Dolgu geçiş açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="f2947-126">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="f2947-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2947-127">-ResourceGroupName</span></span>
<span data-ttu-id="f2947-128">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="f2947-128">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: RemoveDeploymentScriptLogByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2947-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f2947-129">-WhatIf</span></span>
<span data-ttu-id="f2947-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f2947-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f2947-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="f2947-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f2947-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2947-132">CommonParameters</span></span>
<span data-ttu-id="f2947-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f2947-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="f2947-134">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f2947-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2947-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f2947-135">INPUTS</span></span>

### <span data-ttu-id="f2947-136">System. String</span><span class="sxs-lookup"><span data-stu-id="f2947-136">System.String</span></span>

### <span data-ttu-id="f2947-137">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span><span class="sxs-lookup"><span data-stu-id="f2947-137">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span></span>

## <span data-ttu-id="f2947-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f2947-138">OUTPUTS</span></span>

### <span data-ttu-id="f2947-139">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span><span class="sxs-lookup"><span data-stu-id="f2947-139">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span></span>

## <span data-ttu-id="f2947-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f2947-140">NOTES</span></span>

## <span data-ttu-id="f2947-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f2947-141">RELATED LINKS</span></span>