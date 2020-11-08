---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 227EF8A2-E04A-4F6B-B66E-E77F1276A7E4
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementSubscription.md
ms.openlocfilehash: 283d0014b32a1037e3acd655102bc3338d64c554
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94103689"
---
# <span data-ttu-id="627f2-101">Get-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="627f2-101">Get-AzApiManagementSubscription</span></span>

## <span data-ttu-id="627f2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="627f2-102">SYNOPSIS</span></span>
<span data-ttu-id="627f2-103">Abonelikleri alır.</span><span class="sxs-lookup"><span data-stu-id="627f2-103">Gets subscriptions.</span></span>

## <span data-ttu-id="627f2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="627f2-104">SYNTAX</span></span>

### <span data-ttu-id="627f2-105">Getallabonelikleri (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="627f2-105">GetAllSubscriptions (Default)</span></span>
```
Get-AzApiManagementSubscription -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="627f2-106">Getbysubscriptionıd</span><span class="sxs-lookup"><span data-stu-id="627f2-106">GetBySubscriptionId</span></span>
```
Get-AzApiManagementSubscription -Context <PsApiManagementContext> [-SubscriptionId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="627f2-107">Getbyproductidanvseçuser</span><span class="sxs-lookup"><span data-stu-id="627f2-107">GetByProductIdAndUser</span></span>
```
Get-AzApiManagementSubscription -Context <PsApiManagementContext> -UserId <String> -ProductId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="627f2-108">Getbyuserıd</span><span class="sxs-lookup"><span data-stu-id="627f2-108">GetByUserId</span></span>
```
Get-AzApiManagementSubscription -Context <PsApiManagementContext> [-UserId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="627f2-109">Getbyproductıd</span><span class="sxs-lookup"><span data-stu-id="627f2-109">GetByProductId</span></span>
```
Get-AzApiManagementSubscription -Context <PsApiManagementContext> [-ProductId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="627f2-110">GetByScope</span><span class="sxs-lookup"><span data-stu-id="627f2-110">GetByScope</span></span>
```
Get-AzApiManagementSubscription -Context <PsApiManagementContext> -Scope <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="627f2-111">Tanım</span><span class="sxs-lookup"><span data-stu-id="627f2-111">DESCRIPTION</span></span>
<span data-ttu-id="627f2-112">**Get-Azapsananagementsubscription** cmdlet 'i belirtilen bir aboneliği veya herhangi bir abonelik belirtilmemişse tüm abonelikleri alır.</span><span class="sxs-lookup"><span data-stu-id="627f2-112">The **Get-AzApiManagementSubscription** cmdlet gets a specified subscription, or all subscriptions, if no subscription is specified.</span></span>

## <span data-ttu-id="627f2-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="627f2-113">EXAMPLES</span></span>

### <span data-ttu-id="627f2-114">Örnek 1: tüm abonelikleri al</span><span class="sxs-lookup"><span data-stu-id="627f2-114">Example 1: Get all subscriptions</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-East-US" -ServiceName "contoso"
PS C:\>Get-AzApiManagementSubscription -Context $apimContext
```

<span data-ttu-id="627f2-115">Bu komut tüm abonelikleri alır.</span><span class="sxs-lookup"><span data-stu-id="627f2-115">This command gets all subscriptions.</span></span>

### <span data-ttu-id="627f2-116">Örnek 2: belirtilen KIMLIĞE sahip bir abonelik alın</span><span class="sxs-lookup"><span data-stu-id="627f2-116">Example 2: Get a subscription with a specified ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-East-US" -ServiceName "contoso"
PS C:\>Get-AzApiManagementSubscription -Context $apimContext -SubscriptionId "0123456789"
```

<span data-ttu-id="627f2-117">Bu komut, KIMLIĞI bir abonelik alır.</span><span class="sxs-lookup"><span data-stu-id="627f2-117">This command gets a subscription by ID.</span></span>

### <span data-ttu-id="627f2-118">Örnek 3: kullanıcıya yönelik tüm abonelikleri alma</span><span class="sxs-lookup"><span data-stu-id="627f2-118">Example 3: Get all subscriptions for a user</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-East-US" -ServiceName "contoso"
PS C:\>Get-AzApiManagementSubscription -Context $apimContext -UserId "777"
```

<span data-ttu-id="627f2-119">Bu komut kullanıcının aboneliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="627f2-119">This command gets a user's subscriptions.</span></span>

### <span data-ttu-id="627f2-120">Örnek 4: bir ürüne yönelik tüm abonelikleri alma</span><span class="sxs-lookup"><span data-stu-id="627f2-120">Example 4: Get all subscriptions for a product</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-East-US" -ServiceName "contoso"
PS C:\>Get-AzApiManagementSubscription -Context $apimContext -ProductId "999"
```

<span data-ttu-id="627f2-121">Bu komut, ürünün tüm aboneliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="627f2-121">This command gets all subscriptions for the product.</span></span>

### <span data-ttu-id="627f2-122">Örnek 5: bir kapsamın tüm aboneliklerini alma</span><span class="sxs-lookup"><span data-stu-id="627f2-122">Example 5: Get all subscriptions for a Scope</span></span>
```
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

<span data-ttu-id="627f2-123">Bu komut, genel API kapsamı için yapılandırılmış tüm abonelikleri alır</span><span class="sxs-lookup"><span data-stu-id="627f2-123">This command gets all subscriptions which are configured for global api scope</span></span>

### <span data-ttu-id="627f2-124">Örnek 5: bir ürünün ve Kullanıcı kapsamının tüm aboneliklerini alma</span><span class="sxs-lookup"><span data-stu-id="627f2-124">Example 5: Get all subscriptions for a product and user scope</span></span>
```
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

<span data-ttu-id="627f2-125">Bu komut, genel API kapsamı için yapılandırılmış tüm abonelikleri alır</span><span class="sxs-lookup"><span data-stu-id="627f2-125">This command gets all subscriptions which are configured for global api scope</span></span>

## <span data-ttu-id="627f2-126">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="627f2-126">PARAMETERS</span></span>

### <span data-ttu-id="627f2-127">-Context</span><span class="sxs-lookup"><span data-stu-id="627f2-127">-Context</span></span>
<span data-ttu-id="627f2-128">**Psapsananagementcontext** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="627f2-128">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="627f2-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="627f2-129">-DefaultProfile</span></span>
<span data-ttu-id="627f2-130">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="627f2-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="627f2-131">-ÜrünKimliği</span><span class="sxs-lookup"><span data-stu-id="627f2-131">-ProductId</span></span>
<span data-ttu-id="627f2-132">Ürün tanımlayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="627f2-132">Specifies a product identifier.</span></span>
<span data-ttu-id="627f2-133">Belirtilmişse, bu cmdlet ürün tanımlayıcısının tüm aboneliklerini bulur.</span><span class="sxs-lookup"><span data-stu-id="627f2-133">If specified, this cmdlet finds all subscriptions by the product identifier.</span></span>

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

### <span data-ttu-id="627f2-134">-Kapsam</span><span class="sxs-lookup"><span data-stu-id="627f2-134">-Scope</span></span>
<span data-ttu-id="627f2-135">Tanımlama.</span><span class="sxs-lookup"><span data-stu-id="627f2-135">Scope identifier.</span></span> <span data-ttu-id="627f2-136">Bu, API kapsamı/apis/{apiId} veya ürün kapsamı/Products/{productivseç} veya genel API Scope/API 'leri veya genel Scope/.</span><span class="sxs-lookup"><span data-stu-id="627f2-136">The Scope of the Subscription, whether it is Api Scope /apis/{apiId} or Product Scope /products/{productId} or Global API Scope /apis or Global scope /.</span></span>

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

### <span data-ttu-id="627f2-137">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="627f2-137">-SubscriptionId</span></span>
<span data-ttu-id="627f2-138">Abonelik tanımlayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="627f2-138">Specifies a subscription identifier.</span></span>
<span data-ttu-id="627f2-139">Belirtilmişse, bu cmdlet tanımlayıcının tanımlayıcısını bulur.</span><span class="sxs-lookup"><span data-stu-id="627f2-139">If specified, this cmdlet finds subscription by the identifier.</span></span>

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

### <span data-ttu-id="627f2-140">-UserID</span><span class="sxs-lookup"><span data-stu-id="627f2-140">-UserId</span></span>
<span data-ttu-id="627f2-141">Kullanıcı tanımlayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="627f2-141">Specifies a user identifier.</span></span>
<span data-ttu-id="627f2-142">Belirtilmişse, bu cmdlet Kullanıcı tanımlayıcısının tüm aboneliklerini bulur.</span><span class="sxs-lookup"><span data-stu-id="627f2-142">If specified, this cmdlet finds all subscriptions by the user identifier.</span></span>

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

### <span data-ttu-id="627f2-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="627f2-143">CommonParameters</span></span>
<span data-ttu-id="627f2-144">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="627f2-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="627f2-145">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="627f2-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="627f2-146">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="627f2-146">INPUTS</span></span>

### <span data-ttu-id="627f2-147">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="627f2-147">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="627f2-148">System. String</span><span class="sxs-lookup"><span data-stu-id="627f2-148">System.String</span></span>

## <span data-ttu-id="627f2-149">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="627f2-149">OUTPUTS</span></span>

### <span data-ttu-id="627f2-150">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementsubscription</span><span class="sxs-lookup"><span data-stu-id="627f2-150">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription</span></span>

## <span data-ttu-id="627f2-151">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="627f2-151">NOTES</span></span>

## <span data-ttu-id="627f2-152">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="627f2-152">RELATED LINKS</span></span>

[<span data-ttu-id="627f2-153">Yeni-Azsız abonelik</span><span class="sxs-lookup"><span data-stu-id="627f2-153">New-AzApiManagementSubscription</span></span>](./New-AzApiManagementSubscription.md)

[<span data-ttu-id="627f2-154">Remove-Azapsananagementsubscription</span><span class="sxs-lookup"><span data-stu-id="627f2-154">Remove-AzApiManagementSubscription</span></span>](./Remove-AzApiManagementSubscription.md)

[<span data-ttu-id="627f2-155">Set-Azapsananagementsubscription</span><span class="sxs-lookup"><span data-stu-id="627f2-155">Set-AzApiManagementSubscription</span></span>](./Set-AzApiManagementSubscription.md)


