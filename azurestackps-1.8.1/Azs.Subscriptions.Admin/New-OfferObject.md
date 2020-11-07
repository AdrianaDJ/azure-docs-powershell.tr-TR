---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5526ccd8fe050f9aa81974c8ea4ae1872125c087
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/15/2020
ms.locfileid: "93934907"
---
# <span data-ttu-id="669ed-101">New-OfferObject</span><span class="sxs-lookup"><span data-stu-id="669ed-101">New-OfferObject</span></span>

## <span data-ttu-id="669ed-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="669ed-102">SYNOPSIS</span></span>
<span data-ttu-id="669ed-103">Aboneliğin oluşturulabildiği hizmet sunumunu temsil eder.</span><span class="sxs-lookup"><span data-stu-id="669ed-103">Represents an offering of services against which a subscription can be created.</span></span>

## <span data-ttu-id="669ed-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="669ed-104">SYNTAX</span></span>

```
New-OfferObject [[-Tags] <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [[-Type] <String>] [[-MaxSubscriptionsPerAccount] <Int64>] [[-Name] <String>] [[-BasePlanIds] <String[]>]
 [[-DisplayName] <String>] [[-Description] <String>] [[-ExternalReferenceId] <String>] [[-State] <String>]
 [[-Id] <String>] [[-Location] <String>] [[-SubscriptionCount] <Int64>]
 [[-AddonPlanDefinition] <AddonPlanDefinition[]>] [<CommonParameters>]
```

## <span data-ttu-id="669ed-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="669ed-105">DESCRIPTION</span></span>
<span data-ttu-id="669ed-106">Aboneliğin oluşturulabildiği hizmet sunumunu temsil eder.</span><span class="sxs-lookup"><span data-stu-id="669ed-106">Represents an offering of services against which a subscription can be created.</span></span>

## <span data-ttu-id="669ed-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="669ed-107">EXAMPLES</span></span>

### <span data-ttu-id="669ed-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="669ed-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="669ed-109">{{Buraya örnek açıklama ekleyin}}</span><span class="sxs-lookup"><span data-stu-id="669ed-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="669ed-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="669ed-110">PARAMETERS</span></span>

### <span data-ttu-id="669ed-111">-Add</span><span class="sxs-lookup"><span data-stu-id="669ed-111">-AddonPlanDefinition</span></span>
<span data-ttu-id="669ed-112">Bir kiracının isteğe bağlı olarak teklifin bir parçası olarak edinebileceğiniz eklenti planlarına yönelik başvurular.</span><span class="sxs-lookup"><span data-stu-id="669ed-112">References to add-on plans that a tenant can optionally acquire as a part of the offer.</span></span>

```yaml
Type: AddonPlanDefinition[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 13
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="669ed-113">-Temelplankimlikleri</span><span class="sxs-lookup"><span data-stu-id="669ed-113">-BasePlanIds</span></span>
<span data-ttu-id="669ed-114">Kiracı teklife abone olduğunda kiracıya hemen sağlanan temel planların tanımlayıcıları.</span><span class="sxs-lookup"><span data-stu-id="669ed-114">Identifiers of the base plans that become available to the tenant immediately when a tenant subscribes to the offer.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="669ed-115">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="669ed-115">-Description</span></span>
<span data-ttu-id="669ed-116">Teklifin açıklaması.</span><span class="sxs-lookup"><span data-stu-id="669ed-116">Description of offer.</span></span>

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

### <span data-ttu-id="669ed-117">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="669ed-117">-DisplayName</span></span>
<span data-ttu-id="669ed-118">Teklifin adını görüntüler.</span><span class="sxs-lookup"><span data-stu-id="669ed-118">Display name of offer.</span></span>

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

### <span data-ttu-id="669ed-119">-Externalreferenceıd</span><span class="sxs-lookup"><span data-stu-id="669ed-119">-ExternalReferenceId</span></span>
<span data-ttu-id="669ed-120">Dış başvuru tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="669ed-120">External reference identifier.</span></span>

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

### <span data-ttu-id="669ed-121">-ID</span><span class="sxs-lookup"><span data-stu-id="669ed-121">-Id</span></span>
<span data-ttu-id="669ed-122">Kaynağın URI 'SI.</span><span class="sxs-lookup"><span data-stu-id="669ed-122">URI of the resource.</span></span>

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

### <span data-ttu-id="669ed-123">-Konum</span><span class="sxs-lookup"><span data-stu-id="669ed-123">-Location</span></span>
<span data-ttu-id="669ed-124">Kaynağın konum olduğu konum.</span><span class="sxs-lookup"><span data-stu-id="669ed-124">Location where resource is location.</span></span>

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

### <span data-ttu-id="669ed-125">-MaxSubscriptionsPerAccount</span><span class="sxs-lookup"><span data-stu-id="669ed-125">-MaxSubscriptionsPerAccount</span></span>
<span data-ttu-id="669ed-126">Hesap başına maksimum abonelik.</span><span class="sxs-lookup"><span data-stu-id="669ed-126">Maximum subscriptions per account.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="669ed-127">-Ad</span><span class="sxs-lookup"><span data-stu-id="669ed-127">-Name</span></span>
<span data-ttu-id="669ed-128">Kaynağın adı.</span><span class="sxs-lookup"><span data-stu-id="669ed-128">Name of the resource.</span></span>

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

### <span data-ttu-id="669ed-129">Durumlu</span><span class="sxs-lookup"><span data-stu-id="669ed-129">-State</span></span>
<span data-ttu-id="669ed-130">Erişilebilirlik durumunu sunma.</span><span class="sxs-lookup"><span data-stu-id="669ed-130">Offer accessibility state.</span></span>

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

### <span data-ttu-id="669ed-131">-SubscriptionCount</span><span class="sxs-lookup"><span data-stu-id="669ed-131">-SubscriptionCount</span></span>
<span data-ttu-id="669ed-132">Geçerli abonelik sayısı.</span><span class="sxs-lookup"><span data-stu-id="669ed-132">Current subscription count.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: 12
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="669ed-133">-Etiketler</span><span class="sxs-lookup"><span data-stu-id="669ed-133">-Tags</span></span>
<span data-ttu-id="669ed-134">Anahtar-değer çiftleri listesi.</span><span class="sxs-lookup"><span data-stu-id="669ed-134">List of key-value pairs.</span></span>

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="669ed-135">-Tür</span><span class="sxs-lookup"><span data-stu-id="669ed-135">-Type</span></span>
<span data-ttu-id="669ed-136">Kaynak türü.</span><span class="sxs-lookup"><span data-stu-id="669ed-136">Type of resource.</span></span>

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

### <span data-ttu-id="669ed-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="669ed-137">CommonParameters</span></span>
<span data-ttu-id="669ed-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="669ed-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="669ed-139">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="669ed-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="669ed-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="669ed-140">INPUTS</span></span>

## <span data-ttu-id="669ed-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="669ed-141">OUTPUTS</span></span>

## <span data-ttu-id="669ed-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="669ed-142">NOTES</span></span>

## <span data-ttu-id="669ed-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="669ed-143">RELATED LINKS</span></span>

