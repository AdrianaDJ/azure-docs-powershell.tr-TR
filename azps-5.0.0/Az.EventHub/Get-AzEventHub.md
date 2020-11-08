---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/get-azeventhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHub.md
ms.openlocfilehash: ca2afaec702e27b4c20201cbd69984ec3827ded2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94277448"
---
# <span data-ttu-id="2cb44-101">Get-AzEventHub</span><span class="sxs-lookup"><span data-stu-id="2cb44-101">Get-AzEventHub</span></span>

## <span data-ttu-id="2cb44-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2cb44-102">SYNOPSIS</span></span>
<span data-ttu-id="2cb44-103">Tek bir olay hub 'ının ayrıntılarını alır veya Olay Hub 'Larının listesini alır.</span><span class="sxs-lookup"><span data-stu-id="2cb44-103">Gets the details of a single Event Hub, or gets a list of Event Hubs.</span></span>

## <span data-ttu-id="2cb44-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2cb44-104">SYNTAX</span></span>

```
Get-AzEventHub [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>] [-MaxCount <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2cb44-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="2cb44-105">DESCRIPTION</span></span>
<span data-ttu-id="2cb44-106">Get-AzEventHub cmdlet 'i, bir olay hub ayrıntısını veya geçerli ad alanındaki tüm olay hub 'Larının listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="2cb44-106">The Get-AzEventHub cmdlet returns either the details of an Event Hub, or a list of all Event Hubs in the current namespace.</span></span>
<span data-ttu-id="2cb44-107">Olay Hub adı sağlanmışsa, tek bir olay hub 'ının ayrıntıları döndürülür.</span><span class="sxs-lookup"><span data-stu-id="2cb44-107">If the Event Hub name is provided, the details of a single Event Hub are returned.</span></span>
<span data-ttu-id="2cb44-108">Bir olay hub adı sağlanmadıysa, belirtilen ad alanındaki tüm olay hub 'Larının listesi döndürülür.</span><span class="sxs-lookup"><span data-stu-id="2cb44-108">If an Event Hub name is not provided, a list of all Event Hubs in the specified namespace is returned.</span></span>

## <span data-ttu-id="2cb44-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2cb44-109">EXAMPLES</span></span>

### <span data-ttu-id="2cb44-110">Örnek 1: belirtilen EventHub</span><span class="sxs-lookup"><span data-stu-id="2cb44-110">Example 1: specified EventHub</span></span>
```powershell
PS C:\> Get-AzEventHub -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

<span data-ttu-id="2cb44-111">Olay Hub \` myeventhubname 'in ayrıntılarını verir \` .</span><span class="sxs-lookup"><span data-stu-id="2cb44-111">Returns the details of the Event Hub \`MyEventHubName\`.</span></span>

### <span data-ttu-id="2cb44-112">Örnek 2: belirtilen ad alanındaki EventHub listesi</span><span class="sxs-lookup"><span data-stu-id="2cb44-112">Example 2: List of EventHub in specified Namespace</span></span>
```powershell
PS C:\> Get-AzEventHub -ResourceGroup MyResourceGroupName -NamespaceName MyNamespaceName
```

<span data-ttu-id="2cb44-113">Mynamespacadındaki Olay Hub 'Larının listesini döndürür \` \` .</span><span class="sxs-lookup"><span data-stu-id="2cb44-113">Returns a list of Event Hubs in the namespace \`MyNamespaceName\`.</span></span>

## <span data-ttu-id="2cb44-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2cb44-114">PARAMETERS</span></span>

### <span data-ttu-id="2cb44-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2cb44-115">-DefaultProfile</span></span>
<span data-ttu-id="2cb44-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2cb44-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2cb44-117">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="2cb44-117">-MaxCount</span></span>
<span data-ttu-id="2cb44-118">Döndürülecek değer sayısının üst sınırını belirleme.</span><span class="sxs-lookup"><span data-stu-id="2cb44-118">Determine the maximum number of EventHubs to return.</span></span>

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

### <span data-ttu-id="2cb44-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="2cb44-119">-Name</span></span>
<span data-ttu-id="2cb44-120">EventHub adı</span><span class="sxs-lookup"><span data-stu-id="2cb44-120">EventHub Name</span></span>

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

### <span data-ttu-id="2cb44-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="2cb44-121">-Namespace</span></span>
<span data-ttu-id="2cb44-122">Ad alanı adı</span><span class="sxs-lookup"><span data-stu-id="2cb44-122">Namespace Name</span></span>

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

### <span data-ttu-id="2cb44-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2cb44-123">-ResourceGroupName</span></span>
<span data-ttu-id="2cb44-124">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="2cb44-124">Resource Group Name</span></span>

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

### <span data-ttu-id="2cb44-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2cb44-125">CommonParameters</span></span>
<span data-ttu-id="2cb44-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2cb44-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2cb44-127">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2cb44-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2cb44-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2cb44-128">INPUTS</span></span>

### <span data-ttu-id="2cb44-129">System. String</span><span class="sxs-lookup"><span data-stu-id="2cb44-129">System.String</span></span>

## <span data-ttu-id="2cb44-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2cb44-130">OUTPUTS</span></span>

### <span data-ttu-id="2cb44-131">Microsoft. Azure. Commands. EventHub. modeller. Pyetthubattributes</span><span class="sxs-lookup"><span data-stu-id="2cb44-131">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>

## <span data-ttu-id="2cb44-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2cb44-132">NOTES</span></span>

## <span data-ttu-id="2cb44-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2cb44-133">RELATED LINKS</span></span>
