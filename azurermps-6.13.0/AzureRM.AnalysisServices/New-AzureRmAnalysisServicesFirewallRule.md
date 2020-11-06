---
external help file: Microsoft.Azure.Commands.AnalysisServices.dll-Help.xml
Module Name: AzureRM.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.analysisservices/new-azurermanalysisservicesfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/New-AzureRmAnalysisServicesFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/New-AzureRmAnalysisServicesFirewallRule.md
ms.openlocfilehash: 2a47c97ea189d4064edae7a871e21465d866f1f1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589622"
---
# <span data-ttu-id="f2eeb-101">New-AzureRmAnalysisServicesFirewallRule</span><span class="sxs-lookup"><span data-stu-id="f2eeb-101">New-AzureRmAnalysisServicesFirewallRule</span></span>

## <span data-ttu-id="f2eeb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f2eeb-102">SYNOPSIS</span></span>
<span data-ttu-id="f2eeb-103">Yeni bir Analysis Services güvenlik duvarı kuralı oluşturur</span><span class="sxs-lookup"><span data-stu-id="f2eeb-103">Creates a new Analysis Services firewall rule</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f2eeb-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f2eeb-104">SYNTAX</span></span>

```
New-AzureRmAnalysisServicesFirewallRule [-FirewallRuleName] <String> [-RangeStart] <String>
 [-RangeEnd] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f2eeb-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f2eeb-105">DESCRIPTION</span></span>
<span data-ttu-id="f2eeb-106">New-AzureRmAnalysisServicesFirewallRule yeni bir güvenlik duvarı kuralı nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f2eeb-106">The New-AzureRmAnalysisServicesFirewallRule creates a new firewall rule object.</span></span>

## <span data-ttu-id="f2eeb-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f2eeb-107">EXAMPLES</span></span>

### <span data-ttu-id="f2eeb-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="f2eeb-108">Example 1</span></span>
```
PS C:\> New-AzureRmAnalysisServicesFirewallRule -FirewallRuleName rule1 -RangeStart 0.0.0.0 -RangeEnd 255.255.255.255
```

<span data-ttu-id="f2eeb-109">Başlangıç aralığı 0.0.0.0 ve bitiş aralığı 255.255.255.255 olan rule1 adlı bir güvenlik duvarı kuralı oluşturur</span><span class="sxs-lookup"><span data-stu-id="f2eeb-109">Creates a firewall rule named rule1 with start range 0.0.0.0 and end range 255.255.255.255</span></span>

## <span data-ttu-id="f2eeb-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f2eeb-110">PARAMETERS</span></span>

### <span data-ttu-id="f2eeb-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2eeb-111">-DefaultProfile</span></span>
<span data-ttu-id="f2eeb-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f2eeb-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f2eeb-113">-FirewallRuleName</span><span class="sxs-lookup"><span data-stu-id="f2eeb-113">-FirewallRuleName</span></span>
<span data-ttu-id="f2eeb-114">Güvenlik duvarı kuralının adı</span><span class="sxs-lookup"><span data-stu-id="f2eeb-114">Name of firewall rule</span></span>

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

### <span data-ttu-id="f2eeb-115">-RangeEnd</span><span class="sxs-lookup"><span data-stu-id="f2eeb-115">-RangeEnd</span></span>
<span data-ttu-id="f2eeb-116">Güvenlik duvarı kuralının Aralık sonu</span><span class="sxs-lookup"><span data-stu-id="f2eeb-116">The range end of a firewall rule</span></span>

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

### <span data-ttu-id="f2eeb-117">-RangeStart</span><span class="sxs-lookup"><span data-stu-id="f2eeb-117">-RangeStart</span></span>
<span data-ttu-id="f2eeb-118">Güvenlik duvarının başlangıç aralığı</span><span class="sxs-lookup"><span data-stu-id="f2eeb-118">The range start of a firewall rule</span></span>

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

### <span data-ttu-id="f2eeb-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2eeb-119">CommonParameters</span></span>
<span data-ttu-id="f2eeb-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f2eeb-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2eeb-121">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f2eeb-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2eeb-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f2eeb-122">INPUTS</span></span>

### <span data-ttu-id="f2eeb-123">System. String</span><span class="sxs-lookup"><span data-stu-id="f2eeb-123">System.String</span></span>

## <span data-ttu-id="f2eeb-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f2eeb-124">OUTPUTS</span></span>

### <span data-ttu-id="f2eeb-125">Microsoft. Azure. Commands. AnalysisServices. modeller. Psazureanalysisservices, Allrule</span><span class="sxs-lookup"><span data-stu-id="f2eeb-125">Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallRule</span></span>

## <span data-ttu-id="f2eeb-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f2eeb-126">NOTES</span></span>

## <span data-ttu-id="f2eeb-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f2eeb-127">RELATED LINKS</span></span>

[<span data-ttu-id="f2eeb-128">New-AzureRmAnalysisServicesFirewallConfig</span><span class="sxs-lookup"><span data-stu-id="f2eeb-128">New-AzureRmAnalysisServicesFirewallConfig</span></span>](./New-AzureRmAnalysisServicesFirewallConfig.md)
