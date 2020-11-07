---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 818A048F-7CBE-4845-BBC2-6420CE48199A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/get-azurermoperationalinsightsworkspaceusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsWorkspaceUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsWorkspaceUsage.md
ms.openlocfilehash: fa238d963f472e79946632311a9f93c8586650ba
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594843"
---
# <span data-ttu-id="6ad0d-101">Get-AzureRmOperationalInsightsWorkspaceUsage</span><span class="sxs-lookup"><span data-stu-id="6ad0d-101">Get-AzureRmOperationalInsightsWorkspaceUsage</span></span>

## <span data-ttu-id="6ad0d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6ad0d-102">SYNOPSIS</span></span>
<span data-ttu-id="6ad0d-103">Çalışma alanı için kullanım verilerini alır.</span><span class="sxs-lookup"><span data-stu-id="6ad0d-103">Gets the usage data for a workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6ad0d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6ad0d-104">SYNTAX</span></span>

```
Get-AzureRmOperationalInsightsWorkspaceUsage [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6ad0d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="6ad0d-105">DESCRIPTION</span></span>
<span data-ttu-id="6ad0d-106">**Get-Azurermoperationalınsightse**</span><span class="sxs-lookup"><span data-stu-id="6ad0d-106">The **Get-AzureRmOperationalInsightsWorkspaceUsage** cmdlet retrieves the usage data for a workspace.</span></span>
<span data-ttu-id="6ad0d-107">Bu, belirli bir süre içinde çalışma alanı tarafından ne kadar veri Çözümlenmiş olduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="6ad0d-107">This exposes how much data has been analyzed by the workspace over a certain period.</span></span>

## <span data-ttu-id="6ad0d-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6ad0d-108">EXAMPLES</span></span>

### <span data-ttu-id="6ad0d-109">Örnek 1: çalışma alanı adına göre kullanım verilerini alma</span><span class="sxs-lookup"><span data-stu-id="6ad0d-109">Example 1: Get usage data by workspace name</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsWorkspaceUsage -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"
```

<span data-ttu-id="6ad0d-110">Bu komut, belirtilen kaynak grubundaki MyWorkspace adındaki çalışma alanının kullanım ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="6ad0d-110">This command gets the usage details for the workspace named MyWorkspace in the specified resource group.</span></span>

### <span data-ttu-id="6ad0d-111">Örnek 2: ardışık düzeni kullanarak kullanım verilerini alma</span><span class="sxs-lookup"><span data-stu-id="6ad0d-111">Example 2: Get usage data using the pipeline</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" | Get-AzureOperationalInsightsWorkspaceUsage
```

<span data-ttu-id="6ad0d-112">Bu komut MyWorkSpace adındaki çalışma alanını Get-AzureRmOperationalInsightsWorkspace cmdlet 'ini kullanarak alır ve çalışma alanını geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="6ad0d-112">This command gets the workspace named MyWorkSpace using the Get-AzureRmOperationalInsightsWorkspace cmdlet, and then passes the workspace to the current cmdlet.</span></span>
<span data-ttu-id="6ad0d-113">Komut, bu çalışma alanının kullanım ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="6ad0d-113">The command gets the usage details for that workspace.</span></span>

## <span data-ttu-id="6ad0d-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6ad0d-114">PARAMETERS</span></span>

### <span data-ttu-id="6ad0d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ad0d-115">-DefaultProfile</span></span>
<span data-ttu-id="6ad0d-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="6ad0d-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6ad0d-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="6ad0d-117">-Name</span></span>
<span data-ttu-id="6ad0d-118">Çalışma alanı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6ad0d-118">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="6ad0d-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ad0d-119">-ResourceGroupName</span></span>
<span data-ttu-id="6ad0d-120">Bir Azure Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6ad0d-120">Specifies the name of an Azure resource group.</span></span>

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

### <span data-ttu-id="6ad0d-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ad0d-121">CommonParameters</span></span>
<span data-ttu-id="6ad0d-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6ad0d-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ad0d-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6ad0d-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ad0d-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6ad0d-124">INPUTS</span></span>

### <span data-ttu-id="6ad0d-125">System. String</span><span class="sxs-lookup"><span data-stu-id="6ad0d-125">System.String</span></span>

## <span data-ttu-id="6ad0d-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6ad0d-126">OUTPUTS</span></span>

### <span data-ttu-id="6ad0d-127">Microsoft. Azure. Commands. Operationalınsights. model. PSUsageMetric</span><span class="sxs-lookup"><span data-stu-id="6ad0d-127">Microsoft.Azure.Commands.OperationalInsights.Models.PSUsageMetric</span></span>

## <span data-ttu-id="6ad0d-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6ad0d-128">NOTES</span></span>

## <span data-ttu-id="6ad0d-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6ad0d-129">RELATED LINKS</span></span>

[<span data-ttu-id="6ad0d-130">Azure Operasyonel Öngörüler cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="6ad0d-130">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)

[<span data-ttu-id="6ad0d-131">Get-Azurermoperationalınsightsworkspace</span><span class="sxs-lookup"><span data-stu-id="6ad0d-131">Get-AzureRmOperationalInsightsWorkspace</span></span>](./Get-AzureRmOperationalInsightsWorkspace.md)

