---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/get-azurermeventhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHub.md
ms.openlocfilehash: e87300af80c38fa0f7989836c992fd1baa53ba6d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589793"
---
# <span data-ttu-id="29c03-101">Get-AzureRmEventHub</span><span class="sxs-lookup"><span data-stu-id="29c03-101">Get-AzureRmEventHub</span></span>

## <span data-ttu-id="29c03-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="29c03-102">SYNOPSIS</span></span>
<span data-ttu-id="29c03-103">Tek bir olay hub 'ının ayrıntılarını alır veya Olay Hub 'Larının listesini alır.</span><span class="sxs-lookup"><span data-stu-id="29c03-103">Gets the details of a single Event Hub, or gets a list of Event Hubs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="29c03-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="29c03-104">SYNTAX</span></span>

```
Get-AzureRmEventHub [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="29c03-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="29c03-105">DESCRIPTION</span></span>
<span data-ttu-id="29c03-106">Get-AzureRmEventHub cmdlet 'i, bir olay hub ayrıntısını veya geçerli ad alanındaki tüm olay hub 'Larının listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="29c03-106">The Get-AzureRmEventHub cmdlet returns either the details of an Event Hub, or a list of all Event Hubs in the current namespace.</span></span>
<span data-ttu-id="29c03-107">Olay Hub adı sağlanmışsa, tek bir olay hub 'ının ayrıntıları döndürülür.</span><span class="sxs-lookup"><span data-stu-id="29c03-107">If the Event Hub name is provided, the details of a single Event Hub are returned.</span></span>
<span data-ttu-id="29c03-108">Bir olay hub adı sağlanmadıysa, belirtilen ad alanındaki tüm olay hub 'Larının listesi döndürülür.</span><span class="sxs-lookup"><span data-stu-id="29c03-108">If an Event Hub name is not provided, a list of all Event Hubs in the specified namespace is returned.</span></span>

## <span data-ttu-id="29c03-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="29c03-109">EXAMPLES</span></span>

### <span data-ttu-id="29c03-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="29c03-110">Example 1</span></span>
```
PS C:\> Get-AzureRmEventHub -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

<span data-ttu-id="29c03-111">Olay Hub \` myeventhubname 'in ayrıntılarını verir \` .</span><span class="sxs-lookup"><span data-stu-id="29c03-111">Returns the details of the Event Hub \`MyEventHubName\`.</span></span>

### <span data-ttu-id="29c03-112">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="29c03-112">Example 2</span></span>
```
PS C:\> Get-AzureRmEventHub -ResourceGroup MyResourceGroupName -NamespaceName MyNamespaceName
```

<span data-ttu-id="29c03-113">Mynamespacadındaki Olay Hub 'Larının listesini döndürür \` \` .</span><span class="sxs-lookup"><span data-stu-id="29c03-113">Returns a list of Event Hubs in the namespace \`MyNamespaceName\`.</span></span>

## <span data-ttu-id="29c03-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="29c03-114">PARAMETERS</span></span>

### <span data-ttu-id="29c03-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29c03-115">-DefaultProfile</span></span>
<span data-ttu-id="29c03-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="29c03-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="29c03-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="29c03-117">-Name</span></span>
<span data-ttu-id="29c03-118">EventHub adı</span><span class="sxs-lookup"><span data-stu-id="29c03-118">EventHub Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: EventHubName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29c03-119">-Namespace</span><span class="sxs-lookup"><span data-stu-id="29c03-119">-Namespace</span></span>
<span data-ttu-id="29c03-120">Ad alanı adı</span><span class="sxs-lookup"><span data-stu-id="29c03-120">Namespace Name</span></span>

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

### <span data-ttu-id="29c03-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29c03-121">-ResourceGroupName</span></span>
<span data-ttu-id="29c03-122">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="29c03-122">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29c03-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29c03-123">CommonParameters</span></span>
<span data-ttu-id="29c03-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="29c03-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="29c03-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="29c03-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29c03-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="29c03-126">INPUTS</span></span>

### <span data-ttu-id="29c03-127">System. String</span><span class="sxs-lookup"><span data-stu-id="29c03-127">System.String</span></span>


## <span data-ttu-id="29c03-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="29c03-128">OUTPUTS</span></span>

### <span data-ttu-id="29c03-129">System. Koleksiyonlar. Generic. LIST ' 1 [[Microsoft. Azure. Commands. EventHub. modeller. Pyetthubattributes, Microsoft. Azure. Commands. EventHub, Version = 0.5.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="29c03-129">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes, Microsoft.Azure.Commands.EventHub, Version=0.5.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>


## <span data-ttu-id="29c03-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="29c03-130">NOTES</span></span>

## <span data-ttu-id="29c03-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="29c03-131">RELATED LINKS</span></span>
