---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 818A048F-7CBE-4845-BBC2-6420CE48199A
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsworkspaceusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspaceUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspaceUsage.md
ms.openlocfilehash: 04a62f4929e89dd4bff4d088d84325b0bdbb140b
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/13/2020
ms.locfileid: "93761932"
---
# <span data-ttu-id="c5d2c-101">Get-AzOperationalInsightsWorkspaceUsage</span><span class="sxs-lookup"><span data-stu-id="c5d2c-101">Get-AzOperationalInsightsWorkspaceUsage</span></span>

## <span data-ttu-id="c5d2c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c5d2c-102">SYNOPSIS</span></span>
<span data-ttu-id="c5d2c-103">Çalışma alanı için kullanım verilerini alır.</span><span class="sxs-lookup"><span data-stu-id="c5d2c-103">Gets the usage data for a workspace.</span></span>

## <span data-ttu-id="c5d2c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c5d2c-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsWorkspaceUsage [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c5d2c-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c5d2c-105">DESCRIPTION</span></span>
<span data-ttu-id="c5d2c-106">**Get-Azoperationalınsightsın**</span><span class="sxs-lookup"><span data-stu-id="c5d2c-106">The **Get-AzOperationalInsightsWorkspaceUsage** cmdlet retrieves the usage data for a workspace.</span></span>
<span data-ttu-id="c5d2c-107">Bu, belirli bir süre içinde çalışma alanı tarafından ne kadar veri Çözümlenmiş olduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="c5d2c-107">This exposes how much data has been analyzed by the workspace over a certain period.</span></span>

## <span data-ttu-id="c5d2c-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c5d2c-108">EXAMPLES</span></span>

### <span data-ttu-id="c5d2c-109">Örnek 1: çalışma alanı adına göre kullanım verilerini alma</span><span class="sxs-lookup"><span data-stu-id="c5d2c-109">Example 1: Get usage data by workspace name</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspaceUsage -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"
```

<span data-ttu-id="c5d2c-110">Bu komut, belirtilen kaynak grubundaki MyWorkspace adındaki çalışma alanının kullanım ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="c5d2c-110">This command gets the usage details for the workspace named MyWorkspace in the specified resource group.</span></span>

### <span data-ttu-id="c5d2c-111">Örnek 2: ardışık düzeni kullanarak kullanım verilerini alma</span><span class="sxs-lookup"><span data-stu-id="c5d2c-111">Example 2: Get usage data using the pipeline</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" | Get-AzOperationalInsightsWorkspaceUsage
```

<span data-ttu-id="c5d2c-112">Bu komut MyWorkSpace adındaki çalışma alanını Get-AzOperationalInsightsWorkspace cmdlet 'ini kullanarak alır ve çalışma alanını geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="c5d2c-112">This command gets the workspace named MyWorkSpace using the Get-AzOperationalInsightsWorkspace cmdlet, and then passes the workspace to the current cmdlet.</span></span>
<span data-ttu-id="c5d2c-113">Komut, bu çalışma alanının kullanım ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="c5d2c-113">The command gets the usage details for that workspace.</span></span>

## <span data-ttu-id="c5d2c-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c5d2c-114">PARAMETERS</span></span>

### <span data-ttu-id="c5d2c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5d2c-115">-DefaultProfile</span></span>
<span data-ttu-id="c5d2c-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="c5d2c-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c5d2c-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="c5d2c-117">-Name</span></span>
<span data-ttu-id="c5d2c-118">Çalışma alanı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c5d2c-118">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="c5d2c-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c5d2c-119">-ResourceGroupName</span></span>
<span data-ttu-id="c5d2c-120">Bir Azure Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c5d2c-120">Specifies the name of an Azure resource group.</span></span>

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

### <span data-ttu-id="c5d2c-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5d2c-121">CommonParameters</span></span>
<span data-ttu-id="c5d2c-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c5d2c-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5d2c-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c5d2c-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5d2c-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c5d2c-124">INPUTS</span></span>

### <span data-ttu-id="c5d2c-125">System. String</span><span class="sxs-lookup"><span data-stu-id="c5d2c-125">System.String</span></span>

## <span data-ttu-id="c5d2c-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c5d2c-126">OUTPUTS</span></span>

### <span data-ttu-id="c5d2c-127">Microsoft. Azure. Commands. Operationalınsights. model. PSUsageMetric</span><span class="sxs-lookup"><span data-stu-id="c5d2c-127">Microsoft.Azure.Commands.OperationalInsights.Models.PSUsageMetric</span></span>

## <span data-ttu-id="c5d2c-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c5d2c-128">NOTES</span></span>

## <span data-ttu-id="c5d2c-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c5d2c-129">RELATED LINKS</span></span>

[<span data-ttu-id="c5d2c-130">Azure Operasyonel Öngörüler cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="c5d2c-130">Azure Operational Insights Cmdlets</span></span>](/powershell/module/az.operationalinsights)

[<span data-ttu-id="c5d2c-131">Get-Azoperationalınsightsworkspace</span><span class="sxs-lookup"><span data-stu-id="c5d2c-131">Get-AzOperationalInsightsWorkspace</span></span>](./Get-AzOperationalInsightsWorkspace.md)

