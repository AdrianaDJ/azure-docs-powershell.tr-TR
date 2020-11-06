---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusRule.md
ms.openlocfilehash: e09e4f19a63eef1cd4b87760239d4456afee70fd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587790"
---
# <span data-ttu-id="69ae7-101">Get-AzureRmServiceBusRule</span><span class="sxs-lookup"><span data-stu-id="69ae7-101">Get-AzureRmServiceBusRule</span></span>

## <span data-ttu-id="69ae7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="69ae7-102">SYNOPSIS</span></span>
<span data-ttu-id="69ae7-103">Belirli bir konu aboneliği için belirtilen kuralın açıklamasını alır.</span><span class="sxs-lookup"><span data-stu-id="69ae7-103">Gets a description of the specified rule for a given Subscription of  Topic.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="69ae7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="69ae7-104">SYNTAX</span></span>

```
Get-AzureRmServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="69ae7-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="69ae7-105">DESCRIPTION</span></span>
<span data-ttu-id="69ae7-106">**Get-AzureRmServiceBusRule** cmdlet 'i belirtilen kuralın söz konusu aboneliğindeki açıklamasını alır.</span><span class="sxs-lookup"><span data-stu-id="69ae7-106">The **Get-AzureRmServiceBusRule** cmdlet gets the description of the specified rule in the given subscription of topic.</span></span>

## <span data-ttu-id="69ae7-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="69ae7-107">EXAMPLES</span></span>

### <span data-ttu-id="69ae7-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="69ae7-108">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -NAme SBRule
```

<span data-ttu-id="69ae7-109">Belirtilen aboneliğin belirtilen kural açıklamasını döndürür.</span><span class="sxs-lookup"><span data-stu-id="69ae7-109">Returns the specified rule description for a specified subscription.</span></span>

## <span data-ttu-id="69ae7-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="69ae7-110">PARAMETERS</span></span>

### <span data-ttu-id="69ae7-111">-Ad</span><span class="sxs-lookup"><span data-stu-id="69ae7-111">-Name</span></span>
<span data-ttu-id="69ae7-112">Kural adı.</span><span class="sxs-lookup"><span data-stu-id="69ae7-112">Rule Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69ae7-113">-Namespace</span><span class="sxs-lookup"><span data-stu-id="69ae7-113">-Namespace</span></span>
<span data-ttu-id="69ae7-114">Ad alanı adı.</span><span class="sxs-lookup"><span data-stu-id="69ae7-114">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69ae7-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69ae7-115">-ResourceGroupName</span></span>
<span data-ttu-id="69ae7-116">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="69ae7-116">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69ae7-117">-Abonelik</span><span class="sxs-lookup"><span data-stu-id="69ae7-117">-Subscription</span></span>
<span data-ttu-id="69ae7-118">Abonelik adı.</span><span class="sxs-lookup"><span data-stu-id="69ae7-118">Subscription Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SubscriptionName

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69ae7-119">-Konu</span><span class="sxs-lookup"><span data-stu-id="69ae7-119">-Topic</span></span>
<span data-ttu-id="69ae7-120">Konu adı.</span><span class="sxs-lookup"><span data-stu-id="69ae7-120">Topic Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69ae7-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69ae7-121">-DefaultProfile</span></span>
<span data-ttu-id="69ae7-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="69ae7-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="69ae7-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69ae7-123">CommonParameters</span></span>
<span data-ttu-id="69ae7-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="69ae7-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69ae7-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="69ae7-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69ae7-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="69ae7-126">INPUTS</span></span>

### <span data-ttu-id="69ae7-127">System. String</span><span class="sxs-lookup"><span data-stu-id="69ae7-127">System.String</span></span>

## <span data-ttu-id="69ae7-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="69ae7-128">OUTPUTS</span></span>

### <span data-ttu-id="69ae7-129">Microsoft. Azure. Commands. ServiceBus. modellerini. RulesAttributes</span><span class="sxs-lookup"><span data-stu-id="69ae7-129">Microsoft.Azure.Commands.ServiceBus.Models.RulesAttributes</span></span>

## <span data-ttu-id="69ae7-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="69ae7-130">NOTES</span></span>

## <span data-ttu-id="69ae7-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="69ae7-131">RELATED LINKS</span></span>

