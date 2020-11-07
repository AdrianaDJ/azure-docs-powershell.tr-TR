---
external help file: Microsoft.Azure.Commands.AnalysisServices.dll-Help.xml
Module Name: AzureRM.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.analysisservices/new-azurermanalysisservicesfirewallconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/New-AzureRmAnalysisServicesFirewallConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices/help/New-AzureRmAnalysisServicesFirewallConfig.md
ms.openlocfilehash: ea1a656222383428f7e951ce858ec94c3fdc979e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763292"
---
# <span data-ttu-id="1da10-101">New-AzureRmAnalysisServicesFirewallConfig</span><span class="sxs-lookup"><span data-stu-id="1da10-101">New-AzureRmAnalysisServicesFirewallConfig</span></span>

## <span data-ttu-id="1da10-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1da10-102">SYNOPSIS</span></span>
<span data-ttu-id="1da10-103">Yeni bir Analysis Services güvenlik duvarı yapılandırması oluşturur</span><span class="sxs-lookup"><span data-stu-id="1da10-103">Creates a new Analysis Services firewall config</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1da10-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1da10-104">SYNTAX</span></span>

```
New-AzureRmAnalysisServicesFirewallConfig [-EnablePowerBIService] [-FirewallRules] List<Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesFirewallRule> 
```

## <span data-ttu-id="1da10-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="1da10-105">DESCRIPTION</span></span>
<span data-ttu-id="1da10-106">New-AzureRmAnalysisServicesFirewallConfig yeni bir güvenlik duvarı yapılandırma nesnesi oluşturur</span><span class="sxs-lookup"><span data-stu-id="1da10-106">The New-AzureRmAnalysisServicesFirewallConfig creates a new firewall config object</span></span>

## <span data-ttu-id="1da10-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1da10-107">EXAMPLES</span></span>

### <span data-ttu-id="1da10-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="1da10-108">Example 1</span></span>
```
PS C:\> $rule1 = New-AzureRmAnalysisServicesFirewallRule -FirewallRuleName rule1 -RangeStart 0.0.0.0 -RangeEnd 255.255.255.255
PS C:\> $rule2 = New-AzureRmAnalysisServicesFirewallRule -FirewallRuleName rule2 -RangeStart 6.6.6.6 -RangeEnd 7.7.7.7
PS C:\> New-AzureRmAnalysisServicesFirewallConfig -EnablePowerBIService -FirewallRules $rule1,$rule2
```

<span data-ttu-id="1da10-109">Power BI hizmetini etkinleştirmeden bir güvenlik duvarı kuralı yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1da10-109">Creates a firewall rule config without enabling power bi service.</span></span>

## <span data-ttu-id="1da10-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1da10-110">PARAMETERS</span></span>

### <span data-ttu-id="1da10-111">-Enablepowerbıervice</span><span class="sxs-lookup"><span data-stu-id="1da10-111">-EnablePowerBIService</span></span>
<span data-ttu-id="1da10-112">PowerBI hizmeti 'ni etkinleştirir</span><span class="sxs-lookup"><span data-stu-id="1da10-112">A flag to indicate if enable PowerBI service</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1da10-113">-FirewallRules</span><span class="sxs-lookup"><span data-stu-id="1da10-113">-FirewallRules</span></span>
<span data-ttu-id="1da10-114">Güvenlik Duvarı kurallarının listesi</span><span class="sxs-lookup"><span data-stu-id="1da10-114">A list of firewall rules</span></span>

```yaml
Type: List<Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesFirewallRule>
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="1da10-115">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1da10-115">INPUTS</span></span>

## <span data-ttu-id="1da10-116">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1da10-116">OUTPUTS</span></span>

### <span data-ttu-id="1da10-117">Microsoft. Azure. Commands. AnalysisServices. modeller. AzureAnalysisServicesFirewallConfig</span><span class="sxs-lookup"><span data-stu-id="1da10-117">Microsoft.Azure.Commands.AnalysisServices.Models.AzureAnalysisServicesFirewallConfig</span></span>

## <span data-ttu-id="1da10-118">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1da10-118">RELATED LINKS</span></span>

[<span data-ttu-id="1da10-119">New-AzureRmAnalysisServicesFirewallConfig</span><span class="sxs-lookup"><span data-stu-id="1da10-119">New-AzureRmAnalysisServicesFirewallConfig</span></span>](./New-AzureRmAnalysisServicesFirewallConfig.md)
