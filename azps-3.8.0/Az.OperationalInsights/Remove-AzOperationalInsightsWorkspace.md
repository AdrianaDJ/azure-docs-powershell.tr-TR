---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 0C35E679-B991-49A8-890F-C8DAB68A8240
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/remove-azoperationalinsightsworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsWorkspace.md
ms.openlocfilehash: ac3cda3e6c83106ac299dbd57cba81001f644305
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/13/2020
ms.locfileid: "94107286"
---
# <span data-ttu-id="c0d2e-101">Remove-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="c0d2e-101">Remove-AzOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="c0d2e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c0d2e-102">SYNOPSIS</span></span>
<span data-ttu-id="c0d2e-103">Çalışma alanını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="c0d2e-103">Removes a workspace.</span></span>

## <span data-ttu-id="c0d2e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c0d2e-104">SYNTAX</span></span>

```
Remove-AzOperationalInsightsWorkspace [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c0d2e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c0d2e-105">DESCRIPTION</span></span>
<span data-ttu-id="c0d2e-106">**Remove-Azoperationalınsightsworkspace** cmdlet 'i var olan bir çalışma alanını siler.</span><span class="sxs-lookup"><span data-stu-id="c0d2e-106">The **Remove-AzOperationalInsightsWorkspace** cmdlet deletes an existing workspace.</span></span>
<span data-ttu-id="c0d2e-107">Bu çalışma alanı, oluşturma sırasında *MüşteriNo* parametresi aracılığıyla varolan bir hesaba bağlanmışsa, çalışma</span><span class="sxs-lookup"><span data-stu-id="c0d2e-107">If this workspace was linked to an existing account via the *CustomerId* parameter at creation time the original account is not deleted in the Operational Insights portal.</span></span>

## <span data-ttu-id="c0d2e-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c0d2e-108">EXAMPLES</span></span>

### <span data-ttu-id="c0d2e-109">Örnek 1: çalışma alanını adla kaldırma</span><span class="sxs-lookup"><span data-stu-id="c0d2e-109">Example 1: Remove a workspace by name</span></span>
```
PS C:\>Remove-AzOperationalInsightsWorkspace -ResourceGroupName "ContosResourceGroup" -Name "MyWorkspace"
```

<span data-ttu-id="c0d2e-110">Bu komut MyWorkspace adlı çalışma alanını ContosoResourceGroup adlı kaynak grubundan kaldırır.</span><span class="sxs-lookup"><span data-stu-id="c0d2e-110">This command removes the workspace named MyWorkspace from the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="c0d2e-111">Örnek 2: ardışık düzeni kullanarak bir çalışma alanını kaldırma</span><span class="sxs-lookup"><span data-stu-id="c0d2e-111">Example 2: Remove a workspace by using the pipeline and without confirmation</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosResourceGroup" -Name "MyWorkspace" | Remove-AzOperationalInsightsWorkspace -Force
```

<span data-ttu-id="c0d2e-112">Bu komut MyWorkspace adlı çalışma alanını almak için Get-AzOperationalInsightsWorkspace cmdlet 'ini kullanır ve bunu kaldırmak için ardışık düzen işlecini kullanarak Remove **-Azoperationalınsightsworkspace** cmdlet 'ine geçirir.</span><span class="sxs-lookup"><span data-stu-id="c0d2e-112">This command uses the Get-AzOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkspace, and then passes it to the **Remove-AzOperationalInsightsWorkspace** cmdlet by using the pipeline operator to remove it.</span></span>
<span data-ttu-id="c0d2e-113">*Force* parametresi belirtildiğinden, komut çalışma alanını kaldırmadan önce sizi istemez.</span><span class="sxs-lookup"><span data-stu-id="c0d2e-113">Since the *Force* parameter is specified, the command does not prompt you before removing the workspace.</span></span>

## <span data-ttu-id="c0d2e-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c0d2e-114">PARAMETERS</span></span>

### <span data-ttu-id="c0d2e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0d2e-115">-DefaultProfile</span></span>
<span data-ttu-id="c0d2e-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="c0d2e-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c0d2e-117">-Force</span><span class="sxs-lookup"><span data-stu-id="c0d2e-117">-Force</span></span>
<span data-ttu-id="c0d2e-118">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="c0d2e-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c0d2e-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="c0d2e-119">-Name</span></span>
<span data-ttu-id="c0d2e-120">Çalışma alanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c0d2e-120">Specifies the name of the workspace.</span></span>

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

### <span data-ttu-id="c0d2e-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0d2e-121">-ResourceGroupName</span></span>
<span data-ttu-id="c0d2e-122">Bir Azure Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c0d2e-122">Specifies the name of an Azure resource group.</span></span>

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

### <span data-ttu-id="c0d2e-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="c0d2e-123">-Confirm</span></span>
<span data-ttu-id="c0d2e-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c0d2e-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c0d2e-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0d2e-125">-WhatIf</span></span>
<span data-ttu-id="c0d2e-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c0d2e-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c0d2e-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="c0d2e-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c0d2e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0d2e-128">CommonParameters</span></span>
<span data-ttu-id="c0d2e-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c0d2e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0d2e-130">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c0d2e-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0d2e-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c0d2e-131">INPUTS</span></span>

### <span data-ttu-id="c0d2e-132">System. String</span><span class="sxs-lookup"><span data-stu-id="c0d2e-132">System.String</span></span>

## <span data-ttu-id="c0d2e-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c0d2e-133">OUTPUTS</span></span>

### <span data-ttu-id="c0d2e-134">System. void</span><span class="sxs-lookup"><span data-stu-id="c0d2e-134">System.Void</span></span>

## <span data-ttu-id="c0d2e-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c0d2e-135">NOTES</span></span>

## <span data-ttu-id="c0d2e-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c0d2e-136">RELATED LINKS</span></span>

[<span data-ttu-id="c0d2e-137">Azure Operasyonel Öngörüler cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="c0d2e-137">Azure Operational Insights Cmdlets</span></span>](/powershell/module/az.operationalinsights)

[<span data-ttu-id="c0d2e-138">Get-Azoperationalınsightsworkspace</span><span class="sxs-lookup"><span data-stu-id="c0d2e-138">Get-AzOperationalInsightsWorkspace</span></span>](./Get-AzOperationalInsightsWorkspace.md)


