---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/get-azurermsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmSubscription.md
ms.openlocfilehash: 09d51ccf8d4ebdc387977d480be606bf9ed9d9df
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593466"
---
# <span data-ttu-id="56cd2-101">Get-AzureRmSubscription</span><span class="sxs-lookup"><span data-stu-id="56cd2-101">Get-AzureRmSubscription</span></span>

## <span data-ttu-id="56cd2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="56cd2-102">SYNOPSIS</span></span>
<span data-ttu-id="56cd2-103">Geçerli hesabın erişebileceği abonelikleri alın.</span><span class="sxs-lookup"><span data-stu-id="56cd2-103">Get subscriptions that the current account can access.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="56cd2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="56cd2-104">SYNTAX</span></span>

### <span data-ttu-id="56cd2-105">Listın (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="56cd2-105">ListByIdInTenant (Default)</span></span>
```
Get-AzureRmSubscription [-SubscriptionId <String>] [-TenantId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="56cd2-106">Listbynamei</span><span class="sxs-lookup"><span data-stu-id="56cd2-106">ListByNameInTenant</span></span>
```
Get-AzureRmSubscription [-SubscriptionName <String>] [-TenantId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="56cd2-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="56cd2-107">DESCRIPTION</span></span>
<span data-ttu-id="56cd2-108">Get-AzureRmSubscription cmdlet 'i, geçerli hesabın erişebileceği abonelikler için abonelik KIMLIĞI, abonelik adı ve ev kiracısını alır.</span><span class="sxs-lookup"><span data-stu-id="56cd2-108">The Get-AzureRmSubscription cmdlet gets the subscription ID, subscription name, and home tenant for subscriptions that the current account can access.</span></span>

## <span data-ttu-id="56cd2-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="56cd2-109">EXAMPLES</span></span>

### <span data-ttu-id="56cd2-110">Örnek 1: Tüm kiracıları tüm abonelikleri al</span><span class="sxs-lookup"><span data-stu-id="56cd2-110">Example 1: Get all subscriptions in all tenants</span></span>
```
PS C:\>Get-AzureRmSubscription

Name     : Contoso Subscription 1
Id       : xxxx-xxxx-xxxx-xxxx
TenantId : yyyy-yyyy-yyyy-yyyy
State    : Enabled
```

<span data-ttu-id="56cd2-111">Bu komut, geçerli hesap için yetkilendirilmiş tüm kiracıları tüm abonelikleri alır.</span><span class="sxs-lookup"><span data-stu-id="56cd2-111">This command gets all subscriptions in all tenants that are authorized for the current account.</span></span>

### <span data-ttu-id="56cd2-112">Örnek 2: belirli bir kiracıya yönelik tüm abonelikleri alma</span><span class="sxs-lookup"><span data-stu-id="56cd2-112">Example 2: Get all subscriptions for a specific tenant</span></span>
```
PS C:\>Get-AzureRmSubscription -TenantId "xxxx-xxxx-xxxx-xxxx"

Name     : Contoso Subscription 1
Id       : yyyy-yyyy-yyyy-yyyy
TenantId : xxxx-xxxx-xxxx-xxxx
State    : Enabled

Name     : Contoso Subscription 2
Id       : yyyy-yyyy-yyyy-yyyy
TenantId : xxxx-xxxx-xxxx-xxxx
State    : Enabled
```

<span data-ttu-id="56cd2-113">Belirtilen Kiracıdaki geçerli hesap için yetkilendirilmiş tüm abonelikleri listeler.</span><span class="sxs-lookup"><span data-stu-id="56cd2-113">List all subscriptions in the given tenant that are authorized for the current account.</span></span>

### <span data-ttu-id="56cd2-114">Örnek 3: geçerli Kiracıdaki tüm abonelikleri alma</span><span class="sxs-lookup"><span data-stu-id="56cd2-114">Example 3: Get all subscriptions in the current tenant</span></span>
```
PS C:\>Get-AzureRmSubscription

Name     : Contoso Subscription 1
Id       : yyyy-yyyy-yyyy-yyyy
TenantId : xxxx-xxxx-xxxx-xxxx
State    : Enabled

Name     : Contoso Subscription 2
Id       : yyyy-yyyy-yyyy-yyyy
TenantId : xxxx-xxxx-xxxx-xxxx
State    : Enabled
```

<span data-ttu-id="56cd2-115">Bu komut geçerli Kiracıdaki geçerli kullanıcı için yetkilendirilmiş tüm abonelikleri alır.</span><span class="sxs-lookup"><span data-stu-id="56cd2-115">This command gets all subscriptions in the current tenant that are authorized for the current user.</span></span>

### <span data-ttu-id="56cd2-116">Örnek 4: belirli bir aboneliği kullanmak için geçerli bağlamı değiştirme</span><span class="sxs-lookup"><span data-stu-id="56cd2-116">Example 4: Change the current context to use a specific subscription</span></span>
```
PS C:\>Get-AzureRmSubscription -SubscriptionId "xxxx-xxxx-xxxx-xxxx" -TenantId "yyyy-yyyy-yyyy-yyyy" | Set-AzureRmContext

Environment           : AzureCloud
Account               : user@example.com
TenantId              : yyyy-yyyy-yyyy-yyyy
SubscriptionId        : xxxx-xxxx-xxxx-xxxx
SubscriptionName      : Contoso Subscription 1
CurrentStorageAccount :
```

<span data-ttu-id="56cd2-117">Bu komut belirtilen aboneliği alır ve geçerli bağlamı kullanacak şekilde ayarlar.</span><span class="sxs-lookup"><span data-stu-id="56cd2-117">This command gets the specified subscription, and then sets the current context to use it.</span></span> <span data-ttu-id="56cd2-118">Bu oturumdaki sonraki tüm cmdlet 'ler yeni aboneliği (contoso aboneliği 1) varsayılan olarak kullanır.</span><span class="sxs-lookup"><span data-stu-id="56cd2-118">All subsequent cmdlets in this session use the new subscription (Contoso Subscription 1) by default.</span></span>

## <span data-ttu-id="56cd2-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="56cd2-119">PARAMETERS</span></span>

### <span data-ttu-id="56cd2-120">-Iş</span><span class="sxs-lookup"><span data-stu-id="56cd2-120">-AsJob</span></span>
<span data-ttu-id="56cd2-121">Arka planda cmdlet 'i çalıştırın ve ilerlemeyi izlemek için bir Iş dönün.</span><span class="sxs-lookup"><span data-stu-id="56cd2-121">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="56cd2-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56cd2-122">-DefaultProfile</span></span>
<span data-ttu-id="56cd2-123">Azure ile iletişimde kullanılan kimlik bilgileri, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="56cd2-123">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="56cd2-124">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="56cd2-124">-SubscriptionId</span></span>
<span data-ttu-id="56cd2-125">Alınacak aboneliğin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="56cd2-125">Specifies the ID of the subscription to get.</span></span>

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

### <span data-ttu-id="56cd2-126">-SubscriptionName</span><span class="sxs-lookup"><span data-stu-id="56cd2-126">-SubscriptionName</span></span>
<span data-ttu-id="56cd2-127">Alınacak aboneliğin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="56cd2-127">Specifies the name of the subscription to get.</span></span>

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

### <span data-ttu-id="56cd2-128">-Tenantıd</span><span class="sxs-lookup"><span data-stu-id="56cd2-128">-TenantId</span></span>
<span data-ttu-id="56cd2-129">Alınacak abonelikleri içeren kiracının KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="56cd2-129">Specifies the ID of the tenant that contains subscriptions to get.</span></span>

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

### <span data-ttu-id="56cd2-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56cd2-130">CommonParameters</span></span>
<span data-ttu-id="56cd2-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="56cd2-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56cd2-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="56cd2-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56cd2-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="56cd2-133">INPUTS</span></span>

### <span data-ttu-id="56cd2-134">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="56cd2-134">None</span></span>
<span data-ttu-id="56cd2-135">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="56cd2-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="56cd2-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="56cd2-136">OUTPUTS</span></span>

### <span data-ttu-id="56cd2-137">Psazuyeniden gönderme komut dosyası</span><span class="sxs-lookup"><span data-stu-id="56cd2-137">PSAzureSubscription</span></span>

## <span data-ttu-id="56cd2-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="56cd2-138">NOTES</span></span>

## <span data-ttu-id="56cd2-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="56cd2-139">RELATED LINKS</span></span>

