---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/get-azeventhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/EventHub/EventHub/help/Get-AzEventHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/EventHub/EventHub/help/Get-AzEventHub.md
ms.openlocfilehash: a23fc0f41bd50a956c68cb52fa341f1bd8119372
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935902"
---
# <span data-ttu-id="b98bd-101">Get-AzEventHub</span><span class="sxs-lookup"><span data-stu-id="b98bd-101">Get-AzEventHub</span></span>

## <span data-ttu-id="b98bd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b98bd-102">SYNOPSIS</span></span>
<span data-ttu-id="b98bd-103">Tek bir olay hub 'ının ayrıntılarını alır veya Olay Hub 'Larının listesini alır.</span><span class="sxs-lookup"><span data-stu-id="b98bd-103">Gets the details of a single Event Hub, or gets a list of Event Hubs.</span></span>

## <span data-ttu-id="b98bd-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b98bd-104">SYNTAX</span></span>

```
Get-AzEventHub [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>] [-MaxCount <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b98bd-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b98bd-105">DESCRIPTION</span></span>
<span data-ttu-id="b98bd-106">Get-AzEventHub cmdlet 'i, bir olay hub ayrıntısını veya geçerli ad alanındaki tüm olay hub 'Larının listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="b98bd-106">The Get-AzEventHub cmdlet returns either the details of an Event Hub, or a list of all Event Hubs in the current namespace.</span></span>
<span data-ttu-id="b98bd-107">Olay Hub adı sağlanmışsa, tek bir olay hub 'ının ayrıntıları döndürülür.</span><span class="sxs-lookup"><span data-stu-id="b98bd-107">If the Event Hub name is provided, the details of a single Event Hub are returned.</span></span>
<span data-ttu-id="b98bd-108">Bir olay hub adı sağlanmadıysa, belirtilen ad alanındaki tüm olay hub 'Larının listesi döndürülür.</span><span class="sxs-lookup"><span data-stu-id="b98bd-108">If an Event Hub name is not provided, a list of all Event Hubs in the specified namespace is returned.</span></span>

## <span data-ttu-id="b98bd-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b98bd-109">EXAMPLES</span></span>

### <span data-ttu-id="b98bd-110">Örnek 1-belirtilen EventHub</span><span class="sxs-lookup"><span data-stu-id="b98bd-110">Example 1 - specified EventHub</span></span>
```
PS C:\> Get-AzEventHub -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

<span data-ttu-id="b98bd-111">Olay Hub \` myeventhubname 'in ayrıntılarını verir \` .</span><span class="sxs-lookup"><span data-stu-id="b98bd-111">Returns the details of the Event Hub \`MyEventHubName\`.</span></span>

### <span data-ttu-id="b98bd-112">Örnek 2-belirtilen ad alanındaki EventHub listesi</span><span class="sxs-lookup"><span data-stu-id="b98bd-112">Example 2 - List of EventHub in specified Namespace</span></span>
```
PS C:\> Get-AzEventHub -ResourceGroup MyResourceGroupName -NamespaceName MyNamespaceName
```

<span data-ttu-id="b98bd-113">Mynamespacadındaki Olay Hub 'Larının listesini döndürür \` \` .</span><span class="sxs-lookup"><span data-stu-id="b98bd-113">Returns a list of Event Hubs in the namespace \`MyNamespaceName\`.</span></span>

## <span data-ttu-id="b98bd-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b98bd-114">PARAMETERS</span></span>

### <span data-ttu-id="b98bd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b98bd-115">-DefaultProfile</span></span>
<span data-ttu-id="b98bd-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b98bd-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b98bd-117">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="b98bd-117">-MaxCount</span></span>
<span data-ttu-id="b98bd-118">Döndürülecek değer sayısının üst sınırını belirleme.</span><span class="sxs-lookup"><span data-stu-id="b98bd-118">Determine the maximum number of EventHubs to return.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b98bd-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="b98bd-119">-Name</span></span>
<span data-ttu-id="b98bd-120">EventHub adı</span><span class="sxs-lookup"><span data-stu-id="b98bd-120">EventHub Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: EventHubName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b98bd-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="b98bd-121">-Namespace</span></span>
<span data-ttu-id="b98bd-122">Ad alanı adı</span><span class="sxs-lookup"><span data-stu-id="b98bd-122">Namespace Name</span></span>

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

### <span data-ttu-id="b98bd-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b98bd-123">-ResourceGroupName</span></span>
<span data-ttu-id="b98bd-124">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="b98bd-124">Resource Group Name</span></span>

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

### <span data-ttu-id="b98bd-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b98bd-125">CommonParameters</span></span>
<span data-ttu-id="b98bd-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b98bd-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b98bd-127">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b98bd-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b98bd-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b98bd-128">INPUTS</span></span>

### <span data-ttu-id="b98bd-129">System. String</span><span class="sxs-lookup"><span data-stu-id="b98bd-129">System.String</span></span>

## <span data-ttu-id="b98bd-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b98bd-130">OUTPUTS</span></span>

### <span data-ttu-id="b98bd-131">Microsoft. Azure. Commands. EventHub. modeller. Pyetthubattributes</span><span class="sxs-lookup"><span data-stu-id="b98bd-131">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>

## <span data-ttu-id="b98bd-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b98bd-132">NOTES</span></span>

## <span data-ttu-id="b98bd-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b98bd-133">RELATED LINKS</span></span>
