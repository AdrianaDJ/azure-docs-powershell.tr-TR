---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/new-azanalysisservicesfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/New-AzAnalysisServicesFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/New-AzAnalysisServicesFirewallRule.md
ms.openlocfilehash: 9aecede69497bd1a8723720200ed73e12b4aa776
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096657"
---
# <span data-ttu-id="e7319-101">New-AzAnalysisServicesFirewallRule</span><span class="sxs-lookup"><span data-stu-id="e7319-101">New-AzAnalysisServicesFirewallRule</span></span>

## <span data-ttu-id="e7319-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e7319-102">SYNOPSIS</span></span>
<span data-ttu-id="e7319-103">Yeni bir Analysis Services güvenlik duvarı kuralı oluşturur</span><span class="sxs-lookup"><span data-stu-id="e7319-103">Creates a new Analysis Services firewall rule</span></span>

## <span data-ttu-id="e7319-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e7319-104">SYNTAX</span></span>

```
New-AzAnalysisServicesFirewallRule [-FirewallRuleName] <String> [-RangeStart] <String> [-RangeEnd] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e7319-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e7319-105">DESCRIPTION</span></span>
<span data-ttu-id="e7319-106">New-AzAnalysisServicesFirewallRule yeni bir güvenlik duvarı kuralı nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e7319-106">The New-AzAnalysisServicesFirewallRule creates a new firewall rule object.</span></span>

## <span data-ttu-id="e7319-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e7319-107">EXAMPLES</span></span>

### <span data-ttu-id="e7319-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="e7319-108">Example 1</span></span>
```
PS C:\> New-AzAnalysisServicesFirewallRule -FirewallRuleName rule1 -RangeStart 0.0.0.0 -RangeEnd 255.255.255.255
```

<span data-ttu-id="e7319-109">Başlangıç aralığı 0.0.0.0 ve bitiş aralığı 255.255.255.255 olan rule1 adlı bir güvenlik duvarı kuralı oluşturur</span><span class="sxs-lookup"><span data-stu-id="e7319-109">Creates a firewall rule named rule1 with start range 0.0.0.0 and end range 255.255.255.255</span></span>

## <span data-ttu-id="e7319-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e7319-110">PARAMETERS</span></span>

### <span data-ttu-id="e7319-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7319-111">-DefaultProfile</span></span>
<span data-ttu-id="e7319-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e7319-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e7319-113">-FirewallRuleName</span><span class="sxs-lookup"><span data-stu-id="e7319-113">-FirewallRuleName</span></span>
<span data-ttu-id="e7319-114">Güvenlik duvarı kuralının adı</span><span class="sxs-lookup"><span data-stu-id="e7319-114">Name of firewall rule</span></span>

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

### <span data-ttu-id="e7319-115">-RangeEnd</span><span class="sxs-lookup"><span data-stu-id="e7319-115">-RangeEnd</span></span>
<span data-ttu-id="e7319-116">Güvenlik duvarı kuralının Aralık sonu</span><span class="sxs-lookup"><span data-stu-id="e7319-116">The range end of a firewall rule</span></span>

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

### <span data-ttu-id="e7319-117">-RangeStart</span><span class="sxs-lookup"><span data-stu-id="e7319-117">-RangeStart</span></span>
<span data-ttu-id="e7319-118">Güvenlik duvarının başlangıç aralığı</span><span class="sxs-lookup"><span data-stu-id="e7319-118">The range start of a firewall rule</span></span>

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

### <span data-ttu-id="e7319-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7319-119">CommonParameters</span></span>
<span data-ttu-id="e7319-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e7319-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7319-121">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e7319-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7319-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e7319-122">INPUTS</span></span>

### <span data-ttu-id="e7319-123">System. String</span><span class="sxs-lookup"><span data-stu-id="e7319-123">System.String</span></span>

## <span data-ttu-id="e7319-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e7319-124">OUTPUTS</span></span>

### <span data-ttu-id="e7319-125">Microsoft. Azure. Commands. AnalysisServices. modeller. Psazureanalysisservices, Allrule</span><span class="sxs-lookup"><span data-stu-id="e7319-125">Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallRule</span></span>

## <span data-ttu-id="e7319-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e7319-126">NOTES</span></span>

## <span data-ttu-id="e7319-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e7319-127">RELATED LINKS</span></span>

[<span data-ttu-id="e7319-128">Yeni-AzAnalysisServicesFirewallConfig</span><span class="sxs-lookup"><span data-stu-id="e7319-128">New-AzAnalysisServicesFirewallConfig</span></span>](./New-AzAnalysisServicesFirewallConfig.md)