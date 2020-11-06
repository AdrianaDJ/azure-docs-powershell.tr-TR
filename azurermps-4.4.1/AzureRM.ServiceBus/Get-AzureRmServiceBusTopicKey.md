---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusTopicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusTopicKey.md
ms.openlocfilehash: 24041c299f2f242126f265ad232db3e0c5d526b0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593801"
---
# <span data-ttu-id="7dc5f-101">Get-AzureRmServiceBusTopicKey</span><span class="sxs-lookup"><span data-stu-id="7dc5f-101">Get-AzureRmServiceBusTopicKey</span></span>

## <span data-ttu-id="7dc5f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7dc5f-102">SYNOPSIS</span></span>
<span data-ttu-id="7dc5f-103">Service Bus konusu için birincil ve ikincil bağlantı dizelerini alır.</span><span class="sxs-lookup"><span data-stu-id="7dc5f-103">Gets the primary and secondary connection strings for the Service Bus topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7dc5f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7dc5f-104">SYNTAX</span></span>

```
Get-AzureRmServiceBusTopicKey [-ResourceGroup] <String> -Namespace <String> -Topic <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7dc5f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="7dc5f-105">DESCRIPTION</span></span>
<span data-ttu-id="7dc5f-106">**Get-AzureRmServiceBusTopicKey** cmdlet 'i, verilen hizmet veri yolu konusu için birincil ve ikincil bağlantı dizelerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="7dc5f-106">The **Get-AzureRmServiceBusTopicKey** cmdlet returns the primary and secondary connection strings for the given Service Bus topic.</span></span>

## <span data-ttu-id="7dc5f-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7dc5f-107">EXAMPLES</span></span>

### <span data-ttu-id="7dc5f-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="7dc5f-108">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusTopicKey -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -AuthorizationRuleName SBTopicAuthoRule1
```

<span data-ttu-id="7dc5f-109">Belirtilen hizmet veri yolu konusu için birincil ve ikincil bağlantı dizelerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="7dc5f-109">Returns the primary and secondary connection strings for the specified Service Bus topic.</span></span>

## <span data-ttu-id="7dc5f-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7dc5f-110">PARAMETERS</span></span>

### <span data-ttu-id="7dc5f-111">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="7dc5f-111">-ResourceGroup</span></span>
<span data-ttu-id="7dc5f-112">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="7dc5f-112">The name of the resource group.</span></span>

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

### <span data-ttu-id="7dc5f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7dc5f-113">-DefaultProfile</span></span>
<span data-ttu-id="7dc5f-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7dc5f-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7dc5f-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="7dc5f-115">-Name</span></span>
<span data-ttu-id="7dc5f-116">Konu AuthorizationRule adı.</span><span class="sxs-lookup"><span data-stu-id="7dc5f-116">Topic AuthorizationRule Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7dc5f-117">-Namespace</span><span class="sxs-lookup"><span data-stu-id="7dc5f-117">-Namespace</span></span>
<span data-ttu-id="7dc5f-118">Ad alanı adı.</span><span class="sxs-lookup"><span data-stu-id="7dc5f-118">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7dc5f-119">-Konu</span><span class="sxs-lookup"><span data-stu-id="7dc5f-119">-Topic</span></span>
<span data-ttu-id="7dc5f-120">Konu adı.</span><span class="sxs-lookup"><span data-stu-id="7dc5f-120">Topic Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7dc5f-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7dc5f-121">CommonParameters</span></span>
<span data-ttu-id="7dc5f-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7dc5f-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7dc5f-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7dc5f-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7dc5f-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7dc5f-124">INPUTS</span></span>

### <span data-ttu-id="7dc5f-125">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="7dc5f-125">-ResourceGroup</span></span>
 <span data-ttu-id="7dc5f-126">System. String</span><span class="sxs-lookup"><span data-stu-id="7dc5f-126">System.String</span></span>
 

### <span data-ttu-id="7dc5f-127">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="7dc5f-127">-NamespaceName</span></span>
 <span data-ttu-id="7dc5f-128">System. String</span><span class="sxs-lookup"><span data-stu-id="7dc5f-128">System.String</span></span>
 

### <span data-ttu-id="7dc5f-129">-TopicName</span><span class="sxs-lookup"><span data-stu-id="7dc5f-129">-TopicName</span></span>
 <span data-ttu-id="7dc5f-130">System. String</span><span class="sxs-lookup"><span data-stu-id="7dc5f-130">System.String</span></span>
 

### <span data-ttu-id="7dc5f-131">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="7dc5f-131">-AuthorizationRuleName</span></span>
 <span data-ttu-id="7dc5f-132">System. String</span><span class="sxs-lookup"><span data-stu-id="7dc5f-132">System.String</span></span>

## <span data-ttu-id="7dc5f-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7dc5f-133">OUTPUTS</span></span>

### <span data-ttu-id="7dc5f-134">Microsoft. Azure. Commands. ServiceBus. modeller. ListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="7dc5f-134">Microsoft.Azure.Commands.ServiceBus.Models.ListKeysAttributes</span></span>
<span data-ttu-id="7dc5f-135">PrimaryConnectionString: Endpoint = SB://SB-example1.ServiceBus.Windows.net/; SharedAccessKeyName = SBTopicAuthoRule1; SharedAccessKey = {SharedAccessKey-Value}; EntityPath = SB-to pic_exampl1 SecondaryConnectionString: Endpoint = SB://SB-example1.ServiceBus.Windows.net/; SharedAccessKeyName = SBTopicAuthoRule1; SharedAccessKey = {SharedAccessKey-Value}; EntityPath = SB-to pic_exampl1 PrimaryKey: {PrimaryKey değeri} SecondaryKey: {SecondaryKey Value} AnahtarAdı: SBTopicAuthoRule1</span><span class="sxs-lookup"><span data-stu-id="7dc5f-135">PrimaryConnectionString   : Endpoint=sb://sb-example1.servicebus.windows.net/;SharedAccessKeyName=SBTopicAuthoRule1;SharedAccessKey={SharedAccessKey-value};EntityPath=SB-To pic_exampl1 SecondaryConnectionString : Endpoint=sb://sb-example1.servicebus.windows.net/;SharedAccessKeyName=SBTopicAuthoRule1;SharedAccessKey={SharedAccessKey-value};EntityPath=SB-To pic_exampl1 PrimaryKey                : {PrimaryKey value} SecondaryKey              : {SecondaryKey value} KeyName                   : SBTopicAuthoRule1</span></span>

## <span data-ttu-id="7dc5f-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7dc5f-136">NOTES</span></span>

## <span data-ttu-id="7dc5f-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7dc5f-137">RELATED LINKS</span></span>

