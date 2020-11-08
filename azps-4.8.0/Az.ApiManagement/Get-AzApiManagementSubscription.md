---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 227EF8A2-E04A-4F6B-B66E-E77F1276A7E4
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementSubscription.md
ms.openlocfilehash: e3400ea600ed2891101a94f9ec1a7853326a7c04
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94109895"
---
# <span data-ttu-id="6e2e2-101">Get-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="6e2e2-101">Get-AzApiManagementSubscription</span></span>

## <span data-ttu-id="6e2e2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6e2e2-102">SYNOPSIS</span></span>
<span data-ttu-id="6e2e2-103">Abonelikleri alır.</span><span class="sxs-lookup"><span data-stu-id="6e2e2-103">Gets subscriptions.</span></span>

## <span data-ttu-id="6e2e2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6e2e2-104">SYNTAX</span></span>

### <span data-ttu-id="6e2e2-105">Getallabonelikleri (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="6e2e2-105">GetAllSubscriptions (Default)</span></span>
```
Get-AzApiManagementSubscription -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6e2e2-106">Getbysubscriptionıd</span><span class="sxs-lookup"><span data-stu-id="6e2e2-106">GetBySubscriptionId</span></span>
```
Get-AzApiManagementSubscription -Context <PsApiManagementContext> [-SubscriptionId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6e2e2-107">Getbyproductidanvseçuser</span><span class="sxs-lookup"><span data-stu-id="6e2e2-107">GetByProductIdAndUser</span></span>
```
Get-AzApiManagementSubscription -Context <PsApiManagementContext> -UserId <String> -ProductId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6e2e2-108">Getbyuserıd</span><span class="sxs-lookup"><span data-stu-id="6e2e2-108">GetByUserId</span></span>
```
Get-AzApiManagementSubscription -Context <PsApiManagementContext> [-UserId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6e2e2-109">Getbyproductıd</span><span class="sxs-lookup"><span data-stu-id="6e2e2-109">GetByProductId</span></span>
```
Get-AzApiManagementSubscription -Context <PsApiManagementContext> [-ProductId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6e2e2-110">GetByScope</span><span class="sxs-lookup"><span data-stu-id="6e2e2-110">GetByScope</span></span>
```
Get-AzApiManagementSubscription -Context <PsApiManagementContext> -Scope <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6e2e2-111">Tanım</span><span class="sxs-lookup"><span data-stu-id="6e2e2-111">DESCRIPTION</span></span>
<span data-ttu-id="6e2e2-112">**Get-Azapsananagementsubscription** cmdlet 'i belirtilen bir aboneliği veya herhangi bir abonelik belirtilmemişse tüm abonelikleri alır.</span><span class="sxs-lookup"><span data-stu-id="6e2e2-112">The **Get-AzApiManagementSubscription** cmdlet gets a specified subscription, or all subscriptions, if no subscription is specified.</span></span>
<span data-ttu-id="6e2e2-113">Anahtarlar sonuç ayrıntılarına dahil olmaz.</span><span class="sxs-lookup"><span data-stu-id="6e2e2-113">Keys will not be included into result details.</span></span> <span data-ttu-id="6e2e2-114">Anahtarları almak için **Get-Azapsananagementsubscriptionkey** seçeneğini kullanın.</span><span class="sxs-lookup"><span data-stu-id="6e2e2-114">To get keys, use **Get-AzApiManagementSubscriptionKey**.</span></span>

## <span data-ttu-id="6e2e2-115">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6e2e2-115">EXAMPLES</span></span>

### <span data-ttu-id="6e2e2-116">Örnek 1: tüm abonelikleri al</span><span class="sxs-lookup"><span data-stu-id="6e2e2-116">Example 1: Get all subscriptions</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-East-US" -ServiceName "contoso"
PS C:\>Get-AzApiManagementSubscription -Context $apimContext
```

<span data-ttu-id="6e2e2-117">Bu komut tüm abonelikleri alır.</span><span class="sxs-lookup"><span data-stu-id="6e2e2-117">This command gets all subscriptions.</span></span>

### <span data-ttu-id="6e2e2-118">Örnek 2: belirtilen KIMLIĞE sahip bir abonelik alın</span><span class="sxs-lookup"><span data-stu-id="6e2e2-118">Example 2: Get a subscription with a specified ID</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-East-US" -ServiceName "contoso"
PS C:\>Get-AzApiManagementSubscription -Context $apimContext -SubscriptionId "0123456789"
```

<span data-ttu-id="6e2e2-119">Bu komut, KIMLIĞI bir abonelik alır.</span><span class="sxs-lookup"><span data-stu-id="6e2e2-119">This command gets a subscription by ID.</span></span>

### <span data-ttu-id="6e2e2-120">Örnek 3: kullanıcıya yönelik tüm abonelikleri alma</span><span class="sxs-lookup"><span data-stu-id="6e2e2-120">Example 3: Get all subscriptions for a user</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-East-US" -ServiceName "contoso"
PS C:\>Get-AzApiManagementSubscription -Context $apimContext -UserId "777"
```

<span data-ttu-id="6e2e2-121">Bu komut kullanıcının aboneliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="6e2e2-121">This command gets a user's subscriptions.</span></span>

### <span data-ttu-id="6e2e2-122">Örnek 4: bir ürüne yönelik tüm abonelikleri alma</span><span class="sxs-lookup"><span data-stu-id="6e2e2-122">Example 4: Get all subscriptions for a product</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-East-US" -ServiceName "contoso"
PS C:\>Get-AzApiManagementSubscription -Context $apimContext -ProductId "999"
```

<span data-ttu-id="6e2e2-123">Bu komut, ürünün tüm aboneliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="6e2e2-123">This command gets all subscriptions for the product.</span></span>

### <span data-ttu-id="6e2e2-124">Örnek 5: bir kapsamın tüm aboneliklerini alma</span><span class="sxs-lookup"><span data-stu-id="6e2e2-124">Example 5: Get all subscriptions for a Scope</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-East-US" -ServiceName "contoso"
PS C:\>Get-AzApiManagementSubscription -Context $apimContext -Scope "/apis"

SubscriptionId    : allApScope
UserId            :
OwnerId           :
ProductId         :
Scope             : /subscriptions/subid/resourceGroups/Api-Default-East-US/providers/Microsoft.ApiManagement/service/contoso/apis
Name              : All Api Scope
State             : Active
CreatedDate       : 6/18/2019 5:53:49 PM
StartDate         :
ExpirationDate    :
EndDate           :
NotificationDate  :
PrimaryKey        : 5e48532634114fe999a6979ce0d63a64
SecondaryKey      : 0a8efaf85a664aa0a412241015c7c8f6
StateComment      :
AllowTracing      : False
Id                : /subscriptions/subid/resourceGroups/Api-Default-East-US/providers/Microsoft.ApiManagement/service/contoso/subscriptions/allApScope
ResourceGroupName : Api-Default-East-US
ServiceName       : contoso
```

<span data-ttu-id="6e2e2-125">Bu komut, genel API kapsamı için yapılandırılmış tüm abonelikleri alır</span><span class="sxs-lookup"><span data-stu-id="6e2e2-125">This command gets all subscriptions which are configured for global api scope</span></span>

### <span data-ttu-id="6e2e2-126">Örnek 6: bir ürünün ve Kullanıcı kapsamının tüm aboneliklerini alma</span><span class="sxs-lookup"><span data-stu-id="6e2e2-126">Example 6: Get all subscriptions for a product and user scope</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-East-US" -ServiceName "contoso"
PS C:\>Get-AzApiManagementSubscription -Context $apimContext -ProductId 59b872f28a82740f547e6270 -UserId 1

SubscriptionId    : 59b872f38a82741750c8da56
UserId            : 1
OwnerId           : /subscriptions/subid/resourceGroups/Api-Default-East-US/providers/Microsoft.ApiManagement/service/contoso/users/1
ProductId         : 59b872f28a82740f547e6270
Scope             : /subscriptions/subid/resourceGroups/Api-Default-East-US/providers/Microsoft.ApiManagement/service/contoso/products/59b872f28a82740f547e6270
Name              :
State             : Active
CreatedDate       : 9/12/2017 11:51:15 PM
StartDate         : 9/12/2017 12:00:00 AM
ExpirationDate    :
EndDate           :
NotificationDate  :
PrimaryKey        : 7e64ef904b194706835febf87f729bb0
SecondaryKey      : 0354fccef73e43feb82e5c5da17674d5
StateComment      :
AllowTracing      : True
Id                : /subscriptions/subid/resourceGroups/Api-Default-East-US/providers/Microsoft.ApiManagement/service/contoso/subscriptions/59b872f38a82741750c8da56
ResourceGroupName : Api-Default-East-US
ServiceName       : contoso
```

<span data-ttu-id="6e2e2-127">Bu komut, genel API kapsamı için yapılandırılmış tüm abonelikleri alır</span><span class="sxs-lookup"><span data-stu-id="6e2e2-127">This command gets all subscriptions which are configured for global api scope</span></span>

## <span data-ttu-id="6e2e2-128">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6e2e2-128">PARAMETERS</span></span>

### <span data-ttu-id="6e2e2-129">-Context</span><span class="sxs-lookup"><span data-stu-id="6e2e2-129">-Context</span></span>
<span data-ttu-id="6e2e2-130">**Psapsananagementcontext** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="6e2e2-130">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6e2e2-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e2e2-131">-DefaultProfile</span></span>
<span data-ttu-id="6e2e2-132">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6e2e2-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6e2e2-133">-ÜrünKimliği</span><span class="sxs-lookup"><span data-stu-id="6e2e2-133">-ProductId</span></span>
<span data-ttu-id="6e2e2-134">Ürün tanımlayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6e2e2-134">Specifies a product identifier.</span></span>
<span data-ttu-id="6e2e2-135">Belirtilmişse, bu cmdlet ürün tanımlayıcısının tüm aboneliklerini bulur.</span><span class="sxs-lookup"><span data-stu-id="6e2e2-135">If specified, this cmdlet finds all subscriptions by the product identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByProductIdAndUser
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByProductId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e2e2-136">-Kapsam</span><span class="sxs-lookup"><span data-stu-id="6e2e2-136">-Scope</span></span>
<span data-ttu-id="6e2e2-137">Tanımlama.</span><span class="sxs-lookup"><span data-stu-id="6e2e2-137">Scope identifier.</span></span> <span data-ttu-id="6e2e2-138">Bu, API kapsamı/apis/{apiId} veya ürün kapsamı/Products/{productivseç} veya genel API Scope/API 'leri veya genel Scope/.</span><span class="sxs-lookup"><span data-stu-id="6e2e2-138">The Scope of the Subscription, whether it is Api Scope /apis/{apiId} or Product Scope /products/{productId} or Global API Scope /apis or Global scope /.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e2e2-139">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="6e2e2-139">-SubscriptionId</span></span>
<span data-ttu-id="6e2e2-140">Abonelik tanımlayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6e2e2-140">Specifies a subscription identifier.</span></span>
<span data-ttu-id="6e2e2-141">Belirtilmişse, bu cmdlet tanımlayıcının tanımlayıcısını bulur.</span><span class="sxs-lookup"><span data-stu-id="6e2e2-141">If specified, this cmdlet finds subscription by the identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: GetBySubscriptionId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e2e2-142">-UserID</span><span class="sxs-lookup"><span data-stu-id="6e2e2-142">-UserId</span></span>
<span data-ttu-id="6e2e2-143">Kullanıcı tanımlayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6e2e2-143">Specifies a user identifier.</span></span>
<span data-ttu-id="6e2e2-144">Belirtilmişse, bu cmdlet Kullanıcı tanımlayıcısının tüm aboneliklerini bulur.</span><span class="sxs-lookup"><span data-stu-id="6e2e2-144">If specified, this cmdlet finds all subscriptions by the user identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByProductIdAndUser
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByUserId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e2e2-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e2e2-145">CommonParameters</span></span>
<span data-ttu-id="6e2e2-146">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6e2e2-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e2e2-147">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="6e2e2-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e2e2-148">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6e2e2-148">INPUTS</span></span>

### <span data-ttu-id="6e2e2-149">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="6e2e2-149">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="6e2e2-150">System. String</span><span class="sxs-lookup"><span data-stu-id="6e2e2-150">System.String</span></span>

## <span data-ttu-id="6e2e2-151">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6e2e2-151">OUTPUTS</span></span>

### <span data-ttu-id="6e2e2-152">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementsubscription</span><span class="sxs-lookup"><span data-stu-id="6e2e2-152">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription</span></span>

## <span data-ttu-id="6e2e2-153">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6e2e2-153">NOTES</span></span>

## <span data-ttu-id="6e2e2-154">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6e2e2-154">RELATED LINKS</span></span>

[<span data-ttu-id="6e2e2-155">Yeni-Azsız abonelik</span><span class="sxs-lookup"><span data-stu-id="6e2e2-155">New-AzApiManagementSubscription</span></span>](./New-AzApiManagementSubscription.md)

[<span data-ttu-id="6e2e2-156">Remove-Azapsananagementsubscription</span><span class="sxs-lookup"><span data-stu-id="6e2e2-156">Remove-AzApiManagementSubscription</span></span>](./Remove-AzApiManagementSubscription.md)

[<span data-ttu-id="6e2e2-157">Set-Azapsananagementsubscription</span><span class="sxs-lookup"><span data-stu-id="6e2e2-157">Set-AzApiManagementSubscription</span></span>](./Set-AzApiManagementSubscription.md)


