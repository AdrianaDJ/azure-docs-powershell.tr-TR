---
external help file: Microsoft.Azure.Commands.AnalysisServices.dll-Help.xml
Module Name: AzureRM.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.analysisservices/new-azurermanalysisservicesfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/New-AzureRmAnalysisServicesFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/New-AzureRmAnalysisServicesFirewallRule.md
ms.openlocfilehash: 74a6d563772e84c7356c400b674cbab960ee8dd6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592524"
---
# <span data-ttu-id="7a7d8-101">New-AzureRmAnalysisServicesFirewallRule</span><span class="sxs-lookup"><span data-stu-id="7a7d8-101">New-AzureRmAnalysisServicesFirewallRule</span></span>

## <span data-ttu-id="7a7d8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7a7d8-102">SYNOPSIS</span></span>
<span data-ttu-id="7a7d8-103">Yeni bir Analysis Services güvenlik duvarı kuralı oluşturur</span><span class="sxs-lookup"><span data-stu-id="7a7d8-103">Creates a new Analysis Services firewall rule</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7a7d8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7a7d8-104">SYNTAX</span></span>

```
New-AzureRmAnalysisServicesFirewallRule [-FirewallRuleName] <String> [-RangeStart] <String> [-RangeEnd] <String>
```

## <span data-ttu-id="7a7d8-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="7a7d8-105">DESCRIPTION</span></span>
<span data-ttu-id="7a7d8-106">New-AzureRmAnalysisServicesFirewallRule yeni bir güvenlik duvarı kuralı nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7a7d8-106">The New-AzureRmAnalysisServicesFirewallRule creates a new firewall rule object.</span></span>

## <span data-ttu-id="7a7d8-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7a7d8-107">EXAMPLES</span></span>

### <span data-ttu-id="7a7d8-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="7a7d8-108">Example 1</span></span>
```
PS C:\> New-AzureRmAnalysisServicesFirewallRule -FirewallRuleName rule1 -RangeStart 0.0.0.0 -RangeEnd 255.255.255.255
```

<span data-ttu-id="7a7d8-109">Başlangıç aralığı 0.0.0.0 ve bitiş aralığı 255.255.255.255 olan rule1 adlı bir güvenlik duvarı kuralı oluşturur</span><span class="sxs-lookup"><span data-stu-id="7a7d8-109">Creates a firewall rule named rule1 with start range 0.0.0.0 and end range 255.255.255.255</span></span>

## <span data-ttu-id="7a7d8-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7a7d8-110">PARAMETERS</span></span>

### <span data-ttu-id="7a7d8-111">-FirewallRuleName</span><span class="sxs-lookup"><span data-stu-id="7a7d8-111">-FirewallRuleName</span></span>
<span data-ttu-id="7a7d8-112">Güvenlik duvarı kuralının adı</span><span class="sxs-lookup"><span data-stu-id="7a7d8-112">Name of firewall rule</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a7d8-113">-RangeStart</span><span class="sxs-lookup"><span data-stu-id="7a7d8-113">-RangeStart</span></span>
<span data-ttu-id="7a7d8-114">Güvenlik duvarının başlangıç aralığı</span><span class="sxs-lookup"><span data-stu-id="7a7d8-114">The range start of a firewall rule</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a7d8-115">-RangeEnd</span><span class="sxs-lookup"><span data-stu-id="7a7d8-115">-RangeEnd</span></span>
<span data-ttu-id="7a7d8-116">Güvenlik duvarı kuralının Aralık sonu</span><span class="sxs-lookup"><span data-stu-id="7a7d8-116">The range end of a firewall rule</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="7a7d8-117">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7a7d8-117">INPUTS</span></span>

## <span data-ttu-id="7a7d8-118">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7a7d8-118">OUTPUTS</span></span>

### <span data-ttu-id="7a7d8-119">Microsoft. Azure. Commands. AnalysisServices. modeller. AzureAnalysisServicesFirewallRule</span><span class="sxs-lookup"><span data-stu-id="7a7d8-119">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesFirewallRule</span></span>

## <span data-ttu-id="7a7d8-120">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7a7d8-120">RELATED LINKS</span></span>

[<span data-ttu-id="7a7d8-121">New-AzureRmAnalysisServicesFirewallConfig</span><span class="sxs-lookup"><span data-stu-id="7a7d8-121">New-AzureRmAnalysisServicesFirewallConfig</span></span>](./New-AzureRmAnalysisServicesFirewallConfig.md)
