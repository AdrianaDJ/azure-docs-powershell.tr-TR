---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 0C35E679-B991-49A8-890F-C8DAB68A8240
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/remove-azoperationalinsightsworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsWorkspace.md
ms.openlocfilehash: d02338c34584a68ece2ad3a90887a765f8142347
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94109413"
---
# <span data-ttu-id="fd010-101">Remove-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="fd010-101">Remove-AzOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="fd010-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fd010-102">SYNOPSIS</span></span>
<span data-ttu-id="fd010-103">Çalışma alanını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="fd010-103">Removes a workspace.</span></span>

## <span data-ttu-id="fd010-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fd010-104">SYNTAX</span></span>

```
Remove-AzOperationalInsightsWorkspace [-ResourceGroupName] <String> [-Name] <String> [-ForceDelete] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fd010-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="fd010-105">DESCRIPTION</span></span>
<span data-ttu-id="fd010-106">**Remove-Azoperationalınsightsworkspace** cmdlet 'i var olan bir çalışma alanını siler.</span><span class="sxs-lookup"><span data-stu-id="fd010-106">The **Remove-AzOperationalInsightsWorkspace** cmdlet deletes an existing workspace.</span></span>
<span data-ttu-id="fd010-107">Bu çalışma alanı, oluşturma sırasında *MüşteriNo* parametresi aracılığıyla varolan bir hesaba bağlanmışsa, çalışma</span><span class="sxs-lookup"><span data-stu-id="fd010-107">If this workspace was linked to an existing account via the *CustomerId* parameter at creation time the original account is not deleted in the Operational Insights portal.</span></span>

## <span data-ttu-id="fd010-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fd010-108">EXAMPLES</span></span>

### <span data-ttu-id="fd010-109">Örnek 1: çalışma alanını adla kaldırma</span><span class="sxs-lookup"><span data-stu-id="fd010-109">Example 1: Remove a workspace by name</span></span>
```
PS C:\>Remove-AzOperationalInsightsWorkspace -ResourceGroupName "ContosResourceGroup" -Name "MyWorkspace"
```

<span data-ttu-id="fd010-110">Bu komut MyWorkspace adlı çalışma alanını ContosoResourceGroup adlı kaynak grubundan kaldırır.</span><span class="sxs-lookup"><span data-stu-id="fd010-110">This command removes the workspace named MyWorkspace from the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="fd010-111">Örnek 2: ardışık düzeni kullanarak bir çalışma alanını kaldırma</span><span class="sxs-lookup"><span data-stu-id="fd010-111">Example 2: Remove a workspace by using the pipeline and without confirmation</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosResourceGroup" -Name "MyWorkspace" | Remove-AzOperationalInsightsWorkspace -Force
```

<span data-ttu-id="fd010-112">Bu komut MyWorkspace adlı çalışma alanını almak için Get-AzOperationalInsightsWorkspace cmdlet 'ini kullanır ve bunu kaldırmak için ardışık düzen işlecini kullanarak Remove **-Azoperationalınsightsworkspace** cmdlet 'ine geçirir.</span><span class="sxs-lookup"><span data-stu-id="fd010-112">This command uses the Get-AzOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkspace, and then passes it to the **Remove-AzOperationalInsightsWorkspace** cmdlet by using the pipeline operator to remove it.</span></span>
<span data-ttu-id="fd010-113">*Force* parametresi belirtildiğinden, komut çalışma alanını kaldırmadan önce sizi istemez.</span><span class="sxs-lookup"><span data-stu-id="fd010-113">Since the *Force* parameter is specified, the command does not prompt you before removing the workspace.</span></span>

### <span data-ttu-id="fd010-114">Örnek 3: çalışma alanını silmeye zorla (kurtarılamaz)</span><span class="sxs-lookup"><span data-stu-id="fd010-114">Example 3: Force delete workspace (cannot be recovered)</span></span>
```
PS C:\> $workspace = New-AzOperationalInsightsWorkspace -ResourceGroupName $rgname -Name $wsname -Location $wslocation
PS C:\> $workspace | Remove-AzOperationalInsightsWorkspace -ForceDelete
```

<span data-ttu-id="fd010-115">Çalışma alanını silmeye zorla.</span><span class="sxs-lookup"><span data-stu-id="fd010-115">Force delete a workspace.</span></span>

## <span data-ttu-id="fd010-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fd010-116">PARAMETERS</span></span>

### <span data-ttu-id="fd010-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd010-117">-DefaultProfile</span></span>
<span data-ttu-id="fd010-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="fd010-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fd010-119">-Force</span><span class="sxs-lookup"><span data-stu-id="fd010-119">-Force</span></span>
<span data-ttu-id="fd010-120">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="fd010-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="fd010-121">-ForceDelete</span><span class="sxs-lookup"><span data-stu-id="fd010-121">-ForceDelete</span></span>
<span data-ttu-id="fd010-122">Çalışma alanını silmeye zorla.</span><span class="sxs-lookup"><span data-stu-id="fd010-122">Force delete workspace.</span></span>

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

### <span data-ttu-id="fd010-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="fd010-123">-Name</span></span>
<span data-ttu-id="fd010-124">Çalışma alanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fd010-124">Specifies the name of the workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd010-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd010-125">-ResourceGroupName</span></span>
<span data-ttu-id="fd010-126">Bir Azure Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fd010-126">Specifies the name of an Azure resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd010-127">-Onay</span><span class="sxs-lookup"><span data-stu-id="fd010-127">-Confirm</span></span>
<span data-ttu-id="fd010-128">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="fd010-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fd010-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd010-129">-WhatIf</span></span>
<span data-ttu-id="fd010-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="fd010-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fd010-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="fd010-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fd010-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd010-132">CommonParameters</span></span>
<span data-ttu-id="fd010-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fd010-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd010-134">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="fd010-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd010-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fd010-135">INPUTS</span></span>

### <span data-ttu-id="fd010-136">System. String</span><span class="sxs-lookup"><span data-stu-id="fd010-136">System.String</span></span>

## <span data-ttu-id="fd010-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fd010-137">OUTPUTS</span></span>

### <span data-ttu-id="fd010-138">System. void</span><span class="sxs-lookup"><span data-stu-id="fd010-138">System.Void</span></span>

## <span data-ttu-id="fd010-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fd010-139">NOTES</span></span>

## <span data-ttu-id="fd010-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fd010-140">RELATED LINKS</span></span>

[<span data-ttu-id="fd010-141">Azure Operasyonel Öngörüler cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="fd010-141">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)

[<span data-ttu-id="fd010-142">Get-Azoperationalınsightsworkspace</span><span class="sxs-lookup"><span data-stu-id="fd010-142">Get-AzOperationalInsightsWorkspace</span></span>](./Get-AzOperationalInsightsWorkspace.md)


