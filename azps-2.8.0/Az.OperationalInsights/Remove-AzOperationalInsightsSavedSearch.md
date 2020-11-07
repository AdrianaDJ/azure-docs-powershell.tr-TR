---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: D4A40E83-2969-40A2-AED0-A6073142CAF1
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/remove-azoperationalinsightssavedsearch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsSavedSearch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsSavedSearch.md
ms.openlocfilehash: 404624f85dcf5647055ced9cd4ad55b373215c7d
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/13/2020
ms.locfileid: "93938737"
---
# <span data-ttu-id="b3bee-101">Remove-AzOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="b3bee-101">Remove-AzOperationalInsightsSavedSearch</span></span>

## <span data-ttu-id="b3bee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b3bee-102">SYNOPSIS</span></span>
<span data-ttu-id="b3bee-103">Kaydedilmiş bir aramayı çalışma alanından kaldırır.</span><span class="sxs-lookup"><span data-stu-id="b3bee-103">Removes a saved search from the workspace.</span></span>

## <span data-ttu-id="b3bee-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b3bee-104">SYNTAX</span></span>

```
Remove-AzOperationalInsightsSavedSearch [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b3bee-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b3bee-105">DESCRIPTION</span></span>
<span data-ttu-id="b3bee-106">**Remove-Azoperationalınsightssavedsearch** cmdlet 'i, kaydedilmiş bir aramayı çalışma alanından kaldırır.</span><span class="sxs-lookup"><span data-stu-id="b3bee-106">The **Remove-AzOperationalInsightsSavedSearch** cmdlet removes a saved search from the workspace.</span></span>

## <span data-ttu-id="b3bee-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b3bee-107">EXAMPLES</span></span>

### <span data-ttu-id="b3bee-108">Örnek 1: kaydedilen aramayı kaldırma</span><span class="sxs-lookup"><span data-stu-id="b3bee-108">Example 1: Remove a saved search</span></span>
```
PS C:\>Remove-AzOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId" -Force
```

<span data-ttu-id="b3bee-109">Bu komut, kaydedilmiş bir aramayı çalışma alanından kaldırır.</span><span class="sxs-lookup"><span data-stu-id="b3bee-109">This command removes a saved search from the workspace.</span></span>

## <span data-ttu-id="b3bee-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b3bee-110">PARAMETERS</span></span>

### <span data-ttu-id="b3bee-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3bee-111">-DefaultProfile</span></span>
<span data-ttu-id="b3bee-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="b3bee-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b3bee-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3bee-113">-ResourceGroupName</span></span>
<span data-ttu-id="b3bee-114">Çalışma alanı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b3bee-114">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="b3bee-115">-Savedsearchıd</span><span class="sxs-lookup"><span data-stu-id="b3bee-115">-SavedSearchId</span></span>
<span data-ttu-id="b3bee-116">Kayıtlı arama KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="b3bee-116">Specifies the saved search ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3bee-117">-Çalışmaalanıadı</span><span class="sxs-lookup"><span data-stu-id="b3bee-117">-WorkspaceName</span></span>
<span data-ttu-id="b3bee-118">Çalışma alanı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b3bee-118">Specifies the workspace name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3bee-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="b3bee-119">-Confirm</span></span>
<span data-ttu-id="b3bee-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b3bee-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b3bee-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b3bee-121">-WhatIf</span></span>
<span data-ttu-id="b3bee-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b3bee-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b3bee-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b3bee-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b3bee-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3bee-124">CommonParameters</span></span>
<span data-ttu-id="b3bee-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b3bee-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3bee-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b3bee-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3bee-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b3bee-127">INPUTS</span></span>

### <span data-ttu-id="b3bee-128">System. String</span><span class="sxs-lookup"><span data-stu-id="b3bee-128">System.String</span></span>

## <span data-ttu-id="b3bee-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b3bee-129">OUTPUTS</span></span>

### <span data-ttu-id="b3bee-130">System. void</span><span class="sxs-lookup"><span data-stu-id="b3bee-130">System.Void</span></span>

## <span data-ttu-id="b3bee-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b3bee-131">NOTES</span></span>

## <span data-ttu-id="b3bee-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b3bee-132">RELATED LINKS</span></span>

[<span data-ttu-id="b3bee-133">Azure Operasyonel Öngörüler cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="b3bee-133">Azure Operational Insights Cmdlets</span></span>](/powershell/module/az.operationalinsights)


