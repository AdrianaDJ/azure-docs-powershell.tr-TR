---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/get-azurermsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmSubscription.md
ms.openlocfilehash: 62f3e1b357c0a85f30ba4eeba6a92d9b8dfc9dd6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590095"
---
# <span data-ttu-id="a6448-101">Get-AzureRmSubscription</span><span class="sxs-lookup"><span data-stu-id="a6448-101">Get-AzureRmSubscription</span></span>

## <span data-ttu-id="a6448-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a6448-102">SYNOPSIS</span></span>
<span data-ttu-id="a6448-103">Geçerli hesabın erişebileceği abonelikleri alın.</span><span class="sxs-lookup"><span data-stu-id="a6448-103">Get subscriptions that the current account can access.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a6448-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a6448-104">SYNTAX</span></span>

### <span data-ttu-id="a6448-105">Listın (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="a6448-105">ListByIdInTenant (Default)</span></span>
```
Get-AzureRmSubscription [-SubscriptionId <String>] [-TenantId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a6448-106">Listbynamei</span><span class="sxs-lookup"><span data-stu-id="a6448-106">ListByNameInTenant</span></span>
```
Get-AzureRmSubscription [-SubscriptionName <String>] [-TenantId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a6448-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="a6448-107">DESCRIPTION</span></span>
<span data-ttu-id="a6448-108">Get-AzureRmSubscription cmdlet 'i, geçerli hesabın erişebileceği abonelikler için abonelik KIMLIĞI, abonelik adı ve ev kiracısını alır.</span><span class="sxs-lookup"><span data-stu-id="a6448-108">The Get-AzureRmSubscription cmdlet gets the subscription ID, subscription name, and home tenant for subscriptions that the current account can access.</span></span>

## <span data-ttu-id="a6448-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a6448-109">EXAMPLES</span></span>

### <span data-ttu-id="a6448-110">Örnek 1: Tüm kiracıları tüm abonelikleri al</span><span class="sxs-lookup"><span data-stu-id="a6448-110">Example 1: Get all subscriptions in all tenants</span></span>
```
PS C:\>Get-AzureRmSubscription

Name                               Id                      TenantId                        State
----                               --                      --------                        -----
Subscription1                      yyyy-yyyy-yyyy-yyyy     aaaa-aaaa-aaaa-aaaa             Enabled
Subscription2                      xxxx-xxxx-xxxx-xxxx     aaaa-aaaa-aaaa-aaaa             Enabled
Subscription3                      zzzz-zzzz-zzzz-zzzz     bbbb-bbbb-bbbb-bbbb             Enabled
```

<span data-ttu-id="a6448-111">Bu komut, geçerli hesap için yetkilendirilmiş tüm kiracıları tüm abonelikleri alır.</span><span class="sxs-lookup"><span data-stu-id="a6448-111">This command gets all subscriptions in all tenants that are authorized for the current account.</span></span>

### <span data-ttu-id="a6448-112">Örnek 2: belirli bir kiracıya yönelik tüm abonelikleri alma</span><span class="sxs-lookup"><span data-stu-id="a6448-112">Example 2: Get all subscriptions for a specific tenant</span></span>
```
PS C:\>Get-AzureRmSubscription -TenantId "xxxx-xxxx-xxxx-xxxx"

Name                               Id                      TenantId                        State
----                               --                      --------                        -----
Subscription1                      yyyy-yyyy-yyyy-yyyy     aaaa-aaaa-aaaa-aaaa             Enabled
Subscription2                      xxxx-xxxx-xxxx-xxxx     aaaa-aaaa-aaaa-aaaa             Enabled
```

<span data-ttu-id="a6448-113">Belirtilen Kiracıdaki geçerli hesap için yetkilendirilmiş tüm abonelikleri listeler.</span><span class="sxs-lookup"><span data-stu-id="a6448-113">List all subscriptions in the given tenant that are authorized for the current account.</span></span>

### <span data-ttu-id="a6448-114">Örnek 3: geçerli Kiracıdaki tüm abonelikleri alma</span><span class="sxs-lookup"><span data-stu-id="a6448-114">Example 3: Get all subscriptions in the current tenant</span></span>
```
PS C:\>Get-AzureRmSubscription

Name                               Id                      TenantId                        State
----                               --                      --------                        -----
Subscription1                      yyyy-yyyy-yyyy-yyyy     aaaa-aaaa-aaaa-aaaa             Enabled
Subscription2                      xxxx-xxxx-xxxx-xxxx     aaaa-aaaa-aaaa-aaaa             Enabled
```

<span data-ttu-id="a6448-115">Bu komut geçerli Kiracıdaki geçerli kullanıcı için yetkilendirilmiş tüm abonelikleri alır.</span><span class="sxs-lookup"><span data-stu-id="a6448-115">This command gets all subscriptions in the current tenant that are authorized for the current user.</span></span>

### <span data-ttu-id="a6448-116">Örnek 4: belirli bir aboneliği kullanmak için geçerli bağlamı değiştirme</span><span class="sxs-lookup"><span data-stu-id="a6448-116">Example 4: Change the current context to use a specific subscription</span></span>
```
PS C:\>Get-AzureRmSubscription -SubscriptionId "xxxx-xxxx-xxxx-xxxx" -TenantId "yyyy-yyyy-yyyy-yyyy" | Set-AzureRmContext

Name                                     Account             SubscriptionName    Environment         TenantId
----                                     -------             ----------------    -----------         --------
Subscription1 (xxxx-xxxx-xxxx-xxxx)      azureuser@micros... Subscription1       AzureCloud          yyyy-yyyy-yyyy-yyyy
```

<span data-ttu-id="a6448-117">Bu komut belirtilen aboneliği alır ve geçerli bağlamı kullanacak şekilde ayarlar.</span><span class="sxs-lookup"><span data-stu-id="a6448-117">This command gets the specified subscription, and then sets the current context to use it.</span></span> <span data-ttu-id="a6448-118">Bu oturumdaki sonraki tüm cmdlet 'ler yeni aboneliği (contoso aboneliği 1) varsayılan olarak kullanır.</span><span class="sxs-lookup"><span data-stu-id="a6448-118">All subsequent cmdlets in this session use the new subscription (Contoso Subscription 1) by default.</span></span>

## <span data-ttu-id="a6448-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a6448-119">PARAMETERS</span></span>

### <span data-ttu-id="a6448-120">-Iş</span><span class="sxs-lookup"><span data-stu-id="a6448-120">-AsJob</span></span>
<span data-ttu-id="a6448-121">Arka planda cmdlet 'i çalıştırın ve ilerlemeyi izlemek için bir Iş dönün.</span><span class="sxs-lookup"><span data-stu-id="a6448-121">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="a6448-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6448-122">-DefaultProfile</span></span>
<span data-ttu-id="a6448-123">Azure ile iletişimde kullanılan kimlik bilgileri, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="a6448-123">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a6448-124">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="a6448-124">-SubscriptionId</span></span>
<span data-ttu-id="a6448-125">Alınacak aboneliğin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="a6448-125">Specifies the ID of the subscription to get.</span></span>

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

### <span data-ttu-id="a6448-126">-SubscriptionName</span><span class="sxs-lookup"><span data-stu-id="a6448-126">-SubscriptionName</span></span>
<span data-ttu-id="a6448-127">Alınacak aboneliğin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a6448-127">Specifies the name of the subscription to get.</span></span>

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

### <span data-ttu-id="a6448-128">-Tenantıd</span><span class="sxs-lookup"><span data-stu-id="a6448-128">-TenantId</span></span>
<span data-ttu-id="a6448-129">Alınacak abonelikleri içeren kiracının KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="a6448-129">Specifies the ID of the tenant that contains subscriptions to get.</span></span>

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

### <span data-ttu-id="a6448-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6448-130">CommonParameters</span></span>
<span data-ttu-id="a6448-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a6448-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6448-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a6448-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6448-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a6448-133">INPUTS</span></span>

### <span data-ttu-id="a6448-134">System. String</span><span class="sxs-lookup"><span data-stu-id="a6448-134">System.String</span></span>

## <span data-ttu-id="a6448-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a6448-135">OUTPUTS</span></span>

### <span data-ttu-id="a6448-136">Microsoft. Azure. Commands. Profile. modeller. psazuyeniden gönderme komutları</span><span class="sxs-lookup"><span data-stu-id="a6448-136">Microsoft.Azure.Commands.Profile.Models.PSAzureSubscription</span></span>

## <span data-ttu-id="a6448-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a6448-137">NOTES</span></span>

## <span data-ttu-id="a6448-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a6448-138">RELATED LINKS</span></span>
