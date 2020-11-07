---
external help file: Microsoft.Azure.Commands.AnalysisServices.dll-Help.xml
Module Name: AzureRM.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.analysisservices/new-azurermanalysisservicesfirewallconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/New-AzureRmAnalysisServicesFirewallConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/New-AzureRmAnalysisServicesFirewallConfig.md
ms.openlocfilehash: 2369720eb3a2df1e1c65df727cb02c1464ddc218
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762500"
---
# <span data-ttu-id="d0388-101">New-AzureRmAnalysisServicesFirewallConfig</span><span class="sxs-lookup"><span data-stu-id="d0388-101">New-AzureRmAnalysisServicesFirewallConfig</span></span>

## <span data-ttu-id="d0388-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d0388-102">SYNOPSIS</span></span>
<span data-ttu-id="d0388-103">Yeni bir Analysis Services güvenlik duvarı yapılandırması oluşturur</span><span class="sxs-lookup"><span data-stu-id="d0388-103">Creates a new Analysis Services firewall config</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d0388-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d0388-104">SYNTAX</span></span>

```
New-AzureRmAnalysisServicesFirewallConfig [-EnablePowerBIService]
 [-FirewallRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallRule]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d0388-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="d0388-105">DESCRIPTION</span></span>
<span data-ttu-id="d0388-106">New-AzureRmAnalysisServicesFirewallConfig yeni bir güvenlik duvarı yapılandırma nesnesi oluşturur</span><span class="sxs-lookup"><span data-stu-id="d0388-106">The New-AzureRmAnalysisServicesFirewallConfig creates a new firewall config object</span></span>

## <span data-ttu-id="d0388-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d0388-107">EXAMPLES</span></span>

### <span data-ttu-id="d0388-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="d0388-108">Example 1</span></span>
```
PS C:\> $rule1 = New-AzureRmAnalysisServicesFirewallRule -FirewallRuleName rule1 -RangeStart 0.0.0.0 -RangeEnd 255.255.255.255
PS C:\> $rule2 = New-AzureRmAnalysisServicesFirewallRule -FirewallRuleName rule2 -RangeStart 6.6.6.6 -RangeEnd 7.7.7.7
PS C:\> $config = New-AzureRmAnalysisServicesFirewallConfig -EnablePowerBIService -FirewallRule $rule1,$rule2
```

<span data-ttu-id="d0388-109">Power BI hizmetinden Access 'i etkinleştirerek iki kurala sahip bir güvenlik duvarı yapılandırma nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d0388-109">Creates a firewall config object with two rules while also enabling access from Power BI service.</span></span>

## <span data-ttu-id="d0388-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d0388-110">PARAMETERS</span></span>

### <span data-ttu-id="d0388-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0388-111">-DefaultProfile</span></span>
<span data-ttu-id="d0388-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d0388-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d0388-113">-Enablepowerbıervice</span><span class="sxs-lookup"><span data-stu-id="d0388-113">-EnablePowerBIService</span></span>
<span data-ttu-id="d0388-114">Power BI 'deki erişime izin verme</span><span class="sxs-lookup"><span data-stu-id="d0388-114">A flag to indicate if the firewall is allowing access from Power BI</span></span>

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

### <span data-ttu-id="d0388-115">-FirewallRule</span><span class="sxs-lookup"><span data-stu-id="d0388-115">-FirewallRule</span></span>
<span data-ttu-id="d0388-116">Güvenlik Duvarı kurallarının listesi</span><span class="sxs-lookup"><span data-stu-id="d0388-116">A list of firewall rules</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallRule]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0388-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0388-117">CommonParameters</span></span>
<span data-ttu-id="d0388-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d0388-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0388-119">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d0388-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0388-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d0388-120">INPUTS</span></span>

### <span data-ttu-id="d0388-121">System. Koleksiyonlar. Generic. LIST ' 1 [[Microsoft. Azure. Commands. AnalysisServices. modeller. PsAzureAnalysisServicesFirewallRule, Microsoft. Azure. Commands. AnalysisServices, Version = 0.6.11.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="d0388-121">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallRule, Microsoft.Azure.Commands.AnalysisServices, Version=0.6.11.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="d0388-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d0388-122">OUTPUTS</span></span>

### <span data-ttu-id="d0388-123">Microsoft. Azure. Commands. AnalysisServices. modeller. Psazureanalysisservices, Allconfig</span><span class="sxs-lookup"><span data-stu-id="d0388-123">Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallConfig</span></span>

## <span data-ttu-id="d0388-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d0388-124">NOTES</span></span>

## <span data-ttu-id="d0388-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d0388-125">RELATED LINKS</span></span>

[<span data-ttu-id="d0388-126">New-AzureRmAnalysisServicesFirewallRule</span><span class="sxs-lookup"><span data-stu-id="d0388-126">New-AzureRmAnalysisServicesFirewallRule</span></span>](./New-AzureRmAnalysisServicesFirewallRule.md)
