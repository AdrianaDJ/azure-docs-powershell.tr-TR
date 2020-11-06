---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusQueueKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusQueueKey.md
ms.openlocfilehash: 4faca15a0c348ee1011789db5acd227c06ee1b85
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593003"
---
# <span data-ttu-id="e9778-101">Get-AzureRmServiceBusQueueKey</span><span class="sxs-lookup"><span data-stu-id="e9778-101">Get-AzureRmServiceBusQueueKey</span></span>

## <span data-ttu-id="e9778-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e9778-102">SYNOPSIS</span></span>
<span data-ttu-id="e9778-103">Verilen hizmet veri yolu kuyruğu için birincil ve ikincil bağlantı dizelerini alır.</span><span class="sxs-lookup"><span data-stu-id="e9778-103">Gets the primary and secondary connection strings for the given Service Bus queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e9778-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e9778-104">SYNTAX</span></span>

```
Get-AzureRmServiceBusQueueKey [-ResourceGroup] <String> -Namespace <String> -Queue <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e9778-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e9778-105">DESCRIPTION</span></span>
<span data-ttu-id="e9778-106">**Get-AzureRmServiceBusQueueKey** cmdlet 'i, verilen hizmet veri yolu kuyruğu için birincil ve ikincil bağlantı dizelerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="e9778-106">The **Get-AzureRmServiceBusQueueKey** cmdlet returns the primary and secondary connection strings for the given Service Bus queue.</span></span> 

## <span data-ttu-id="e9778-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e9778-107">EXAMPLES</span></span>

### <span data-ttu-id="e9778-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="e9778-108">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusQueueKey -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_exampl1 -AuthorizationRuleName SBAuthoRule1
```

<span data-ttu-id="e9778-109">Belirtilen hizmet veri yolu kuyruğu için birincil ve ikincil bağlantı dizelerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="e9778-109">Returns the primary and secondary connection strings for the specified Service Bus queue.</span></span>

## <span data-ttu-id="e9778-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e9778-110">PARAMETERS</span></span>

### <span data-ttu-id="e9778-111">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="e9778-111">-ResourceGroup</span></span>
<span data-ttu-id="e9778-112">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="e9778-112">The name of the resource group.</span></span>

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

### <span data-ttu-id="e9778-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9778-113">-DefaultProfile</span></span>
<span data-ttu-id="e9778-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e9778-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e9778-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="e9778-115">-Name</span></span>
<span data-ttu-id="e9778-116">ServiceBus kuyruğu AuthorizationRule adı.</span><span class="sxs-lookup"><span data-stu-id="e9778-116">ServiceBus Queue AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="e9778-117">-Namespace</span><span class="sxs-lookup"><span data-stu-id="e9778-117">-Namespace</span></span>
<span data-ttu-id="e9778-118">ServiceBus ad alanı adı.</span><span class="sxs-lookup"><span data-stu-id="e9778-118">ServiceBus Namespace Name.</span></span>

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

### <span data-ttu-id="e9778-119">-Sıra</span><span class="sxs-lookup"><span data-stu-id="e9778-119">-Queue</span></span>
<span data-ttu-id="e9778-120">ServiceBus sıra adı.</span><span class="sxs-lookup"><span data-stu-id="e9778-120">ServiceBus Queue Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: QueueName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e9778-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9778-121">CommonParameters</span></span>
<span data-ttu-id="e9778-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e9778-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9778-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e9778-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9778-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e9778-124">INPUTS</span></span>

### <span data-ttu-id="e9778-125">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="e9778-125">-ResourceGroup</span></span>
 <span data-ttu-id="e9778-126">System. String</span><span class="sxs-lookup"><span data-stu-id="e9778-126">System.String</span></span>
 

### <span data-ttu-id="e9778-127">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="e9778-127">-NamespaceName</span></span>
 <span data-ttu-id="e9778-128">System. String</span><span class="sxs-lookup"><span data-stu-id="e9778-128">System.String</span></span>
 

### <span data-ttu-id="e9778-129">-SıraAdı</span><span class="sxs-lookup"><span data-stu-id="e9778-129">-QueueName</span></span>
 <span data-ttu-id="e9778-130">System. String</span><span class="sxs-lookup"><span data-stu-id="e9778-130">System.String</span></span>
 

### <span data-ttu-id="e9778-131">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="e9778-131">-AuthorizationRuleName</span></span>
 <span data-ttu-id="e9778-132">System. String</span><span class="sxs-lookup"><span data-stu-id="e9778-132">System.String</span></span>

## <span data-ttu-id="e9778-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e9778-133">OUTPUTS</span></span>

### <span data-ttu-id="e9778-134">Microsoft. Azure. Commands. ServiceBus. modeller. ListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="e9778-134">Microsoft.Azure.Commands.ServiceBus.Models.ListKeysAttributes</span></span>
<span data-ttu-id="e9778-135">PrimaryConnectionString: Endpoint = SB://SB-example1.ServiceBus.Windows.net/; SharedAccessKeyName = SBAuthoRule1; SharedAccessKey = {SharedAccessKey-Value}; EntityPath = SB-Queue_e xampl1 SecondaryConnectionString: Endpoint = SB://SB-example1.ServiceBus.Windows.net/; SharedAccessKeyName = SBAuthoRule1; SharedAccessKey = {SharedAccessKey-Value}; EntityPath = SB-Queue_e xampl1 PrimaryKey: {PrimaryKey değeri} SecondaryKey: {SecondaryKey Value} AnahtarAdı: SBAuthoRule1</span><span class="sxs-lookup"><span data-stu-id="e9778-135">PrimaryConnectionString   : Endpoint=sb://sb-example1.servicebus.windows.net/;SharedAccessKeyName=SBAuthoRule1;SharedAccessKey={SharedAccessKey-value};EntityPath=SB-Queue_e xampl1 SecondaryConnectionString : Endpoint=sb://sb-example1.servicebus.windows.net/;SharedAccessKeyName=SBAuthoRule1;SharedAccessKey={SharedAccessKey-value};EntityPath=SB-Queue_e xampl1 PrimaryKey                : {PrimaryKey value} SecondaryKey              : {SecondaryKey value} KeyName                   : SBAuthoRule1</span></span>

## <span data-ttu-id="e9778-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e9778-136">NOTES</span></span>

## <span data-ttu-id="e9778-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e9778-137">RELATED LINKS</span></span>

