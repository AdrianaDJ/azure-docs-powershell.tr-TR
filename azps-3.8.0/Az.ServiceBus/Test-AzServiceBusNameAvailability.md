---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/test-azservicebusnameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Test-AzServiceBusNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Test-AzServiceBusNameAvailability.md
ms.openlocfilehash: adaf7485b0af16821a1f4adec7919422bef07f90
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096360"
---
# <span data-ttu-id="9af29-101">Test-AzServiceBusNameAvailability</span><span class="sxs-lookup"><span data-stu-id="9af29-101">Test-AzServiceBusNameAvailability</span></span>

## <span data-ttu-id="9af29-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9af29-102">SYNOPSIS</span></span>
<span data-ttu-id="9af29-103">Verilen sıra veya konu adının uygunluk durumunu denetler</span><span class="sxs-lookup"><span data-stu-id="9af29-103">Checks the Availability of the given Queue or Topic name</span></span>

## <span data-ttu-id="9af29-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9af29-104">SYNTAX</span></span>

### <span data-ttu-id="9af29-105">Queuechecknamekullanılabilirlik (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="9af29-105">QueueCheckNameAvailabilitySet (Default)</span></span>
```
Test-AzServiceBusNameAvailability [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-Queue]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9af29-106">Topicchecknamekullanılabilirliği Bilityset</span><span class="sxs-lookup"><span data-stu-id="9af29-106">TopicCheckNameAvailabilitySet</span></span>
```
Test-AzServiceBusNameAvailability [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-Topic]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9af29-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="9af29-107">DESCRIPTION</span></span>
<span data-ttu-id="9af29-108">**Test-Azhizmetibusnameuygunluk** cmdlet 'i</span><span class="sxs-lookup"><span data-stu-id="9af29-108">The **Test-AzServiceBusNameAvailability** Cmdlet Check Availability of the provided Name of Queue or Topic</span></span>

## <span data-ttu-id="9af29-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9af29-109">EXAMPLES</span></span>

### <span data-ttu-id="9af29-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="9af29-110">Example 1</span></span>
```powershell
Test-AzServiceBusNameAvailability -ResourceGroupName $resourceGroupName -Namespace $namespaceName -Name $nameQueue -Queue
True
```

<span data-ttu-id="9af29-111">Sağlanan $nameQueue adı availabile veya sağlanan $nameQueue adı sağlanmadıysa yanlış değerini döndürür</span><span class="sxs-lookup"><span data-stu-id="9af29-111">Returns True if the Provided $nameQueue name is Availabile or returns False if Provided $nameQueue name in not available</span></span>

### <span data-ttu-id="9af29-112">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="9af29-112">Example 2</span></span>
```powershell
Test-AzServiceBusNameAvailability -ResourceGroupName $resourceGroupName -Namespace $namespaceName -Name $nameTopic -Topic
True
```

<span data-ttu-id="9af29-113">Sağlanan $nameTopic adı availabile veya sağlanan $nameTopic adı sağlanmadıysa yanlış değerini döndürür</span><span class="sxs-lookup"><span data-stu-id="9af29-113">Returns True if the Provided $nameTopic name is Availabile or returns False if Provided $nameTopic name in not available</span></span>

## <span data-ttu-id="9af29-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9af29-114">PARAMETERS</span></span>

### <span data-ttu-id="9af29-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9af29-115">-DefaultProfile</span></span>
<span data-ttu-id="9af29-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9af29-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9af29-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="9af29-117">-Name</span></span>
<span data-ttu-id="9af29-118">Ad kullanılabilirliğini denetlemek için sıra adı</span><span class="sxs-lookup"><span data-stu-id="9af29-118">Queue Name to check the Name Availability</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9af29-119">-Namespace</span><span class="sxs-lookup"><span data-stu-id="9af29-119">-Namespace</span></span>
<span data-ttu-id="9af29-120">ServiceBus ad alanı adı</span><span class="sxs-lookup"><span data-stu-id="9af29-120">Servicebus Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9af29-121">-Sıra</span><span class="sxs-lookup"><span data-stu-id="9af29-121">-Queue</span></span>
<span data-ttu-id="9af29-122">Sıra adının adını denetleme</span><span class="sxs-lookup"><span data-stu-id="9af29-122">To Check Name Availability for Queue Name</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: QueueCheckNameAvailabilitySet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9af29-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9af29-123">-ResourceGroupName</span></span>
<span data-ttu-id="9af29-124">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="9af29-124">Resource Group Name</span></span>

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

### <span data-ttu-id="9af29-125">-Konu</span><span class="sxs-lookup"><span data-stu-id="9af29-125">-Topic</span></span>
<span data-ttu-id="9af29-126">Konu adının adını denetleme</span><span class="sxs-lookup"><span data-stu-id="9af29-126">To Check Name Availability for Topic Name</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: TopicCheckNameAvailabilitySet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9af29-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9af29-127">CommonParameters</span></span>
<span data-ttu-id="9af29-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9af29-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="9af29-129">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9af29-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9af29-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9af29-130">INPUTS</span></span>

### <span data-ttu-id="9af29-131">System. String</span><span class="sxs-lookup"><span data-stu-id="9af29-131">System.String</span></span>

## <span data-ttu-id="9af29-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9af29-132">OUTPUTS</span></span>

### <span data-ttu-id="9af29-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9af29-133">System.Boolean</span></span>

## <span data-ttu-id="9af29-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9af29-134">NOTES</span></span>

## <span data-ttu-id="9af29-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9af29-135">RELATED LINKS</span></span>
