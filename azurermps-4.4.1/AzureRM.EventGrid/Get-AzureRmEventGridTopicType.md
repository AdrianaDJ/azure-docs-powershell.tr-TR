---
external help file: Microsoft.Azure.Commands.EventGrid.dll-Help.xml
Module Name: AzureRM.EventGrid
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Get-AzureRmEventGridTopicType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Get-AzureRmEventGridTopicType.md
ms.openlocfilehash: 621fb15d3a83b7c704e5828d6541ad9d4404875c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593133"
---
# <span data-ttu-id="eef19-101">Get-AzureRmEventGridTopicType</span><span class="sxs-lookup"><span data-stu-id="eef19-101">Get-AzureRmEventGridTopicType</span></span>

## <span data-ttu-id="eef19-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eef19-102">SYNOPSIS</span></span>
<span data-ttu-id="eef19-103">Azure olay Kılavuzu tarafından desteklenen konu türleriyle ilgili ayrıntıları alır.</span><span class="sxs-lookup"><span data-stu-id="eef19-103">Gets the details about the topic types supported by Azure Event Grid.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eef19-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="eef19-104">SYNTAX</span></span>

```
Get-AzureRmEventGridTopicType [[-Name] <String>] [-IncludeEventTypeData]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eef19-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="eef19-105">DESCRIPTION</span></span>
<span data-ttu-id="eef19-106">Azure olay Kılavuzu tarafından desteklenen konu türlerinin ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="eef19-106">Gets the details of topic types supported by Azure Event Grid.</span></span>
<span data-ttu-id="eef19-107">Konu türü adı belirtilmişse, bu konu türüyle ilgili Ayrıntılar döndürülür.</span><span class="sxs-lookup"><span data-stu-id="eef19-107">If a topic type name is specified, details about that topic type are returned.</span></span>
<span data-ttu-id="eef19-108">Konu türü adı belirtilmezse, tüm konu türleriyle ilgili ayrıntılar verilir.</span><span class="sxs-lookup"><span data-stu-id="eef19-108">If a topic type name is not specified, details about all topic types are returned.</span></span>
<span data-ttu-id="eef19-109">Includeeventtypes belirtildiğinde, her konu türü tarafından desteklenen olay türleriyle ilgili bilgiler yanıta dahildir.</span><span class="sxs-lookup"><span data-stu-id="eef19-109">If IncludeEventTypes is specified, information about event types supported by each topic type is included in the response.</span></span>

## <span data-ttu-id="eef19-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="eef19-110">EXAMPLES</span></span>

### <span data-ttu-id="eef19-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="eef19-111">Example 1</span></span>
```
PS C:\> Get-AzureRmEventGridTopicType
```

<span data-ttu-id="eef19-112">Konu türlerinin bir listesini alır.</span><span class="sxs-lookup"><span data-stu-id="eef19-112">Gets a list of the topic types.</span></span>

### <span data-ttu-id="eef19-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="eef19-113">Example 2</span></span>
```
PS C:\> Get-AzureRmEventGridTopicType -Name "Microsoft.Storage.StorageAccounts"
```

<span data-ttu-id="eef19-114">StorageAccounts konu türü hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="eef19-114">Gets information about the StorageAccounts topic type.</span></span>

### <span data-ttu-id="eef19-115">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="eef19-115">Example 3</span></span>
```
PS C:\> Get-AzureRmEventGridTopicType -Name "Microsoft.Storage.StorageAccounts" -IncludeEventTypeData
```

<span data-ttu-id="eef19-116">Storageaccounts konu türüyle ilgili bilgileri, StorageAccounts tarafından desteklenen olay türleriyle birlikte alır.</span><span class="sxs-lookup"><span data-stu-id="eef19-116">Gets information about the StorageAccounts topic type, including the event types supported by StorageAccounts.</span></span>

## <span data-ttu-id="eef19-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="eef19-117">PARAMETERS</span></span>

### <span data-ttu-id="eef19-118">-Includeeventtypedata</span><span class="sxs-lookup"><span data-stu-id="eef19-118">-IncludeEventTypeData</span></span>
<span data-ttu-id="eef19-119">Belirtilmişse, yanıt bir konu türü tarafından desteklenen olay türlerini içerecektir.</span><span class="sxs-lookup"><span data-stu-id="eef19-119">If specified, the response will include the event types supported by a topic type.</span></span>

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

### <span data-ttu-id="eef19-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="eef19-120">-Name</span></span>
<span data-ttu-id="eef19-121">EventGrid konu türü adı.</span><span class="sxs-lookup"><span data-stu-id="eef19-121">EventGrid Topic Type Name.</span></span>

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

### <span data-ttu-id="eef19-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eef19-122">-DefaultProfile</span></span>
<span data-ttu-id="eef19-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="eef19-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eef19-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eef19-124">CommonParameters</span></span>
<span data-ttu-id="eef19-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="eef19-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eef19-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eef19-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eef19-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="eef19-127">INPUTS</span></span>

### <span data-ttu-id="eef19-128">System. String</span><span class="sxs-lookup"><span data-stu-id="eef19-128">System.String</span></span>
<span data-ttu-id="eef19-129">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="eef19-129">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="eef19-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="eef19-130">OUTPUTS</span></span>

### <span data-ttu-id="eef19-131">System. koleksiyonları. Generic. LIST ' 1 [[Microsoft. Azure. Commands. EventGrid. modeller. Pstopictypeınfolistınstance, Microsoft. Azure. Commands. EventGrid, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="eef19-131">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.EventGrid.Models.PSTopicTypeInfoListInstance, Microsoft.Azure.Commands.EventGrid, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="eef19-132">Microsoft. Azure. Commands. EventGrid. modeller. Pstopictypeınfo</span><span class="sxs-lookup"><span data-stu-id="eef19-132">Microsoft.Azure.Commands.EventGrid.Models.PSTopicTypeInfo</span></span>

## <span data-ttu-id="eef19-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="eef19-133">NOTES</span></span>

## <span data-ttu-id="eef19-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="eef19-134">RELATED LINKS</span></span>

