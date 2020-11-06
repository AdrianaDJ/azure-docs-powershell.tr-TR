---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/get-azurermservicebusrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusRule.md
ms.openlocfilehash: 3eb629665f8bc4ed030b5c616410fb47455136e2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593416"
---
# <span data-ttu-id="699ff-101">Get-AzureRmServiceBusRule</span><span class="sxs-lookup"><span data-stu-id="699ff-101">Get-AzureRmServiceBusRule</span></span>

## <span data-ttu-id="699ff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="699ff-102">SYNOPSIS</span></span>
<span data-ttu-id="699ff-103">Belirli bir konu aboneliği için belirtilen kuralın açıklamasını alır.</span><span class="sxs-lookup"><span data-stu-id="699ff-103">Gets a description of the specified rule for a given Subscription of  Topic.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="699ff-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="699ff-104">SYNTAX</span></span>

```
Get-AzureRmServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="699ff-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="699ff-105">DESCRIPTION</span></span>
<span data-ttu-id="699ff-106">**Get-AzureRmServiceBusRule** cmdlet 'i belirtilen kuralın söz konusu aboneliğindeki açıklamasını alır.</span><span class="sxs-lookup"><span data-stu-id="699ff-106">The **Get-AzureRmServiceBusRule** cmdlet gets the description of the specified rule in the given subscription of topic.</span></span>

## <span data-ttu-id="699ff-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="699ff-107">EXAMPLES</span></span>

### <span data-ttu-id="699ff-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="699ff-108">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -NAme SBRule
```

<span data-ttu-id="699ff-109">Belirtilen aboneliğin belirtilen kural açıklamasını döndürür.</span><span class="sxs-lookup"><span data-stu-id="699ff-109">Returns the specified rule description for a specified subscription.</span></span>

## <span data-ttu-id="699ff-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="699ff-110">PARAMETERS</span></span>

### <span data-ttu-id="699ff-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="699ff-111">-DefaultProfile</span></span>
<span data-ttu-id="699ff-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="699ff-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="699ff-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="699ff-113">-Name</span></span>
<span data-ttu-id="699ff-114">Kural adı.</span><span class="sxs-lookup"><span data-stu-id="699ff-114">Rule Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="699ff-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="699ff-115">-Namespace</span></span>
<span data-ttu-id="699ff-116">Ad alanı adı.</span><span class="sxs-lookup"><span data-stu-id="699ff-116">Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="699ff-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="699ff-117">-ResourceGroupName</span></span>
<span data-ttu-id="699ff-118">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="699ff-118">The name of the resource group</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="699ff-119">-Abonelik</span><span class="sxs-lookup"><span data-stu-id="699ff-119">-Subscription</span></span>
<span data-ttu-id="699ff-120">Abonelik adı.</span><span class="sxs-lookup"><span data-stu-id="699ff-120">Subscription Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SubscriptionName

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="699ff-121">-Konu</span><span class="sxs-lookup"><span data-stu-id="699ff-121">-Topic</span></span>
<span data-ttu-id="699ff-122">Konu adı.</span><span class="sxs-lookup"><span data-stu-id="699ff-122">Topic Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="699ff-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="699ff-123">CommonParameters</span></span>
<span data-ttu-id="699ff-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="699ff-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="699ff-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="699ff-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="699ff-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="699ff-126">INPUTS</span></span>

### <span data-ttu-id="699ff-127">System. String</span><span class="sxs-lookup"><span data-stu-id="699ff-127">System.String</span></span>

## <span data-ttu-id="699ff-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="699ff-128">OUTPUTS</span></span>

### <span data-ttu-id="699ff-129">Microsoft. Azure. Commands. ServiceBus. modeller. PSRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="699ff-129">Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes</span></span>

## <span data-ttu-id="699ff-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="699ff-130">NOTES</span></span>

## <span data-ttu-id="699ff-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="699ff-131">RELATED LINKS</span></span>

