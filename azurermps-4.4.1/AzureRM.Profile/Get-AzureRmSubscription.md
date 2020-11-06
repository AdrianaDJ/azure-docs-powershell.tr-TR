---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.profile
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmSubscription.md
ms.openlocfilehash: 9e59fb8ce19d705fffdd52a172be2a333a3ca7a6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590681"
---
# <span data-ttu-id="76837-101">Get-AzureRmSubscription</span><span class="sxs-lookup"><span data-stu-id="76837-101">Get-AzureRmSubscription</span></span>

## <span data-ttu-id="76837-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="76837-102">SYNOPSIS</span></span>
<span data-ttu-id="76837-103">Geçerli hesabın erişebileceği abonelikleri alın.</span><span class="sxs-lookup"><span data-stu-id="76837-103">Get subscriptions that the current account can access.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="76837-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="76837-104">SYNTAX</span></span>

### <span data-ttu-id="76837-105">Listın (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="76837-105">ListByIdInTenant (Default)</span></span>
```
Get-AzureRmSubscription [-SubscriptionId <String>] [-TenantId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="76837-106">Listbynamei</span><span class="sxs-lookup"><span data-stu-id="76837-106">ListByNameInTenant</span></span>
```
Get-AzureRmSubscription [-SubscriptionName <String>] [-TenantId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="76837-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="76837-107">DESCRIPTION</span></span>
<span data-ttu-id="76837-108">Get-AzureRmSubscription cmdlet 'i, geçerli hesabın erişebileceği abonelikler için abonelik KIMLIĞI, abonelik adı ve ev kiracısını alır.</span><span class="sxs-lookup"><span data-stu-id="76837-108">The Get-AzureRmSubscription cmdlet gets the subscription ID, subscription name, and home tenant for subscriptions that the current account can access.</span></span>

## <span data-ttu-id="76837-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="76837-109">EXAMPLES</span></span>

### <span data-ttu-id="76837-110">Örnek 1: Tüm kiracıları tüm abonelikleri al</span><span class="sxs-lookup"><span data-stu-id="76837-110">Example 1: Get all subscriptions in all tenants</span></span>
```
PS C:\>Get-AzureRmSubscription

Subscription Name : Contoso Subscription 1
SubscriptionId    : xxxx-xxxx-xxxx-xxxx
TenantId          : yyyy-yyyy-yyyy-yyyy
```

<span data-ttu-id="76837-111">Bu komut, geçerli hesap için yetkilendirilmiş tüm kiracıları tüm abonelikleri alır.</span><span class="sxs-lookup"><span data-stu-id="76837-111">This command gets all subscriptions in all tenants that are authorized for the current account.</span></span>

### <span data-ttu-id="76837-112">Örnek 2: belirli bir kiracıya yönelik tüm abonelikleri alma</span><span class="sxs-lookup"><span data-stu-id="76837-112">Example 2: Get all subscriptions for a specific tenant</span></span>
```
PS C:\>Get-AzureRmSubscription -TenantId "xxxx-xxxx-xxxx-xxxx"

Subscription Name : Contoso Subscription 1
SubscriptionId    : yyyy-yyyy-yyyy-yyyy
TenantId          : xxxx-xxxx-xxxx-xxxx

Subscription Name : Contoso Subscription 2
SubscriptionId    : yyyy-yyyy-yyyy-yyyy
TenantId          : xxxx-xxxx-xxxx-xxxx
```

<span data-ttu-id="76837-113">Belirtilen Kiracıdaki geçerli hesap için yetkilendirilmiş tüm abonelikleri listeler.</span><span class="sxs-lookup"><span data-stu-id="76837-113">List all subscriptions in the given tenant that are authorized for the current account.</span></span>

### <span data-ttu-id="76837-114">Örnek 3: geçerli Kiracıdaki tüm abonelikleri alma</span><span class="sxs-lookup"><span data-stu-id="76837-114">Example 3: Get all subscriptions in the current tenant</span></span>
```
PS C:\>Get-AzureRmSubscription

Subscription Name : Contoso Subscription 1
SubscriptionId    : yyyy-yyyy-yyyy-yyyy
TenantId          : xxxx-xxxx-xxxx-xxxx

Subscription Name : Contoso Subscription 2
SubscriptionId    : yyyy-yyyy-yyyy-yyyy
TenantId          : xxxx-xxxx-xxxx-xxxx
```

<span data-ttu-id="76837-115">Bu komut geçerli Kiracıdaki geçerli kullanıcı için yetkilendirilmiş tüm abonelikleri alır.</span><span class="sxs-lookup"><span data-stu-id="76837-115">This command gets all subscriptions in the current tenant that are authorized for the current user.</span></span>

### <span data-ttu-id="76837-116">Örnek 4: belirli bir aboneliği kullanmak için geçerli bağlamı değiştirme</span><span class="sxs-lookup"><span data-stu-id="76837-116">Example 4: Change the current context to use a specific subscription</span></span>
```
PS C:\>Get-AzureRmSubscription -SubscriptionId "xxxx-xxxx-xxxx-xxxx" -TenantId "yyyy-yyyy-yyyy-yyyy" | Set-AzureRmContext

Subscription Name : Contoso Subscription 1
SubscriptionId    : xxxx-xxxx-xxxx-xxxx
TenantId          : yyyy-yyyy-yyyy-yyyy
```

<span data-ttu-id="76837-117">Bu komut belirtilen aboneliği alır ve geçerli bağlamı kullanacak şekilde ayarlar.</span><span class="sxs-lookup"><span data-stu-id="76837-117">This command gets the specified subscription, and then sets the current context to use it.</span></span> <span data-ttu-id="76837-118">Bu oturumdaki sonraki tüm cmdlet 'ler yeni aboneliği (contoso aboneliği 1) varsayılan olarak kullanır.</span><span class="sxs-lookup"><span data-stu-id="76837-118">All subsequent cmdlets in this session use the new subscription (Contoso Subscription 1) by default.</span></span>

## <span data-ttu-id="76837-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="76837-119">PARAMETERS</span></span>

### <span data-ttu-id="76837-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76837-120">-DefaultProfile</span></span>
<span data-ttu-id="76837-121">Azure ile iletişimde kullanılan kimlik bilgileri, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="76837-121">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="76837-122">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="76837-122">-SubscriptionId</span></span>
<span data-ttu-id="76837-123">Alınacak aboneliğin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="76837-123">Specifies the ID of the subscription to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByIdInTenant
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76837-124">-SubscriptionName</span><span class="sxs-lookup"><span data-stu-id="76837-124">-SubscriptionName</span></span>
<span data-ttu-id="76837-125">Alınacak aboneliğin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="76837-125">Specifies the name of the subscription to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByNameInTenant
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76837-126">-Tenantıd</span><span class="sxs-lookup"><span data-stu-id="76837-126">-TenantId</span></span>
<span data-ttu-id="76837-127">Alınacak abonelikleri içeren kiracının KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="76837-127">Specifies the ID of the tenant that contains subscriptions to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76837-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76837-128">CommonParameters</span></span>
<span data-ttu-id="76837-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="76837-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76837-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="76837-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76837-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="76837-131">INPUTS</span></span>

## <span data-ttu-id="76837-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="76837-132">OUTPUTS</span></span>

### <span data-ttu-id="76837-133">Psazuyeniden gönderme komut dosyası</span><span class="sxs-lookup"><span data-stu-id="76837-133">PSAzureSubscription</span></span>

## <span data-ttu-id="76837-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="76837-134">NOTES</span></span>

## <span data-ttu-id="76837-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="76837-135">RELATED LINKS</span></span>

