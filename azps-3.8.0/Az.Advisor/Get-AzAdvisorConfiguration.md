---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Advisor.dll-Help.xml
Module Name: Az.Advisor
online version: https://docs.microsoft.com/en-us/powershell/module/az.advisor/get-azadvisorconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Get-AzAdvisorConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Get-AzAdvisorConfiguration.md
ms.openlocfilehash: 1e2f1daa222714c23f394d362222f9ef1fd1bde4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94097459"
---
# <span data-ttu-id="bb5f1-101">Get-AzAdvisorConfiguration</span><span class="sxs-lookup"><span data-stu-id="bb5f1-101">Get-AzAdvisorConfiguration</span></span>

## <span data-ttu-id="bb5f1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bb5f1-102">SYNOPSIS</span></span>
<span data-ttu-id="bb5f1-103">Verilen abonelik veya kaynak grubu için Azure Advisor yapılandırmalarını edinin.</span><span class="sxs-lookup"><span data-stu-id="bb5f1-103">Get the Azure Advisor configurations for the given subscription or resource group.</span></span>

## <span data-ttu-id="bb5f1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="bb5f1-104">SYNTAX</span></span>

```
Get-AzAdvisorConfiguration [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bb5f1-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="bb5f1-105">DESCRIPTION</span></span>
<span data-ttu-id="bb5f1-106">Abonelikle ilişkili yapılandırmaların iki türü vardır:</span><span class="sxs-lookup"><span data-stu-id="bb5f1-106">The configurations associated with a subscription have two types:</span></span>

<span data-ttu-id="bb5f1-107">Abonelik düzeyi yapılandırması: abonelik için bu türde yalnızca bir yapılandırma olabilir.</span><span class="sxs-lookup"><span data-stu-id="bb5f1-107">Subscription level configuration: There can be only one configuration of this type for a subscription.</span></span> <span data-ttu-id="bb5f1-108">LowCpuThreshold ve exclude bu yapılandırma türünün tek özelliğidir.</span><span class="sxs-lookup"><span data-stu-id="bb5f1-108">LowCpuThreshold and Exclude are the only property of this type of configuration.</span></span>

<span data-ttu-id="bb5f1-109">ResourceGroup düzeyi yapılandırması: bir abonelikteki her ResourceGroup için yalnızca bir yapılandırma olabilir.</span><span class="sxs-lookup"><span data-stu-id="bb5f1-109">ResourceGroup level configuration: There can be only one configuration for each ResourceGroup in a subscription.</span></span> <span data-ttu-id="bb5f1-110">Exclude, bu yapılandırma türünün tek özelliğidir.</span><span class="sxs-lookup"><span data-stu-id="bb5f1-110">Exclude is the only property of this type of configuration.</span></span>

## <span data-ttu-id="bb5f1-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="bb5f1-111">EXAMPLES</span></span>

### <span data-ttu-id="bb5f1-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="bb5f1-112">Example 1</span></span>
```powershell
PS C:\>$data = Get-AzAdvisorConfiguration
Id         : /subscriptions/{user_subscription}/providers/Microsoft.Advisor/configurations/{user_subscription}
Name       : {user_subscription}
Properties : Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorConfigurationProperties
Type       : Microsoft.Advisor/Configurations

Id         : /subscriptions/{user_subscription}/providers/Microsoft.Advisor/configurations/{user_subscription}-{resourceGroupName}
Name       : {user_subscription}-{resourceGroupName}
Properties : Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorConfigurationProperties
Type       : Microsoft.Advisor/Configurations

PS C:\>$data[0].Properties
AdditionalProperties :
Exclude              : False
LowCpuThreshold      : 20

PS C:\>$data[1].Properties
AdditionalProperties :
Exclude              : True
LowCpuThreshold      : null

```
<span data-ttu-id="bb5f1-113">Azure Danışmanı yapılandırmasının bir listesini alır.</span><span class="sxs-lookup"><span data-stu-id="bb5f1-113">Retrieves a list of Azure Advisor Configuration(s).</span></span>

## <span data-ttu-id="bb5f1-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="bb5f1-114">PARAMETERS</span></span>

### <span data-ttu-id="bb5f1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb5f1-115">-DefaultProfile</span></span>
<span data-ttu-id="bb5f1-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="bb5f1-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb5f1-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb5f1-117">-ResourceGroupName</span></span>
<span data-ttu-id="bb5f1-118">Yapılandırmanın kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="bb5f1-118">Resource Group name of the configuration</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb5f1-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb5f1-119">CommonParameters</span></span>
<span data-ttu-id="bb5f1-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="bb5f1-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="bb5f1-121">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bb5f1-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb5f1-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="bb5f1-122">INPUTS</span></span>

### <span data-ttu-id="bb5f1-123">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="bb5f1-123">None</span></span>

## <span data-ttu-id="bb5f1-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="bb5f1-124">OUTPUTS</span></span>

### <span data-ttu-id="bb5f1-125">Microsoft. Azure. Commands. Advisor. cmdlet. modeller. PsAzureAdvisorConfigurationData</span><span class="sxs-lookup"><span data-stu-id="bb5f1-125">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorConfigurationData</span></span>

## <span data-ttu-id="bb5f1-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="bb5f1-126">NOTES</span></span>

## <span data-ttu-id="bb5f1-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="bb5f1-127">RELATED LINKS</span></span>