---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/get-azcognitiveservicesaccountnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountNetworkRuleSet.md
ms.openlocfilehash: 24b2cb6efca1213365c99a2c095f90e675c317c7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94095794"
---
# <span data-ttu-id="ba12a-101">Get-AzCognitiveServicesAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="ba12a-101">Get-AzCognitiveServicesAccountNetworkRuleSet</span></span>

## <span data-ttu-id="ba12a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ba12a-102">SYNOPSIS</span></span>
<span data-ttu-id="ba12a-103">Bir öğretici hizmet hesabının NetworkRule özelliğini alma</span><span class="sxs-lookup"><span data-stu-id="ba12a-103">Get the NetworkRule property of a Cognitive Services account</span></span>

## <span data-ttu-id="ba12a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ba12a-104">SYNTAX</span></span>

```
Get-AzCognitiveServicesAccountNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ba12a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ba12a-105">DESCRIPTION</span></span>
<span data-ttu-id="ba12a-106">**Get-Azlıveiveservicesaccountnetworkruleset** cmdlet 'i, bir öğretici hizmet hesabının networkrule özelliğini alır</span><span class="sxs-lookup"><span data-stu-id="ba12a-106">The **Get-AzCognitiveServicesAccountNetworkRuleSet** cmdlet gets the NetworkRule property of a Cognitive Services account</span></span>

## <span data-ttu-id="ba12a-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ba12a-107">EXAMPLES</span></span>

### <span data-ttu-id="ba12a-108">Örnek 1: belirtilen bir öğretici hizmet hesabının NetworkRule özelliğini al</span><span class="sxs-lookup"><span data-stu-id="ba12a-108">Example 1: Get NetworkRule property of a specified Cognitive Services account</span></span>
```
PS C:\> Get-AzCognitiveServicesAccountNetworkRuleSet  -ResourceGroupName "rg1" -Name "myaccount"
```

<span data-ttu-id="ba12a-109">Bu komut belirtilen bir öğretici hizmet hesabının NetworkRule özelliğini alır</span><span class="sxs-lookup"><span data-stu-id="ba12a-109">This command gets NetworkRule property of a specified Cognitive Services account</span></span>

## <span data-ttu-id="ba12a-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ba12a-110">PARAMETERS</span></span>

### <span data-ttu-id="ba12a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba12a-111">-DefaultProfile</span></span>
<span data-ttu-id="ba12a-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ba12a-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ba12a-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="ba12a-113">-Name</span></span>
<span data-ttu-id="ba12a-114">Öğretici hizmetler hesap adı.</span><span class="sxs-lookup"><span data-stu-id="ba12a-114">Cognitive Services Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CognitiveServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba12a-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba12a-115">-ResourceGroupName</span></span>
<span data-ttu-id="ba12a-116">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="ba12a-116">Resource Group Name.</span></span>

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

### <span data-ttu-id="ba12a-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba12a-117">CommonParameters</span></span>
<span data-ttu-id="ba12a-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ba12a-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba12a-119">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="ba12a-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba12a-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ba12a-120">INPUTS</span></span>

### <span data-ttu-id="ba12a-121">System. String</span><span class="sxs-lookup"><span data-stu-id="ba12a-121">System.String</span></span>

## <span data-ttu-id="ba12a-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ba12a-122">OUTPUTS</span></span>

### <span data-ttu-id="ba12a-123">Microsoft. Azure. Commands. Management. öğretici ınitialveservices. modeller. PSNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="ba12a-123">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSNetworkRuleSet</span></span>

## <span data-ttu-id="ba12a-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ba12a-124">NOTES</span></span>

## <span data-ttu-id="ba12a-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ba12a-125">RELATED LINKS</span></span>
