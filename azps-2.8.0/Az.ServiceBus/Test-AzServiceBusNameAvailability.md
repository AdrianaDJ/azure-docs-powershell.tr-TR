---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/test-azservicebusnameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Test-AzServiceBusNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Test-AzServiceBusNameAvailability.md
ms.openlocfilehash: 396a328de8c075b49ae4dda181158c33518eaa8a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93932442"
---
# <span data-ttu-id="56064-101">Test-AzServiceBusNameAvailability</span><span class="sxs-lookup"><span data-stu-id="56064-101">Test-AzServiceBusNameAvailability</span></span>

## <span data-ttu-id="56064-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="56064-102">SYNOPSIS</span></span>
<span data-ttu-id="56064-103">Verilen sıra veya konu adının uygunluk durumunu denetler</span><span class="sxs-lookup"><span data-stu-id="56064-103">Checks the Availability of the given Queue or Topic name</span></span>

## <span data-ttu-id="56064-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="56064-104">SYNTAX</span></span>

### <span data-ttu-id="56064-105">Queuechecknamekullanılabilirlik (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="56064-105">QueueCheckNameAvailabilitySet (Default)</span></span>
```
Test-AzServiceBusNameAvailability [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-Queue]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="56064-106">Topicchecknamekullanılabilirliği Bilityset</span><span class="sxs-lookup"><span data-stu-id="56064-106">TopicCheckNameAvailabilitySet</span></span>
```
Test-AzServiceBusNameAvailability [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-Topic]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="56064-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="56064-107">DESCRIPTION</span></span>
<span data-ttu-id="56064-108">**Test-Azhizmetibusnameuygunluk** cmdlet 'i</span><span class="sxs-lookup"><span data-stu-id="56064-108">The **Test-AzServiceBusNameAvailability** Cmdlet Check Availability of the provided Name of Queue or Topic</span></span>

## <span data-ttu-id="56064-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="56064-109">EXAMPLES</span></span>

### <span data-ttu-id="56064-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="56064-110">Example 1</span></span>
```powershell
Test-AzServiceBusNameAvailability -ResourceGroupName $resourceGroupName -Namespace $namespaceName -Name $nameQueue -Queue
True
```

<span data-ttu-id="56064-111">Sağlanan $nameQueue adı availabile veya sağlanan $nameQueue adı sağlanmadıysa yanlış değerini döndürür</span><span class="sxs-lookup"><span data-stu-id="56064-111">Returns True if the Provided $nameQueue name is Availabile or returns False if Provided $nameQueue name in not available</span></span>

### <span data-ttu-id="56064-112">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="56064-112">Example 2</span></span>
```powershell
Test-AzServiceBusNameAvailability -ResourceGroupName $resourceGroupName -Namespace $namespaceName -Name $nameTopic -Topic
True
```

<span data-ttu-id="56064-113">Sağlanan $nameTopic adı availabile veya sağlanan $nameTopic adı sağlanmadıysa yanlış değerini döndürür</span><span class="sxs-lookup"><span data-stu-id="56064-113">Returns True if the Provided $nameTopic name is Availabile or returns False if Provided $nameTopic name in not available</span></span>

## <span data-ttu-id="56064-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="56064-114">PARAMETERS</span></span>

### <span data-ttu-id="56064-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56064-115">-DefaultProfile</span></span>
<span data-ttu-id="56064-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="56064-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="56064-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="56064-117">-Name</span></span>
<span data-ttu-id="56064-118">Ad kullanılabilirliğini denetlemek için sıra adı</span><span class="sxs-lookup"><span data-stu-id="56064-118">Queue Name to check the Name Availability</span></span>

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

### <span data-ttu-id="56064-119">-Namespace</span><span class="sxs-lookup"><span data-stu-id="56064-119">-Namespace</span></span>
<span data-ttu-id="56064-120">ServiceBus ad alanı adı</span><span class="sxs-lookup"><span data-stu-id="56064-120">Servicebus Namespace Name</span></span>

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

### <span data-ttu-id="56064-121">-Sıra</span><span class="sxs-lookup"><span data-stu-id="56064-121">-Queue</span></span>
<span data-ttu-id="56064-122">Sıra adının adını denetleme</span><span class="sxs-lookup"><span data-stu-id="56064-122">To Check Name Availability for Queue Name</span></span>

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

### <span data-ttu-id="56064-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56064-123">-ResourceGroupName</span></span>
<span data-ttu-id="56064-124">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="56064-124">Resource Group Name</span></span>

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

### <span data-ttu-id="56064-125">-Konu</span><span class="sxs-lookup"><span data-stu-id="56064-125">-Topic</span></span>
<span data-ttu-id="56064-126">Konu adının adını denetleme</span><span class="sxs-lookup"><span data-stu-id="56064-126">To Check Name Availability for Topic Name</span></span>

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

### <span data-ttu-id="56064-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56064-127">CommonParameters</span></span>
<span data-ttu-id="56064-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="56064-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="56064-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="56064-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56064-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="56064-130">INPUTS</span></span>

### <span data-ttu-id="56064-131">System. String</span><span class="sxs-lookup"><span data-stu-id="56064-131">System.String</span></span>

## <span data-ttu-id="56064-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="56064-132">OUTPUTS</span></span>

### <span data-ttu-id="56064-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="56064-133">System.Boolean</span></span>

## <span data-ttu-id="56064-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="56064-134">NOTES</span></span>

## <span data-ttu-id="56064-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="56064-135">RELATED LINKS</span></span>