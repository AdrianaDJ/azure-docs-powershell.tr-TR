---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/new-azanalysisservicesfirewallconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/New-AzAnalysisServicesFirewallConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/New-AzAnalysisServicesFirewallConfig.md
ms.openlocfilehash: f3c84b22a9ea8c913cb520ae913fff89ae9470ba
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93751216"
---
# <span data-ttu-id="ca48e-101">New-AzAnalysisServicesFirewallConfig</span><span class="sxs-lookup"><span data-stu-id="ca48e-101">New-AzAnalysisServicesFirewallConfig</span></span>

## <span data-ttu-id="ca48e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ca48e-102">SYNOPSIS</span></span>
<span data-ttu-id="ca48e-103">Yeni bir Analysis Services güvenlik duvarı yapılandırması oluşturur</span><span class="sxs-lookup"><span data-stu-id="ca48e-103">Creates a new Analysis Services firewall config</span></span> 

## <span data-ttu-id="ca48e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ca48e-104">SYNTAX</span></span>

```
New-AzAnalysisServicesFirewallConfig [-EnablePowerBIService]
 [-FirewallRule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallRule]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ca48e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ca48e-105">DESCRIPTION</span></span>
<span data-ttu-id="ca48e-106">New-AzAnalysisServicesFirewallConfig yeni bir güvenlik duvarı yapılandırma nesnesi oluşturur</span><span class="sxs-lookup"><span data-stu-id="ca48e-106">The New-AzAnalysisServicesFirewallConfig creates a new firewall config object</span></span>

## <span data-ttu-id="ca48e-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ca48e-107">EXAMPLES</span></span>

### <span data-ttu-id="ca48e-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="ca48e-108">Example 1</span></span>
```
PS C:\> $rule1 = New-AzAnalysisServicesFirewallRule -FirewallRuleName rule1 -RangeStart 0.0.0.0 -RangeEnd 255.255.255.255
PS C:\> $rule2 = New-AzAnalysisServicesFirewallRule -FirewallRuleName rule2 -RangeStart 6.6.6.6 -RangeEnd 7.7.7.7
PS C:\> $config = New-AzAnalysisServicesFirewallConfig -EnablePowerBIService -FirewallRule $rule1,$rule2
```

<span data-ttu-id="ca48e-109">Power BI hizmetinden Access 'i etkinleştirerek iki kurala sahip bir güvenlik duvarı yapılandırma nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ca48e-109">Creates a firewall config object with two rules while also enabling access from Power BI service.</span></span>

## <span data-ttu-id="ca48e-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ca48e-110">PARAMETERS</span></span>

### <span data-ttu-id="ca48e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca48e-111">-DefaultProfile</span></span>
<span data-ttu-id="ca48e-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ca48e-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ca48e-113">-Enablepowerbıervice</span><span class="sxs-lookup"><span data-stu-id="ca48e-113">-EnablePowerBIService</span></span>
<span data-ttu-id="ca48e-114">Power BI 'deki erişime izin verme</span><span class="sxs-lookup"><span data-stu-id="ca48e-114">A flag to indicate if the firewall is allowing access from Power BI</span></span>

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

### <span data-ttu-id="ca48e-115">-FirewallRule</span><span class="sxs-lookup"><span data-stu-id="ca48e-115">-FirewallRule</span></span>
<span data-ttu-id="ca48e-116">Güvenlik Duvarı kurallarının listesi</span><span class="sxs-lookup"><span data-stu-id="ca48e-116">A list of firewall rules</span></span>

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

### <span data-ttu-id="ca48e-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca48e-117">CommonParameters</span></span>
<span data-ttu-id="ca48e-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ca48e-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca48e-119">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ca48e-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca48e-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ca48e-120">INPUTS</span></span>

### <span data-ttu-id="ca48e-121">System. Koleksiyonlar. Generic. LIST ' 1 [[Microsoft. Azure. Commands. AnalysisServices. modeller. PsAzureAnalysisServicesFirewallRule, Microsoft. Azure. PowerShell. cmdlet. AnalysisServices, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="ca48e-121">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallRule, Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="ca48e-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ca48e-122">OUTPUTS</span></span>

### <span data-ttu-id="ca48e-123">Microsoft. Azure. Commands. AnalysisServices. modeller. Psazureanalysisservices, Allconfig</span><span class="sxs-lookup"><span data-stu-id="ca48e-123">Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallConfig</span></span>

## <span data-ttu-id="ca48e-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ca48e-124">NOTES</span></span>

## <span data-ttu-id="ca48e-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ca48e-125">RELATED LINKS</span></span>

[<span data-ttu-id="ca48e-126">Yeni-AzAnalysisServicesFirewallRule</span><span class="sxs-lookup"><span data-stu-id="ca48e-126">New-AzAnalysisServicesFirewallRule</span></span>](./New-AzAnalysisServicesFirewallRule.md)