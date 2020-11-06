---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 227EF8A2-E04A-4F6B-B66E-E77F1276A7E4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementSubscription.md
ms.openlocfilehash: 1f863ad8e85a89b0a0af9290649944426709bf31
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586848"
---
# <span data-ttu-id="b1b7b-101">Get-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="b1b7b-101">Get-AzureRmApiManagementSubscription</span></span>

## <span data-ttu-id="b1b7b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b1b7b-102">SYNOPSIS</span></span>
<span data-ttu-id="b1b7b-103">Abonelikleri alır.</span><span class="sxs-lookup"><span data-stu-id="b1b7b-103">Gets subscriptions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b1b7b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b1b7b-104">SYNTAX</span></span>

### <span data-ttu-id="b1b7b-105">Getallabonelikleri (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="b1b7b-105">GetAllSubscriptions (Default)</span></span>
```
Get-AzureRmApiManagementSubscription -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b1b7b-106">Getbysubscriptionıd</span><span class="sxs-lookup"><span data-stu-id="b1b7b-106">GetBySubscriptionId</span></span>
```
Get-AzureRmApiManagementSubscription -Context <PsApiManagementContext> [-SubscriptionId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b1b7b-107">Getbyuserıd</span><span class="sxs-lookup"><span data-stu-id="b1b7b-107">GetByUserId</span></span>
```
Get-AzureRmApiManagementSubscription -Context <PsApiManagementContext> [-UserId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b1b7b-108">Getbyproductıd</span><span class="sxs-lookup"><span data-stu-id="b1b7b-108">GetByProductId</span></span>
```
Get-AzureRmApiManagementSubscription -Context <PsApiManagementContext> [-ProductId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b1b7b-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="b1b7b-109">DESCRIPTION</span></span>
<span data-ttu-id="b1b7b-110">**Get-Azurermapsananagementsubscription** cmdlet 'i belirtilen bir aboneliği veya herhangi bir abonelik belirtilmemişse tüm abonelikleri alır.</span><span class="sxs-lookup"><span data-stu-id="b1b7b-110">The **Get-AzureRmApiManagementSubscription** cmdlet gets a specified subscription, or all subscriptions, if no subscription is specified.</span></span>

## <span data-ttu-id="b1b7b-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b1b7b-111">EXAMPLES</span></span>

### <span data-ttu-id="b1b7b-112">Örnek 1: tüm abonelikleri al</span><span class="sxs-lookup"><span data-stu-id="b1b7b-112">Example 1: Get all subscriptions</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementSubscription -Context $apimContext
```

<span data-ttu-id="b1b7b-113">Bu komut tüm abonelikleri alır.</span><span class="sxs-lookup"><span data-stu-id="b1b7b-113">This command gets all subscriptions.</span></span>

### <span data-ttu-id="b1b7b-114">Örnek 2: belirtilen KIMLIĞE sahip bir abonelik alın</span><span class="sxs-lookup"><span data-stu-id="b1b7b-114">Example 2: Get a subscription with a specified ID</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementSubscription -Context $apimContext -SubscriptionId "0123456789"
```

<span data-ttu-id="b1b7b-115">Bu komut, KIMLIĞI bir abonelik alır.</span><span class="sxs-lookup"><span data-stu-id="b1b7b-115">This command gets a subscription by ID.</span></span>

### <span data-ttu-id="b1b7b-116">Örnek 3: kullanıcıya yönelik tüm abonelikleri alma</span><span class="sxs-lookup"><span data-stu-id="b1b7b-116">Example 3: Get all subscriptions for a user</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementSubscription -Context $apimContext -UserId "777"
```

<span data-ttu-id="b1b7b-117">Bu komut kullanıcının aboneliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="b1b7b-117">This command gets a user's subscriptions.</span></span>

### <span data-ttu-id="b1b7b-118">Örnek 4: bir ürüne yönelik tüm abonelikleri alma</span><span class="sxs-lookup"><span data-stu-id="b1b7b-118">Example 4: Get all subscriptions for a product</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementSubscription -Context $apimContext -ProductId "999"
```

<span data-ttu-id="b1b7b-119">Bu komut, ürünün tüm aboneliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="b1b7b-119">This command gets all subscriptions for the product.</span></span>

## <span data-ttu-id="b1b7b-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b1b7b-120">PARAMETERS</span></span>

### <span data-ttu-id="b1b7b-121">-Context</span><span class="sxs-lookup"><span data-stu-id="b1b7b-121">-Context</span></span>
<span data-ttu-id="b1b7b-122">**Psapsananagementcontext** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b1b7b-122">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1b7b-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1b7b-123">-DefaultProfile</span></span>
<span data-ttu-id="b1b7b-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b1b7b-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="b1b7b-125">-ÜrünKimliği</span><span class="sxs-lookup"><span data-stu-id="b1b7b-125">-ProductId</span></span>
<span data-ttu-id="b1b7b-126">Ürün tanımlayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b1b7b-126">Specifies a product identifier.</span></span>
<span data-ttu-id="b1b7b-127">Belirtilmişse, bu cmdlet ürün tanımlayıcısının tüm aboneliklerini bulur.</span><span class="sxs-lookup"><span data-stu-id="b1b7b-127">If specified, this cmdlet finds all subscriptions by the product identifier.</span></span>

```yaml
Type: String
Parameter Sets: GetByProductId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1b7b-128">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="b1b7b-128">-SubscriptionId</span></span>
<span data-ttu-id="b1b7b-129">Abonelik tanımlayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b1b7b-129">Specifies a subscription identifier.</span></span>
<span data-ttu-id="b1b7b-130">Belirtilmişse, bu cmdlet tanımlayıcının tanımlayıcısını bulur.</span><span class="sxs-lookup"><span data-stu-id="b1b7b-130">If specified, this cmdlet finds subscription by the identifier.</span></span>

```yaml
Type: String
Parameter Sets: GetBySubscriptionId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1b7b-131">-UserID</span><span class="sxs-lookup"><span data-stu-id="b1b7b-131">-UserId</span></span>
<span data-ttu-id="b1b7b-132">Kullanıcı tanımlayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b1b7b-132">Specifies a user identifier.</span></span>
<span data-ttu-id="b1b7b-133">Belirtilmişse, bu cmdlet Kullanıcı tanımlayıcısının tüm aboneliklerini bulur.</span><span class="sxs-lookup"><span data-stu-id="b1b7b-133">If specified, this cmdlet finds all subscriptions by the user identifier.</span></span>

```yaml
Type: String
Parameter Sets: GetByUserId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1b7b-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1b7b-134">CommonParameters</span></span>
<span data-ttu-id="b1b7b-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b1b7b-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1b7b-136">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1b7b-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1b7b-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b1b7b-137">INPUTS</span></span>

### <span data-ttu-id="b1b7b-138">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="b1b7b-138">None</span></span>
<span data-ttu-id="b1b7b-139">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="b1b7b-139">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b1b7b-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b1b7b-140">OUTPUTS</span></span>

### <span data-ttu-id="b1b7b-141">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementsubscription</span><span class="sxs-lookup"><span data-stu-id="b1b7b-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription</span></span>
<span data-ttu-id="b1b7b-142">API yönetim hizmetindeki aboneliğin ayrıntıları.</span><span class="sxs-lookup"><span data-stu-id="b1b7b-142">The detail of the subscription in the API Management service.</span></span>

### <span data-ttu-id="b1b7b-143">IList<Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementsubscription></span><span class="sxs-lookup"><span data-stu-id="b1b7b-143">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription></span></span>
<span data-ttu-id="b1b7b-144">API yönetim hizmetindeki abonelik listesi.</span><span class="sxs-lookup"><span data-stu-id="b1b7b-144">The list of subscription in API Management service.</span></span>

## <span data-ttu-id="b1b7b-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b1b7b-145">NOTES</span></span>

## <span data-ttu-id="b1b7b-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b1b7b-146">RELATED LINKS</span></span>

[<span data-ttu-id="b1b7b-147">Yeni-Azurermapımanagementsubscription</span><span class="sxs-lookup"><span data-stu-id="b1b7b-147">New-AzureRmApiManagementSubscription</span></span>](./New-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="b1b7b-148">Remove-Azurermapımanagementsubscription</span><span class="sxs-lookup"><span data-stu-id="b1b7b-148">Remove-AzureRmApiManagementSubscription</span></span>](./Remove-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="b1b7b-149">Set-Azurermapımanagementsubscription</span><span class="sxs-lookup"><span data-stu-id="b1b7b-149">Set-AzureRmApiManagementSubscription</span></span>](./Set-AzureRmApiManagementSubscription.md)


