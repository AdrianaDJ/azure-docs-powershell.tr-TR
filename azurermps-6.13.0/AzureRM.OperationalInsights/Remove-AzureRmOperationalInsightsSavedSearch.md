---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: D4A40E83-2969-40A2-AED0-A6073142CAF1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/remove-azurermoperationalinsightssavedsearch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Remove-AzureRmOperationalInsightsSavedSearch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Remove-AzureRmOperationalInsightsSavedSearch.md
ms.openlocfilehash: a438a84a25e100539f485b5d3a7012f03ee355a1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591305"
---
# <span data-ttu-id="6f22a-101">Remove-AzureRmOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="6f22a-101">Remove-AzureRmOperationalInsightsSavedSearch</span></span>

## <span data-ttu-id="6f22a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6f22a-102">SYNOPSIS</span></span>
<span data-ttu-id="6f22a-103">Kaydedilmiş bir aramayı çalışma alanından kaldırır.</span><span class="sxs-lookup"><span data-stu-id="6f22a-103">Removes a saved search from the workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6f22a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6f22a-104">SYNTAX</span></span>

```
Remove-AzureRmOperationalInsightsSavedSearch [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6f22a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="6f22a-105">DESCRIPTION</span></span>
<span data-ttu-id="6f22a-106">**Remove-Azurermoperationalınsightssavedsearch** cmdlet 'i, kaydedilmiş bir aramayı çalışma alanından kaldırır.</span><span class="sxs-lookup"><span data-stu-id="6f22a-106">The **Remove-AzureRmOperationalInsightsSavedSearch** cmdlet removes a saved search from the workspace.</span></span>

## <span data-ttu-id="6f22a-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6f22a-107">EXAMPLES</span></span>

### <span data-ttu-id="6f22a-108">Örnek 1: kaydedilen aramayı kaldırma</span><span class="sxs-lookup"><span data-stu-id="6f22a-108">Example 1: Remove a saved search</span></span>
```
PS C:\>Remove-AzureRmOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId" -Force
```

<span data-ttu-id="6f22a-109">Bu komut, kaydedilmiş bir aramayı çalışma alanından kaldırır.</span><span class="sxs-lookup"><span data-stu-id="6f22a-109">This command removes a saved search from the workspace.</span></span>

## <span data-ttu-id="6f22a-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6f22a-110">PARAMETERS</span></span>

### <span data-ttu-id="6f22a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f22a-111">-DefaultProfile</span></span>
<span data-ttu-id="6f22a-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="6f22a-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6f22a-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6f22a-113">-ResourceGroupName</span></span>
<span data-ttu-id="6f22a-114">Çalışma alanı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6f22a-114">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="6f22a-115">-Savedsearchıd</span><span class="sxs-lookup"><span data-stu-id="6f22a-115">-SavedSearchId</span></span>
<span data-ttu-id="6f22a-116">Kayıtlı arama KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="6f22a-116">Specifies the saved search ID.</span></span>

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

### <span data-ttu-id="6f22a-117">-Çalışmaalanıadı</span><span class="sxs-lookup"><span data-stu-id="6f22a-117">-WorkspaceName</span></span>
<span data-ttu-id="6f22a-118">Çalışma alanı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6f22a-118">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="6f22a-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="6f22a-119">-Confirm</span></span>
<span data-ttu-id="6f22a-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="6f22a-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6f22a-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6f22a-121">-WhatIf</span></span>
<span data-ttu-id="6f22a-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6f22a-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6f22a-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="6f22a-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6f22a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f22a-124">CommonParameters</span></span>
<span data-ttu-id="6f22a-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6f22a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f22a-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6f22a-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f22a-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6f22a-127">INPUTS</span></span>

### <span data-ttu-id="6f22a-128">System. String</span><span class="sxs-lookup"><span data-stu-id="6f22a-128">System.String</span></span>

## <span data-ttu-id="6f22a-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6f22a-129">OUTPUTS</span></span>

### <span data-ttu-id="6f22a-130">System. void</span><span class="sxs-lookup"><span data-stu-id="6f22a-130">System.Void</span></span>

## <span data-ttu-id="6f22a-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6f22a-131">NOTES</span></span>

## <span data-ttu-id="6f22a-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6f22a-132">RELATED LINKS</span></span>

[<span data-ttu-id="6f22a-133">Azure Operasyonel Öngörüler cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="6f22a-133">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)


