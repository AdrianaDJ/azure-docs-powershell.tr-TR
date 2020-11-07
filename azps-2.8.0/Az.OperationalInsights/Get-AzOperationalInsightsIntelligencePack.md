---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 0F9D72C1-2E42-4A67-9FDE-6344F5DE6C30
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsintelligencepack
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsIntelligencePack.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsIntelligencePack.md
ms.openlocfilehash: fa4df1d2b2149a0bc9c637ffefd5c60e52fa0059
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/13/2020
ms.locfileid: "93938613"
---
# <span data-ttu-id="9450d-101">Get-AzOperationalInsightsIntelligencePack</span><span class="sxs-lookup"><span data-stu-id="9450d-101">Get-AzOperationalInsightsIntelligencePack</span></span>

## <span data-ttu-id="9450d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9450d-102">SYNOPSIS</span></span>
<span data-ttu-id="9450d-103">Kullanılabilir yönetim bilgileri paketini alır.</span><span class="sxs-lookup"><span data-stu-id="9450d-103">Gets the available Intelligence Packs.</span></span>

## <span data-ttu-id="9450d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9450d-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsIntelligencePack [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9450d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="9450d-105">DESCRIPTION</span></span>
<span data-ttu-id="9450d-106">**Get-AzOperationalInsightsIntelligencePack** cmdlet 'i kullanılabilir bir yönetim bilgileri paketini alır.</span><span class="sxs-lookup"><span data-stu-id="9450d-106">The **Get-AzOperationalInsightsIntelligencePack** cmdlet gets the available Intelligence Packs.</span></span>

## <span data-ttu-id="9450d-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9450d-107">EXAMPLES</span></span>

### <span data-ttu-id="9450d-108">Örnek 1: yönetim bilgileri alma paketleri</span><span class="sxs-lookup"><span data-stu-id="9450d-108">Example 1: Get Intelligence Packs</span></span>
```
PS C:\>Get-AzOperationalInsightsStorageInsight -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace"
```

<span data-ttu-id="9450d-109">Bu komut kullanılabilir Zektyönetim paketini alır.</span><span class="sxs-lookup"><span data-stu-id="9450d-109">This command gets the available Intelligence Packs.</span></span>

## <span data-ttu-id="9450d-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9450d-110">PARAMETERS</span></span>

### <span data-ttu-id="9450d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9450d-111">-DefaultProfile</span></span>
<span data-ttu-id="9450d-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="9450d-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9450d-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9450d-113">-ResourceGroupName</span></span>
<span data-ttu-id="9450d-114">Çalışma alanı içeren bir Azure Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9450d-114">Specifies the name of an Azure resource group that contains a workspace.</span></span>

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

### <span data-ttu-id="9450d-115">-Çalışmaalanıadı</span><span class="sxs-lookup"><span data-stu-id="9450d-115">-WorkspaceName</span></span>
<span data-ttu-id="9450d-116">Çalışma alanı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9450d-116">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="9450d-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9450d-117">CommonParameters</span></span>
<span data-ttu-id="9450d-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9450d-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9450d-119">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9450d-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9450d-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9450d-120">INPUTS</span></span>

### <span data-ttu-id="9450d-121">System. String</span><span class="sxs-lookup"><span data-stu-id="9450d-121">System.String</span></span>

## <span data-ttu-id="9450d-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9450d-122">OUTPUTS</span></span>

### <span data-ttu-id="9450d-123">Microsoft. Azure. Commands. Operationalınsights. modeller. PSIntelligencePack</span><span class="sxs-lookup"><span data-stu-id="9450d-123">Microsoft.Azure.Commands.OperationalInsights.Models.PSIntelligencePack</span></span>

## <span data-ttu-id="9450d-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9450d-124">NOTES</span></span>

## <span data-ttu-id="9450d-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9450d-125">RELATED LINKS</span></span>

[<span data-ttu-id="9450d-126">Azure Operasyonel Öngörüler cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="9450d-126">Azure Operational Insights Cmdlets</span></span>](/powershell/module/az.operationalinsights)


