---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: ba118c80656676c47a2d6740ef7c0266fd491af6
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/15/2020
ms.locfileid: "93934893"
---
# <span data-ttu-id="1772d-101">New-SubscriptionObject</span><span class="sxs-lookup"><span data-stu-id="1772d-101">New-SubscriptionObject</span></span>

## <span data-ttu-id="1772d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1772d-102">SYNOPSIS</span></span>
<span data-ttu-id="1772d-103">Desteklenen işlemlerin listesi.</span><span class="sxs-lookup"><span data-stu-id="1772d-103">List of supported operations.</span></span>

## <span data-ttu-id="1772d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1772d-104">SYNTAX</span></span>

```
New-SubscriptionObject [[-TenantId] <String>] [[-SubscriptionId] <String>] [[-DisplayName] <String>]
 [[-DelegatedProviderSubscriptionId] <String>] [[-Name] <String>] [[-Owner] <String>]
 [[-RoutingResourceManagerType] <String>] [[-ExternalReferenceId] <String>] [[-State] <String>]
 [[-Id] <String>] [[-OfferId] <String>] [<CommonParameters>]
```

## <span data-ttu-id="1772d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="1772d-105">DESCRIPTION</span></span>
<span data-ttu-id="1772d-106">Desteklenen işlemlerin listesi.</span><span class="sxs-lookup"><span data-stu-id="1772d-106">List of supported operations.</span></span>

## <span data-ttu-id="1772d-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1772d-107">EXAMPLES</span></span>

### <span data-ttu-id="1772d-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="1772d-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="1772d-109">{{Buraya örnek açıklama ekleyin}}</span><span class="sxs-lookup"><span data-stu-id="1772d-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="1772d-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1772d-110">PARAMETERS</span></span>

### <span data-ttu-id="1772d-111">-Delegatevseçprovidersubscriptionıd</span><span class="sxs-lookup"><span data-stu-id="1772d-111">-DelegatedProviderSubscriptionId</span></span>
<span data-ttu-id="1772d-112">Üst temsilci abonelik tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="1772d-112">Parent DelegatedProvider subscription identifier.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1772d-113">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="1772d-113">-DisplayName</span></span>
<span data-ttu-id="1772d-114">Abonelik adı.</span><span class="sxs-lookup"><span data-stu-id="1772d-114">Subscription name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1772d-115">-Externalreferenceıd</span><span class="sxs-lookup"><span data-stu-id="1772d-115">-ExternalReferenceId</span></span>
<span data-ttu-id="1772d-116">Dış başvuru tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="1772d-116">External reference identifier.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1772d-117">-ID</span><span class="sxs-lookup"><span data-stu-id="1772d-117">-Id</span></span>
<span data-ttu-id="1772d-118">Tam nitelikli tanımlayıcı.</span><span class="sxs-lookup"><span data-stu-id="1772d-118">Fully qualified identifier.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1772d-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="1772d-119">-Name</span></span>
<span data-ttu-id="1772d-120">Kaynağın adı.</span><span class="sxs-lookup"><span data-stu-id="1772d-120">Name of the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1772d-121">-OfferId</span><span class="sxs-lookup"><span data-stu-id="1772d-121">-OfferId</span></span>
<span data-ttu-id="1772d-122">Temsilci sağlayıcı kapsamı altındaki teklifin tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="1772d-122">Identifier of the offer under the scope of a delegated provider.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 11
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1772d-123">-Sahip</span><span class="sxs-lookup"><span data-stu-id="1772d-123">-Owner</span></span>
<span data-ttu-id="1772d-124">Abonelik sahibi.</span><span class="sxs-lookup"><span data-stu-id="1772d-124">Subscription owner.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1772d-125">-RoutingResourceManagerType</span><span class="sxs-lookup"><span data-stu-id="1772d-125">-RoutingResourceManagerType</span></span>
<span data-ttu-id="1772d-126">Yönlendirme Kaynak Yöneticisi türü.</span><span class="sxs-lookup"><span data-stu-id="1772d-126">Routing resource manager type.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1772d-127">Durumlu</span><span class="sxs-lookup"><span data-stu-id="1772d-127">-State</span></span>
<span data-ttu-id="1772d-128">Abonelik durumu.</span><span class="sxs-lookup"><span data-stu-id="1772d-128">Subscription state.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1772d-129">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="1772d-129">-SubscriptionId</span></span>
<span data-ttu-id="1772d-130">Abonelik tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="1772d-130">Subscription identifier.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1772d-131">-Tenantıd</span><span class="sxs-lookup"><span data-stu-id="1772d-131">-TenantId</span></span>
<span data-ttu-id="1772d-132">Dizin kiracı tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="1772d-132">Directory tenant identifier.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1772d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1772d-133">CommonParameters</span></span>
<span data-ttu-id="1772d-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1772d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1772d-135">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1772d-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1772d-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1772d-136">INPUTS</span></span>

## <span data-ttu-id="1772d-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1772d-137">OUTPUTS</span></span>

## <span data-ttu-id="1772d-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1772d-138">NOTES</span></span>

## <span data-ttu-id="1772d-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1772d-139">RELATED LINKS</span></span>

