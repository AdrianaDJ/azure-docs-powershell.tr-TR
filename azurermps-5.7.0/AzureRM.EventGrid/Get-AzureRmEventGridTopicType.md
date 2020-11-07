---
external help file: Microsoft.Azure.Commands.EventGrid.dll-Help.xml
Module Name: AzureRM.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventgrid/get-azurermeventgridtopictype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Get-AzureRmEventGridTopicType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Get-AzureRmEventGridTopicType.md
ms.openlocfilehash: bc272648920e29ed2e735ca08b9fa78563a9f9d0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763062"
---
# <span data-ttu-id="91b3f-101">Get-AzureRmEventGridTopicType</span><span class="sxs-lookup"><span data-stu-id="91b3f-101">Get-AzureRmEventGridTopicType</span></span>

## <span data-ttu-id="91b3f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="91b3f-102">SYNOPSIS</span></span>
<span data-ttu-id="91b3f-103">Azure olay Kılavuzu tarafından desteklenen konu türleriyle ilgili ayrıntıları alır.</span><span class="sxs-lookup"><span data-stu-id="91b3f-103">Gets the details about the topic types supported by Azure Event Grid.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="91b3f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="91b3f-104">SYNTAX</span></span>

```
Get-AzureRmEventGridTopicType [[-Name] <String>] [-IncludeEventTypeData]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="91b3f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="91b3f-105">DESCRIPTION</span></span>
<span data-ttu-id="91b3f-106">Azure olay Kılavuzu tarafından desteklenen konu türlerinin ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="91b3f-106">Gets the details of topic types supported by Azure Event Grid.</span></span>
<span data-ttu-id="91b3f-107">Konu türü adı belirtilmişse, bu konu türüyle ilgili Ayrıntılar döndürülür.</span><span class="sxs-lookup"><span data-stu-id="91b3f-107">If a topic type name is specified, details about that topic type are returned.</span></span>
<span data-ttu-id="91b3f-108">Konu türü adı belirtilmezse, tüm konu türleriyle ilgili ayrıntılar verilir.</span><span class="sxs-lookup"><span data-stu-id="91b3f-108">If a topic type name is not specified, details about all topic types are returned.</span></span>
<span data-ttu-id="91b3f-109">Includeeventtypes belirtildiğinde, her konu türü tarafından desteklenen olay türleriyle ilgili bilgiler yanıta dahildir.</span><span class="sxs-lookup"><span data-stu-id="91b3f-109">If IncludeEventTypes is specified, information about event types supported by each topic type is included in the response.</span></span>

## <span data-ttu-id="91b3f-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="91b3f-110">EXAMPLES</span></span>

### <span data-ttu-id="91b3f-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="91b3f-111">Example 1</span></span>
```
PS C:\> Get-AzureRmEventGridTopicType
```

<span data-ttu-id="91b3f-112">Konu türlerinin bir listesini alır.</span><span class="sxs-lookup"><span data-stu-id="91b3f-112">Gets a list of the topic types.</span></span>

### <span data-ttu-id="91b3f-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="91b3f-113">Example 2</span></span>
```
PS C:\> Get-AzureRmEventGridTopicType -Name "Microsoft.Storage.StorageAccounts"
```

<span data-ttu-id="91b3f-114">StorageAccounts konu türü hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="91b3f-114">Gets information about the StorageAccounts topic type.</span></span>

### <span data-ttu-id="91b3f-115">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="91b3f-115">Example 3</span></span>
```
PS C:\> Get-AzureRmEventGridTopicType -Name "Microsoft.Storage.StorageAccounts" -IncludeEventTypeData
```

<span data-ttu-id="91b3f-116">Storageaccounts konu türüyle ilgili bilgileri, StorageAccounts tarafından desteklenen olay türleriyle birlikte alır.</span><span class="sxs-lookup"><span data-stu-id="91b3f-116">Gets information about the StorageAccounts topic type, including the event types supported by StorageAccounts.</span></span>

## <span data-ttu-id="91b3f-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="91b3f-117">PARAMETERS</span></span>

### <span data-ttu-id="91b3f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91b3f-118">-DefaultProfile</span></span>
<span data-ttu-id="91b3f-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="91b3f-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="91b3f-120">-Includeeventtypedata</span><span class="sxs-lookup"><span data-stu-id="91b3f-120">-IncludeEventTypeData</span></span>
<span data-ttu-id="91b3f-121">Belirtilmişse, yanıt bir konu türü tarafından desteklenen olay türlerini içerecektir.</span><span class="sxs-lookup"><span data-stu-id="91b3f-121">If specified, the response will include the event types supported by a topic type.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91b3f-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="91b3f-122">-Name</span></span>
<span data-ttu-id="91b3f-123">EventGrid konu türü adı.</span><span class="sxs-lookup"><span data-stu-id="91b3f-123">EventGrid Topic Type Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91b3f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91b3f-124">CommonParameters</span></span>
<span data-ttu-id="91b3f-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="91b3f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91b3f-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="91b3f-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91b3f-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="91b3f-127">INPUTS</span></span>

### <span data-ttu-id="91b3f-128">System. String</span><span class="sxs-lookup"><span data-stu-id="91b3f-128">System.String</span></span>
<span data-ttu-id="91b3f-129">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="91b3f-129">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="91b3f-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="91b3f-130">OUTPUTS</span></span>

### <span data-ttu-id="91b3f-131">System. koleksiyonları. Generic. LIST ' 1 [[Microsoft. Azure. Commands. EventGrid. modeller. Pstopictypeınfolistınstance, Microsoft. Azure. Commands. EventGrid, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="91b3f-131">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.EventGrid.Models.PSTopicTypeInfoListInstance, Microsoft.Azure.Commands.EventGrid, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="91b3f-132">Microsoft. Azure. Commands. EventGrid. modeller. Pstopictypeınfo</span><span class="sxs-lookup"><span data-stu-id="91b3f-132">Microsoft.Azure.Commands.EventGrid.Models.PSTopicTypeInfo</span></span>

## <span data-ttu-id="91b3f-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="91b3f-133">NOTES</span></span>

## <span data-ttu-id="91b3f-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="91b3f-134">RELATED LINKS</span></span>

