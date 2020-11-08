---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 92261663-CF50-4EBD-85D2-C2E254F39B41
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/remove-azoperationalinsightsstorageinsight
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsStorageInsight.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsStorageInsight.md
ms.openlocfilehash: ac9e061fea8c6d7737eb268feec225dff0b0924d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94265849"
---
# <span data-ttu-id="ddb67-101">Remove-AzOperationalInsightsStorageInsight</span><span class="sxs-lookup"><span data-stu-id="ddb67-101">Remove-AzOperationalInsightsStorageInsight</span></span>

## <span data-ttu-id="ddb67-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ddb67-102">SYNOPSIS</span></span>
<span data-ttu-id="ddb67-103">Depolama Insight.</span><span class="sxs-lookup"><span data-stu-id="ddb67-103">Removes a Storage Insight.</span></span>

## <span data-ttu-id="ddb67-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ddb67-104">SYNTAX</span></span>

### <span data-ttu-id="ddb67-105">Byçalışmaalanıadı (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="ddb67-105">ByWorkspaceName (Default)</span></span>
```
Remove-AzOperationalInsightsStorageInsight [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ddb67-106">Byworkspace nesnesi</span><span class="sxs-lookup"><span data-stu-id="ddb67-106">ByWorkspaceObject</span></span>
```
Remove-AzOperationalInsightsStorageInsight [-Workspace] <PSWorkspace> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ddb67-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="ddb67-107">DESCRIPTION</span></span>
<span data-ttu-id="ddb67-108">**Remove-Azoperationalınsightsstorageınsight** cmdlet 'i çalışma alanından bir depolama anlaytöğesini siler.</span><span class="sxs-lookup"><span data-stu-id="ddb67-108">The **Remove-AzOperationalInsightsStorageInsight** cmdlet deletes a Storage Insight from a workspace.</span></span>

## <span data-ttu-id="ddb67-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ddb67-109">EXAMPLES</span></span>

### <span data-ttu-id="ddb67-110">Örnek 1: ada göre bir depolama kavramı kaldırma</span><span class="sxs-lookup"><span data-stu-id="ddb67-110">Example 1: Remove a Storage Insight by name</span></span>
```
PS C:\>Remove-AzOperationalInsightsStorageInsight -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "MyWorkspace" -Name "MyStorageInsight"
```

<span data-ttu-id="ddb67-111">Bu komut Mystorageınsight adındaki depolama anlayış adını belirtilen kaynak grubundaki MyWorkspace adlı çalışma alanından kaldırır.</span><span class="sxs-lookup"><span data-stu-id="ddb67-111">This command removes the Storage Insight named MyStorageInsight from the workspace named MyWorkspace in the specified resource group.</span></span>
<span data-ttu-id="ddb67-112">Komut Force parametresini belirtmezse, böylece depolama *Anlaytanızı* kaldırmadan önce onaylamanız istenir.</span><span class="sxs-lookup"><span data-stu-id="ddb67-112">The command does not specify the *Force* parameter, so it prompts you for confirmation before removing the Storage Insight.</span></span>

### <span data-ttu-id="ddb67-113">Örnek 2: bir depolama Anlaytöğesini onaysız kaldırma</span><span class="sxs-lookup"><span data-stu-id="ddb67-113">Example 2: Remove a Storage Insight without confirmation</span></span>
```
PS C:\>$Workspace = Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"

PS C:\>Remove-AzOperationalInsightsStorageInsight -Workspace $Workspace -Name "MyStorageInsight" -Force
```

<span data-ttu-id="ddb67-114">İlk komut MyWorkspace adlı çalışma alanını almak için Get-AzOperationalInsightsWorkspace cmdlet 'ini kullanır ve $Workspace değişkeninde depolar. İkinci komut, sizden onay istemeden, Mystorage$Workspace Insight adındaki bir depolama anlaytisini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="ddb67-114">The first command uses the Get-AzOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkspace, and then stores it in the $Workspace variable.The second command removes the storage insight named MyStorageInsight from $Workspace without prompting you for confirmation.</span></span>

## <span data-ttu-id="ddb67-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ddb67-115">PARAMETERS</span></span>

### <span data-ttu-id="ddb67-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ddb67-116">-DefaultProfile</span></span>
<span data-ttu-id="ddb67-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="ddb67-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ddb67-118">-Force</span><span class="sxs-lookup"><span data-stu-id="ddb67-118">-Force</span></span>
<span data-ttu-id="ddb67-119">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="ddb67-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ddb67-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="ddb67-120">-Name</span></span>
<span data-ttu-id="ddb67-121">Depolama anlayış adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ddb67-121">Specifies the name of the Storage Insight.</span></span>

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

### <span data-ttu-id="ddb67-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ddb67-122">-ResourceGroupName</span></span>
<span data-ttu-id="ddb67-123">Bir Azure Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ddb67-123">Specifies the name of an Azure resource group.</span></span>

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

### <span data-ttu-id="ddb67-124">-Çalışma alanı</span><span class="sxs-lookup"><span data-stu-id="ddb67-124">-Workspace</span></span>
<span data-ttu-id="ddb67-125">Depolama kavramı içeren çalışma alanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ddb67-125">Specifies the workspace that contains the Storage Insight.</span></span>

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

### <span data-ttu-id="ddb67-126">-Çalışmaalanıadı</span><span class="sxs-lookup"><span data-stu-id="ddb67-126">-WorkspaceName</span></span>
<span data-ttu-id="ddb67-127">Depolama kavramı içeren çalışma alanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ddb67-127">Specifies the name of the workspace that contains the Storage Insight.</span></span>

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

### <span data-ttu-id="ddb67-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="ddb67-128">-Confirm</span></span>
<span data-ttu-id="ddb67-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ddb67-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ddb67-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ddb67-130">-WhatIf</span></span>
<span data-ttu-id="ddb67-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ddb67-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ddb67-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ddb67-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ddb67-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ddb67-133">CommonParameters</span></span>
<span data-ttu-id="ddb67-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ddb67-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ddb67-135">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ddb67-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ddb67-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ddb67-136">INPUTS</span></span>

### <span data-ttu-id="ddb67-137">Microsoft. Azure. Commands. Operationalınsights. model. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="ddb67-137">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="ddb67-138">System. String</span><span class="sxs-lookup"><span data-stu-id="ddb67-138">System.String</span></span>

## <span data-ttu-id="ddb67-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ddb67-139">OUTPUTS</span></span>

### <span data-ttu-id="ddb67-140">System. void</span><span class="sxs-lookup"><span data-stu-id="ddb67-140">System.Void</span></span>

## <span data-ttu-id="ddb67-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ddb67-141">NOTES</span></span>

## <span data-ttu-id="ddb67-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ddb67-142">RELATED LINKS</span></span>

[<span data-ttu-id="ddb67-143">Azure Operasyonel Öngörüler cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="ddb67-143">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)

[<span data-ttu-id="ddb67-144">Get-Azoperationalınsightsworkspace</span><span class="sxs-lookup"><span data-stu-id="ddb67-144">Get-AzOperationalInsightsWorkspace</span></span>](./Get-AzOperationalInsightsWorkspace.md)


