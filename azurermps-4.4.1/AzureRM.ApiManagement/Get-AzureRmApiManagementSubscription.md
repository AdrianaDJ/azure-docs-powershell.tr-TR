---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 227EF8A2-E04A-4F6B-B66E-E77F1276A7E4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementSubscription.md
ms.openlocfilehash: 173a8a7ab41b044d2a9442a9345ec59ab80329ef
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593862"
---
# <span data-ttu-id="15b97-101">Get-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="15b97-101">Get-AzureRmApiManagementSubscription</span></span>

## <span data-ttu-id="15b97-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="15b97-102">SYNOPSIS</span></span>
<span data-ttu-id="15b97-103">Abonelikleri alır.</span><span class="sxs-lookup"><span data-stu-id="15b97-103">Gets subscriptions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="15b97-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="15b97-104">SYNTAX</span></span>

### <span data-ttu-id="15b97-105">Tüm abonelikleri al (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="15b97-105">Get all subscriptions (Default)</span></span>
```
Get-AzureRmApiManagementSubscription -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="15b97-106">Alt simge alma KIMLIĞI</span><span class="sxs-lookup"><span data-stu-id="15b97-106">Get by subsctiption ID</span></span>
```
Get-AzureRmApiManagementSubscription -Context <PsApiManagementContext> [-SubscriptionId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="15b97-107">Kullanıcı KIMLIĞINE göre al</span><span class="sxs-lookup"><span data-stu-id="15b97-107">Get by user ID</span></span>
```
Get-AzureRmApiManagementSubscription -Context <PsApiManagementContext> [-UserId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="15b97-108">Ürün KIMLIĞINE göre al</span><span class="sxs-lookup"><span data-stu-id="15b97-108">Get by product ID</span></span>
```
Get-AzureRmApiManagementSubscription -Context <PsApiManagementContext> [-ProductId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="15b97-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="15b97-109">DESCRIPTION</span></span>
<span data-ttu-id="15b97-110">**Get-Azurermapsananagementsubscription** cmdlet 'i belirtilen bir aboneliği veya herhangi bir abonelik belirtilmemişse tüm abonelikleri alır.</span><span class="sxs-lookup"><span data-stu-id="15b97-110">The **Get-AzureRmApiManagementSubscription** cmdlet gets a specified subscription, or all subscriptions, if no subscription is specified.</span></span>

## <span data-ttu-id="15b97-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="15b97-111">EXAMPLES</span></span>

### <span data-ttu-id="15b97-112">Örnek 1: tüm abonelikleri al</span><span class="sxs-lookup"><span data-stu-id="15b97-112">Example 1: Get all subscriptions</span></span>
```
PS C:\>Get-AzureRmApiManagementSubscription -Context $apimContext
```

<span data-ttu-id="15b97-113">Bu komut tüm abonelikleri alır.</span><span class="sxs-lookup"><span data-stu-id="15b97-113">This command gets all subscriptions.</span></span>

### <span data-ttu-id="15b97-114">Örnek 2: belirtilen KIMLIĞE sahip bir abonelik alın</span><span class="sxs-lookup"><span data-stu-id="15b97-114">Example 2: Get a subscription with a specified ID</span></span>
```
PS C:\>Get-AzureRmApiManagementSubscription -Context $apimContext -SubscriptionId "0123456789"
```

<span data-ttu-id="15b97-115">Bu komut, KIMLIĞI bir abonelik alır.</span><span class="sxs-lookup"><span data-stu-id="15b97-115">This command gets a subscription by ID.</span></span>

### <span data-ttu-id="15b97-116">Örnek 3: kullanıcıya yönelik tüm abonelikleri alma</span><span class="sxs-lookup"><span data-stu-id="15b97-116">Example 3: Get all subscriptions for a user</span></span>
```
PS C:\>Get-AzureRmApiManagementSubscription -Context $apimContext -UserId "777"
```

<span data-ttu-id="15b97-117">Bu komut kullanıcının aboneliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="15b97-117">This command gets a user's subscriptions.</span></span>

### <span data-ttu-id="15b97-118">Örnek 4: bir ürüne yönelik tüm abonelikleri alma</span><span class="sxs-lookup"><span data-stu-id="15b97-118">Example 4: Get all subscriptions for a product</span></span>
```
PS C:\>Get-AzureRmApiManagementSubscription -Context $apimContext -ProductId "999"
```

<span data-ttu-id="15b97-119">Bu komut, ürünün tüm aboneliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="15b97-119">This command gets all subscriptions for the product.</span></span>

## <span data-ttu-id="15b97-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="15b97-120">PARAMETERS</span></span>

### <span data-ttu-id="15b97-121">-Context</span><span class="sxs-lookup"><span data-stu-id="15b97-121">-Context</span></span>
<span data-ttu-id="15b97-122">**Psapsananagementcontext** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="15b97-122">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15b97-123">-ÜrünKimliği</span><span class="sxs-lookup"><span data-stu-id="15b97-123">-ProductId</span></span>
<span data-ttu-id="15b97-124">Ürün tanımlayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="15b97-124">Specifies a product identifier.</span></span>
<span data-ttu-id="15b97-125">Belirtilmişse, bu cmdlet ürün tanımlayıcısının tüm aboneliklerini bulur.</span><span class="sxs-lookup"><span data-stu-id="15b97-125">If specified, this cmdlet finds all subscriptions by the product identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: Get by product ID
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15b97-126">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="15b97-126">-SubscriptionId</span></span>
<span data-ttu-id="15b97-127">Abonelik tanımlayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="15b97-127">Specifies a subscription identifier.</span></span>
<span data-ttu-id="15b97-128">Belirtilmişse, bu cmdlet tanımlayıcının tanımlayıcısını bulur.</span><span class="sxs-lookup"><span data-stu-id="15b97-128">If specified, this cmdlet finds subscription by the identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: Get by subsctiption ID
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15b97-129">-UserID</span><span class="sxs-lookup"><span data-stu-id="15b97-129">-UserId</span></span>
<span data-ttu-id="15b97-130">Kullanıcı tanımlayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="15b97-130">Specifies a user identifier.</span></span>
<span data-ttu-id="15b97-131">Belirtilmişse, bu cmdlet Kullanıcı tanımlayıcısının tüm aboneliklerini bulur.</span><span class="sxs-lookup"><span data-stu-id="15b97-131">If specified, this cmdlet finds all subscriptions by the user identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: Get by user ID
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15b97-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15b97-132">-DefaultProfile</span></span>
<span data-ttu-id="15b97-133">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="15b97-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="15b97-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15b97-134">CommonParameters</span></span>
<span data-ttu-id="15b97-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="15b97-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15b97-136">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="15b97-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15b97-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="15b97-137">INPUTS</span></span>

## <span data-ttu-id="15b97-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="15b97-138">OUTPUTS</span></span>

### <span data-ttu-id="15b97-139">IList<Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementsubscription></span><span class="sxs-lookup"><span data-stu-id="15b97-139">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription></span></span>

## <span data-ttu-id="15b97-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="15b97-140">NOTES</span></span>

## <span data-ttu-id="15b97-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="15b97-141">RELATED LINKS</span></span>

[<span data-ttu-id="15b97-142">Yeni-Azurermapımanagementsubscription</span><span class="sxs-lookup"><span data-stu-id="15b97-142">New-AzureRmApiManagementSubscription</span></span>](./New-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="15b97-143">Remove-Azurermapımanagementsubscription</span><span class="sxs-lookup"><span data-stu-id="15b97-143">Remove-AzureRmApiManagementSubscription</span></span>](./Remove-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="15b97-144">Set-Azurermapımanagementsubscription</span><span class="sxs-lookup"><span data-stu-id="15b97-144">Set-AzureRmApiManagementSubscription</span></span>](./Set-AzureRmApiManagementSubscription.md)


