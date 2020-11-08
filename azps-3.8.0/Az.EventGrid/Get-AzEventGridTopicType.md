---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgridtopictype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopicType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopicType.md
ms.openlocfilehash: 23392f77c9315cee2bf8b1b8369febbc2281c6ff
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93937763"
---
# <span data-ttu-id="a39ce-101">Get-AzEventGridTopicType</span><span class="sxs-lookup"><span data-stu-id="a39ce-101">Get-AzEventGridTopicType</span></span>

## <span data-ttu-id="a39ce-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a39ce-102">SYNOPSIS</span></span>
<span data-ttu-id="a39ce-103">Azure olay Kılavuzu tarafından desteklenen konu türleriyle ilgili ayrıntıları alır.</span><span class="sxs-lookup"><span data-stu-id="a39ce-103">Gets the details about the topic types supported by Azure Event Grid.</span></span>

## <span data-ttu-id="a39ce-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a39ce-104">SYNTAX</span></span>

```
Get-AzEventGridTopicType [[-Name] <String>] [-IncludeEventTypeData] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a39ce-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a39ce-105">DESCRIPTION</span></span>
<span data-ttu-id="a39ce-106">Azure olay Kılavuzu tarafından desteklenen konu türlerinin ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="a39ce-106">Gets the details of topic types supported by Azure Event Grid.</span></span>
<span data-ttu-id="a39ce-107">Konu türü adı belirtilmişse, bu konu türüyle ilgili Ayrıntılar döndürülür.</span><span class="sxs-lookup"><span data-stu-id="a39ce-107">If a topic type name is specified, details about that topic type are returned.</span></span>
<span data-ttu-id="a39ce-108">Konu türü adı belirtilmezse, tüm konu türleriyle ilgili ayrıntılar verilir.</span><span class="sxs-lookup"><span data-stu-id="a39ce-108">If a topic type name is not specified, details about all topic types are returned.</span></span>
<span data-ttu-id="a39ce-109">Includeeventtypes belirtildiğinde, her konu türü tarafından desteklenen olay türleriyle ilgili bilgiler yanıta dahildir.</span><span class="sxs-lookup"><span data-stu-id="a39ce-109">If IncludeEventTypes is specified, information about event types supported by each topic type is included in the response.</span></span>

## <span data-ttu-id="a39ce-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a39ce-110">EXAMPLES</span></span>

### <span data-ttu-id="a39ce-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="a39ce-111">Example 1</span></span>
```powershell
PS C:\> Get-AzEventGridTopicType
```

<span data-ttu-id="a39ce-112">Konu türlerinin bir listesini alır.</span><span class="sxs-lookup"><span data-stu-id="a39ce-112">Gets a list of the topic types.</span></span>

### <span data-ttu-id="a39ce-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="a39ce-113">Example 2</span></span>
```powershell
PS C:\> Get-AzEventGridTopicType -Name "Microsoft.Storage.StorageAccounts"
```

<span data-ttu-id="a39ce-114">StorageAccounts konu türü hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="a39ce-114">Gets information about the StorageAccounts topic type.</span></span>

### <span data-ttu-id="a39ce-115">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="a39ce-115">Example 3</span></span>
```powershell
PS C:\> Get-AzEventGridTopicType -Name "Microsoft.Storage.StorageAccounts" -IncludeEventTypeData
```

<span data-ttu-id="a39ce-116">Storageaccounts konu türüyle ilgili bilgileri, StorageAccounts tarafından desteklenen olay türleriyle birlikte alır.</span><span class="sxs-lookup"><span data-stu-id="a39ce-116">Gets information about the StorageAccounts topic type, including the event types supported by StorageAccounts.</span></span>

## <span data-ttu-id="a39ce-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a39ce-117">PARAMETERS</span></span>

### <span data-ttu-id="a39ce-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a39ce-118">-DefaultProfile</span></span>
<span data-ttu-id="a39ce-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="a39ce-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a39ce-120">-Includeeventtypedata</span><span class="sxs-lookup"><span data-stu-id="a39ce-120">-IncludeEventTypeData</span></span>
<span data-ttu-id="a39ce-121">Belirtilmişse, yanıt bir konu türü tarafından desteklenen olay türlerini içerecektir.</span><span class="sxs-lookup"><span data-stu-id="a39ce-121">If specified, the response will include the event types supported by a topic type.</span></span>

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

### <span data-ttu-id="a39ce-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="a39ce-122">-Name</span></span>
<span data-ttu-id="a39ce-123">EventGrid konu türü adı.</span><span class="sxs-lookup"><span data-stu-id="a39ce-123">EventGrid Topic Type Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a39ce-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a39ce-124">CommonParameters</span></span>
<span data-ttu-id="a39ce-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a39ce-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a39ce-126">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a39ce-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a39ce-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a39ce-127">INPUTS</span></span>

### <span data-ttu-id="a39ce-128">System. String</span><span class="sxs-lookup"><span data-stu-id="a39ce-128">System.String</span></span>

## <span data-ttu-id="a39ce-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a39ce-129">OUTPUTS</span></span>

### <span data-ttu-id="a39ce-130">Microsoft. Azure. Commands. EventGrid. modeller. Pstopictypetypelistınstance</span><span class="sxs-lookup"><span data-stu-id="a39ce-130">Microsoft.Azure.Commands.EventGrid.Models.PSTopicTypeInfoListInstance</span></span>

### <span data-ttu-id="a39ce-131">Microsoft. Azure. Commands. EventGrid. modeller. Pstopictypeınfo</span><span class="sxs-lookup"><span data-stu-id="a39ce-131">Microsoft.Azure.Commands.EventGrid.Models.PSTopicTypeInfo</span></span>

## <span data-ttu-id="a39ce-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a39ce-132">NOTES</span></span>

## <span data-ttu-id="a39ce-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a39ce-133">RELATED LINKS</span></span>