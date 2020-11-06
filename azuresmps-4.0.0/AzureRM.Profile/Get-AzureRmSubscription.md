---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: 13dd14f59b28e3b5730f207c675771e1275392d3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93571746"
---
# <span data-ttu-id="a5590-101">Get-AzureRmSubscription</span><span class="sxs-lookup"><span data-stu-id="a5590-101">Get-AzureRmSubscription</span></span>

## <span data-ttu-id="a5590-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a5590-102">SYNOPSIS</span></span>
<span data-ttu-id="a5590-103">Geçerli hesabın erişebileceği abonelikleri alın.</span><span class="sxs-lookup"><span data-stu-id="a5590-103">Get subscriptions that the current account can access.</span></span>

## <span data-ttu-id="a5590-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a5590-104">SYNTAX</span></span>

### <span data-ttu-id="a5590-105">Listın (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="a5590-105">ListByIdInTenant (Default)</span></span>
```
Get-AzureRmSubscription [-SubscriptionId <String>] [-TenantId <String>] [<CommonParameters>]
```

### <span data-ttu-id="a5590-106">Listbynamei</span><span class="sxs-lookup"><span data-stu-id="a5590-106">ListByNameInTenant</span></span>
```
Get-AzureRmSubscription [-SubscriptionName <String>] [-TenantId <String>] [<CommonParameters>]
```

## <span data-ttu-id="a5590-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="a5590-107">DESCRIPTION</span></span>
<span data-ttu-id="a5590-108">Get-AzureRmSubscription cmdlet 'i, geçerli hesabın erişebileceği abonelikler için abonelik KIMLIĞI, abonelik adı ve ev kiracısını alır.</span><span class="sxs-lookup"><span data-stu-id="a5590-108">The Get-AzureRmSubscription cmdlet gets the subscription ID, subscription name, and home tenant for subscriptions that the current account can access.</span></span>

## <span data-ttu-id="a5590-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a5590-109">EXAMPLES</span></span>

### <span data-ttu-id="a5590-110">Örnek 1: Tüm kiracıları tüm abonelikleri al</span><span class="sxs-lookup"><span data-stu-id="a5590-110">Example 1: Get all subscriptions in all tenants</span></span>
```
PS C:\>Get-AzureRmSubscription -All

Subscription Name : Contoso Subscription 1
SubscriptionId    : xxxx-xxxx-xxxx-xxxx
TenantId          : yyyy-yyyy-yyyy-yyyy
```

<span data-ttu-id="a5590-111">Bu komut, geçerli hesap için yetkilendirilmiş tüm kiracıları tüm abonelikleri alır.</span><span class="sxs-lookup"><span data-stu-id="a5590-111">This command gets all subscriptions in all tenants that are authorized for the current account.</span></span>

### <span data-ttu-id="a5590-112">Örnek 2: belirli bir kiracıya yönelik tüm abonelikleri alma</span><span class="sxs-lookup"><span data-stu-id="a5590-112">Example 2: Get all subscriptions for a specific tenant</span></span>
```
PS C:\>Get-AzureRmSubscription -TenantId "xxxx-xxxx-xxxx-xxxx"

Subscription Name : Contoso Subscription 1
SubscriptionId    : yyyy-yyyy-yyyy-yyyy
TenantId          : xxxx-xxxx-xxxx-xxxx

Subscription Name : Contoso Subscription 2
SubscriptionId    : yyyy-yyyy-yyyy-yyyy
TenantId          : xxxx-xxxx-xxxx-xxxx
```

<span data-ttu-id="a5590-113">Belirtilen Kiracıdaki geçerli hesap için yetkilendirilmiş tüm abonelikleri listeler.</span><span class="sxs-lookup"><span data-stu-id="a5590-113">List all subscriptions in the given tenant that are authorized for the current account.</span></span>

### <span data-ttu-id="a5590-114">Örnek 3: geçerli Kiracıdaki tüm abonelikleri alma</span><span class="sxs-lookup"><span data-stu-id="a5590-114">Example 3: Get all subscriptions in the current tenant</span></span>
```
PS C:\>Get-AzureRmSubscription

Subscription Name : Contoso Subscription 1
SubscriptionId    : yyyy-yyyy-yyyy-yyyy
TenantId          : xxxx-xxxx-xxxx-xxxx

Subscription Name : Contoso Subscription 2
SubscriptionId    : yyyy-yyyy-yyyy-yyyy
TenantId          : xxxx-xxxx-xxxx-xxxx
```

<span data-ttu-id="a5590-115">Bu komut geçerli Kiracıdaki geçerli kullanıcı için yetkilendirilmiş tüm abonelikleri alır.</span><span class="sxs-lookup"><span data-stu-id="a5590-115">This command gets all subscriptions in the current tenant that are authorized for the current user.</span></span>

### <span data-ttu-id="a5590-116">Örnek 4: belirli bir aboneliği kullanmak için geçerli bağlamı değiştirme</span><span class="sxs-lookup"><span data-stu-id="a5590-116">Example 4: Change the current context to use a specific subscription</span></span>
```
PS C:\>Get-AzureRmSubscription -SubscriptionId "xxxx-xxxx-xxxx-xxxx" -TenantId "yyyy-yyyy-yyyy-yyyy" | Set-AzureRmContext

Subscription Name : Contoso Subscription 1
SubscriptionId    : xxxx-xxxx-xxxx-xxxx
TenantId          : yyyy-yyyy-yyyy-yyyy
```

<span data-ttu-id="a5590-117">Bu komut belirtilen aboneliği alır ve geçerli bağlamı kullanacak şekilde ayarlar.</span><span class="sxs-lookup"><span data-stu-id="a5590-117">This command gets the specified subscription, and then sets the current context to use it.</span></span>
<span data-ttu-id="a5590-118">Bu oturumdaki sonraki tüm cmdlet 'ler yeni aboneliği (contoso aboneliği 1) varsayılan olarak kullanır.</span><span class="sxs-lookup"><span data-stu-id="a5590-118">All subsequent cmdlets in this session use the new subscription (Contoso Subscription 1) by default.</span></span>

## <span data-ttu-id="a5590-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a5590-119">PARAMETERS</span></span>

### <span data-ttu-id="a5590-120">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="a5590-120">-SubscriptionId</span></span>
<span data-ttu-id="a5590-121">Alınacak aboneliğin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="a5590-121">Specifies the ID of the subscription to get.</span></span>

```yaml
Type: String
Parameter Sets: ListByIdInTenant
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5590-122">-SubscriptionName</span><span class="sxs-lookup"><span data-stu-id="a5590-122">-SubscriptionName</span></span>
<span data-ttu-id="a5590-123">Alınacak aboneliğin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a5590-123">Specifies the name of the subscription to get.</span></span>

```yaml
Type: String
Parameter Sets: ListByNameInTenant
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5590-124">-Tenantıd</span><span class="sxs-lookup"><span data-stu-id="a5590-124">-TenantId</span></span>
<span data-ttu-id="a5590-125">Alınacak abonelikleri içeren kiracının KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="a5590-125">Specifies the ID of the tenant that contains subscriptions to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5590-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5590-126">CommonParameters</span></span>
<span data-ttu-id="a5590-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a5590-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5590-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5590-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5590-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a5590-129">INPUTS</span></span>

## <span data-ttu-id="a5590-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a5590-130">OUTPUTS</span></span>

### <span data-ttu-id="a5590-131">Psazuyeniden gönderme komut dosyası</span><span class="sxs-lookup"><span data-stu-id="a5590-131">PSAzureSubscription</span></span>

## <span data-ttu-id="a5590-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a5590-132">NOTES</span></span>

## <span data-ttu-id="a5590-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a5590-133">RELATED LINKS</span></span>

