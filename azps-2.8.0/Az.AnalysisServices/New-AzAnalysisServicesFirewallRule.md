---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/new-azanalysisservicesfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/New-AzAnalysisServicesFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/New-AzAnalysisServicesFirewallRule.md
ms.openlocfilehash: 7fb766bfa65d37fd8491e93593b3ea423938fd3f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753643"
---
# <span data-ttu-id="dc612-101">New-AzAnalysisServicesFirewallRule</span><span class="sxs-lookup"><span data-stu-id="dc612-101">New-AzAnalysisServicesFirewallRule</span></span>

## <span data-ttu-id="dc612-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dc612-102">SYNOPSIS</span></span>
<span data-ttu-id="dc612-103">Yeni bir Analysis Services güvenlik duvarı kuralı oluşturur</span><span class="sxs-lookup"><span data-stu-id="dc612-103">Creates a new Analysis Services firewall rule</span></span>

## <span data-ttu-id="dc612-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="dc612-104">SYNTAX</span></span>

```
New-AzAnalysisServicesFirewallRule [-FirewallRuleName] <String> [-RangeStart] <String> [-RangeEnd] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dc612-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="dc612-105">DESCRIPTION</span></span>
<span data-ttu-id="dc612-106">New-AzAnalysisServicesFirewallRule yeni bir güvenlik duvarı kuralı nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="dc612-106">The New-AzAnalysisServicesFirewallRule creates a new firewall rule object.</span></span>

## <span data-ttu-id="dc612-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="dc612-107">EXAMPLES</span></span>

### <span data-ttu-id="dc612-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="dc612-108">Example 1</span></span>
```
PS C:\> New-AzAnalysisServicesFirewallRule -FirewallRuleName rule1 -RangeStart 0.0.0.0 -RangeEnd 255.255.255.255
```

<span data-ttu-id="dc612-109">Başlangıç aralığı 0.0.0.0 ve bitiş aralığı 255.255.255.255 olan rule1 adlı bir güvenlik duvarı kuralı oluşturur</span><span class="sxs-lookup"><span data-stu-id="dc612-109">Creates a firewall rule named rule1 with start range 0.0.0.0 and end range 255.255.255.255</span></span>

## <span data-ttu-id="dc612-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="dc612-110">PARAMETERS</span></span>

### <span data-ttu-id="dc612-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc612-111">-DefaultProfile</span></span>
<span data-ttu-id="dc612-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="dc612-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dc612-113">-FirewallRuleName</span><span class="sxs-lookup"><span data-stu-id="dc612-113">-FirewallRuleName</span></span>
<span data-ttu-id="dc612-114">Güvenlik duvarı kuralının adı</span><span class="sxs-lookup"><span data-stu-id="dc612-114">Name of firewall rule</span></span>

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

### <span data-ttu-id="dc612-115">-RangeEnd</span><span class="sxs-lookup"><span data-stu-id="dc612-115">-RangeEnd</span></span>
<span data-ttu-id="dc612-116">Güvenlik duvarı kuralının Aralık sonu</span><span class="sxs-lookup"><span data-stu-id="dc612-116">The range end of a firewall rule</span></span>

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

### <span data-ttu-id="dc612-117">-RangeStart</span><span class="sxs-lookup"><span data-stu-id="dc612-117">-RangeStart</span></span>
<span data-ttu-id="dc612-118">Güvenlik duvarının başlangıç aralığı</span><span class="sxs-lookup"><span data-stu-id="dc612-118">The range start of a firewall rule</span></span>

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

### <span data-ttu-id="dc612-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc612-119">CommonParameters</span></span>
<span data-ttu-id="dc612-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="dc612-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc612-121">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dc612-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc612-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="dc612-122">INPUTS</span></span>

### <span data-ttu-id="dc612-123">System. String</span><span class="sxs-lookup"><span data-stu-id="dc612-123">System.String</span></span>

## <span data-ttu-id="dc612-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="dc612-124">OUTPUTS</span></span>

### <span data-ttu-id="dc612-125">Microsoft. Azure. Commands. AnalysisServices. modeller. Psazureanalysisservices, Allrule</span><span class="sxs-lookup"><span data-stu-id="dc612-125">Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallRule</span></span>

## <span data-ttu-id="dc612-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="dc612-126">NOTES</span></span>

## <span data-ttu-id="dc612-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="dc612-127">RELATED LINKS</span></span>

[<span data-ttu-id="dc612-128">Yeni-AzAnalysisServicesFirewallConfig</span><span class="sxs-lookup"><span data-stu-id="dc612-128">New-AzAnalysisServicesFirewallConfig</span></span>](./New-AzAnalysisServicesFirewallConfig.md)