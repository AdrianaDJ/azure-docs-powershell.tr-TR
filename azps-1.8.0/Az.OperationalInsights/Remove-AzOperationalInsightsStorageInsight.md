---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 92261663-CF50-4EBD-85D2-C2E254F39B41
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/remove-azoperationalinsightsstorageinsight
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsStorageInsight.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsStorageInsight.md
ms.openlocfilehash: b7fbfe720cd63389ced0c1703925e1551ebad40e
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/13/2020
ms.locfileid: "93761926"
---
# <span data-ttu-id="d72da-101">Remove-AzOperationalInsightsStorageInsight</span><span class="sxs-lookup"><span data-stu-id="d72da-101">Remove-AzOperationalInsightsStorageInsight</span></span>

## <span data-ttu-id="d72da-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d72da-102">SYNOPSIS</span></span>
<span data-ttu-id="d72da-103">Depolama Insight.</span><span class="sxs-lookup"><span data-stu-id="d72da-103">Removes a Storage Insight.</span></span>

## <span data-ttu-id="d72da-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d72da-104">SYNTAX</span></span>

### <span data-ttu-id="d72da-105">Byçalışmaalanıadı (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="d72da-105">ByWorkspaceName (Default)</span></span>
```
Remove-AzOperationalInsightsStorageInsight [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d72da-106">Byworkspace nesnesi</span><span class="sxs-lookup"><span data-stu-id="d72da-106">ByWorkspaceObject</span></span>
```
Remove-AzOperationalInsightsStorageInsight [-Workspace] <PSWorkspace> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d72da-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="d72da-107">DESCRIPTION</span></span>
<span data-ttu-id="d72da-108">**Remove-Azoperationalınsightsstorageınsight** cmdlet 'i çalışma alanından bir depolama anlaytöğesini siler.</span><span class="sxs-lookup"><span data-stu-id="d72da-108">The **Remove-AzOperationalInsightsStorageInsight** cmdlet deletes a Storage Insight from a workspace.</span></span>

## <span data-ttu-id="d72da-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d72da-109">EXAMPLES</span></span>

### <span data-ttu-id="d72da-110">Örnek 1: ada göre bir depolama kavramı kaldırma</span><span class="sxs-lookup"><span data-stu-id="d72da-110">Example 1: Remove a Storage Insight by name</span></span>
```
PS C:\>Remove-AzOperationalInsightsStorageInsight -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "MyWorkspace" -Name "MyStorageInsight"
```

<span data-ttu-id="d72da-111">Bu komut Mystorageınsight adındaki depolama anlayış adını belirtilen kaynak grubundaki MyWorkspace adlı çalışma alanından kaldırır.</span><span class="sxs-lookup"><span data-stu-id="d72da-111">This command removes the Storage Insight named MyStorageInsight from the workspace named MyWorkspace in the specified resource group.</span></span>
<span data-ttu-id="d72da-112">Komut Force parametresini belirtmezse, böylece depolama *Anlaytanızı* kaldırmadan önce onaylamanız istenir.</span><span class="sxs-lookup"><span data-stu-id="d72da-112">The command does not specify the *Force* parameter, so it prompts you for confirmation before removing the Storage Insight.</span></span>

### <span data-ttu-id="d72da-113">Örnek 2: bir depolama Anlaytöğesini onaysız kaldırma</span><span class="sxs-lookup"><span data-stu-id="d72da-113">Example 2: Remove a Storage Insight without confirmation</span></span>
```
PS C:\>$Workspace = Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"

PS C:\>Remove-AzOperationalInsightsStorageInsight -Workspace $Workspace -Name "MyStorageInsight" -Force
```

<span data-ttu-id="d72da-114">İlk komut MyWorkspace adlı çalışma alanını almak için Get-AzOperationalInsightsWorkspace cmdlet 'ini kullanır ve $Workspace değişkeninde depolar. İkinci komut, sizden onay istemeden, Mystorage$Workspace Insight adındaki bir depolama anlaytisini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="d72da-114">The first command uses the Get-AzOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkspace, and then stores it in the $Workspace variable.The second command removes the storage insight named MyStorageInsight from $Workspace without prompting you for confirmation.</span></span>

## <span data-ttu-id="d72da-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d72da-115">PARAMETERS</span></span>

### <span data-ttu-id="d72da-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d72da-116">-DefaultProfile</span></span>
<span data-ttu-id="d72da-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="d72da-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d72da-118">-Force</span><span class="sxs-lookup"><span data-stu-id="d72da-118">-Force</span></span>
<span data-ttu-id="d72da-119">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="d72da-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d72da-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="d72da-120">-Name</span></span>
<span data-ttu-id="d72da-121">Depolama anlayış adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d72da-121">Specifies the name of the Storage Insight.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d72da-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d72da-122">-ResourceGroupName</span></span>
<span data-ttu-id="d72da-123">Bir Azure Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d72da-123">Specifies the name of an Azure resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d72da-124">-Çalışma alanı</span><span class="sxs-lookup"><span data-stu-id="d72da-124">-Workspace</span></span>
<span data-ttu-id="d72da-125">Depolama kavramı içeren çalışma alanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d72da-125">Specifies the workspace that contains the Storage Insight.</span></span>

```yaml
Type: Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace
Parameter Sets: ByWorkspaceObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d72da-126">-Çalışmaalanıadı</span><span class="sxs-lookup"><span data-stu-id="d72da-126">-WorkspaceName</span></span>
<span data-ttu-id="d72da-127">Depolama kavramı içeren çalışma alanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d72da-127">Specifies the name of the workspace that contains the Storage Insight.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d72da-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="d72da-128">-Confirm</span></span>
<span data-ttu-id="d72da-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d72da-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d72da-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d72da-130">-WhatIf</span></span>
<span data-ttu-id="d72da-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d72da-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d72da-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d72da-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d72da-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d72da-133">CommonParameters</span></span>
<span data-ttu-id="d72da-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d72da-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d72da-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d72da-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d72da-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d72da-136">INPUTS</span></span>

### <span data-ttu-id="d72da-137">Microsoft. Azure. Commands. Operationalınsights. model. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="d72da-137">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="d72da-138">System. String</span><span class="sxs-lookup"><span data-stu-id="d72da-138">System.String</span></span>

## <span data-ttu-id="d72da-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d72da-139">OUTPUTS</span></span>

### <span data-ttu-id="d72da-140">System. void</span><span class="sxs-lookup"><span data-stu-id="d72da-140">System.Void</span></span>

## <span data-ttu-id="d72da-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d72da-141">NOTES</span></span>

## <span data-ttu-id="d72da-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d72da-142">RELATED LINKS</span></span>

[<span data-ttu-id="d72da-143">Azure Operasyonel Öngörüler cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="d72da-143">Azure Operational Insights Cmdlets</span></span>](/powershell/module/az.operationalinsights)

[<span data-ttu-id="d72da-144">Get-Azoperationalınsightsworkspace</span><span class="sxs-lookup"><span data-stu-id="d72da-144">Get-AzOperationalInsightsWorkspace</span></span>](./Get-AzOperationalInsightsWorkspace.md)


