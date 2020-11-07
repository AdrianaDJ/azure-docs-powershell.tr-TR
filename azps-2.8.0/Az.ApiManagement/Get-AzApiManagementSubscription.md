---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 227EF8A2-E04A-4F6B-B66E-E77F1276A7E4
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementSubscription.md
ms.openlocfilehash: 13ca3444a48d79b3708042f6cf8fd0229f80676a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753572"
---
# <span data-ttu-id="09649-101">Get-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="09649-101">Get-AzApiManagementSubscription</span></span>

## <span data-ttu-id="09649-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="09649-102">SYNOPSIS</span></span>
<span data-ttu-id="09649-103">Abonelikleri alır.</span><span class="sxs-lookup"><span data-stu-id="09649-103">Gets subscriptions.</span></span>

## <span data-ttu-id="09649-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="09649-104">SYNTAX</span></span>

### <span data-ttu-id="09649-105">Getallabonelikleri (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="09649-105">GetAllSubscriptions (Default)</span></span>
```
Get-AzApiManagementSubscription -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="09649-106">Getbysubscriptionıd</span><span class="sxs-lookup"><span data-stu-id="09649-106">GetBySubscriptionId</span></span>
```
Get-AzApiManagementSubscription -Context <PsApiManagementContext> [-SubscriptionId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="09649-107">Getbyproductidanvseçuser</span><span class="sxs-lookup"><span data-stu-id="09649-107">GetByProductIdAndUser</span></span>
```
Get-AzApiManagementSubscription -Context <PsApiManagementContext> -UserId <String> -ProductId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="09649-108">Getbyuserıd</span><span class="sxs-lookup"><span data-stu-id="09649-108">GetByUserId</span></span>
```
Get-AzApiManagementSubscription -Context <PsApiManagementContext> [-UserId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="09649-109">Getbyproductıd</span><span class="sxs-lookup"><span data-stu-id="09649-109">GetByProductId</span></span>
```
Get-AzApiManagementSubscription -Context <PsApiManagementContext> [-ProductId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="09649-110">GetByScope</span><span class="sxs-lookup"><span data-stu-id="09649-110">GetByScope</span></span>
```
Get-AzApiManagementSubscription -Context <PsApiManagementContext> -Scope <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="09649-111">Tanım</span><span class="sxs-lookup"><span data-stu-id="09649-111">DESCRIPTION</span></span>
<span data-ttu-id="09649-112">**Get-Azapsananagementsubscription** cmdlet 'i belirtilen bir aboneliği veya herhangi bir abonelik belirtilmemişse tüm abonelikleri alır.</span><span class="sxs-lookup"><span data-stu-id="09649-112">The **Get-AzApiManagementSubscription** cmdlet gets a specified subscription, or all subscriptions, if no subscription is specified.</span></span>

## <span data-ttu-id="09649-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="09649-113">EXAMPLES</span></span>

### <span data-ttu-id="09649-114">Örnek 1: tüm abonelikleri al</span><span class="sxs-lookup"><span data-stu-id="09649-114">Example 1: Get all subscriptions</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-East-US" -ServiceName "contoso"
PS C:\>Get-AzApiManagementSubscription -Context $apimContext
```

<span data-ttu-id="09649-115">Bu komut tüm abonelikleri alır.</span><span class="sxs-lookup"><span data-stu-id="09649-115">This command gets all subscriptions.</span></span>

### <span data-ttu-id="09649-116">Örnek 2: belirtilen KIMLIĞE sahip bir abonelik alın</span><span class="sxs-lookup"><span data-stu-id="09649-116">Example 2: Get a subscription with a specified ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-East-US" -ServiceName "contoso"
PS C:\>Get-AzApiManagementSubscription -Context $apimContext -SubscriptionId "0123456789"
```

<span data-ttu-id="09649-117">Bu komut, KIMLIĞI bir abonelik alır.</span><span class="sxs-lookup"><span data-stu-id="09649-117">This command gets a subscription by ID.</span></span>

### <span data-ttu-id="09649-118">Örnek 3: kullanıcıya yönelik tüm abonelikleri alma</span><span class="sxs-lookup"><span data-stu-id="09649-118">Example 3: Get all subscriptions for a user</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-East-US" -ServiceName "contoso"
PS C:\>Get-AzApiManagementSubscription -Context $apimContext -UserId "777"
```

<span data-ttu-id="09649-119">Bu komut kullanıcının aboneliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="09649-119">This command gets a user's subscriptions.</span></span>

### <span data-ttu-id="09649-120">Örnek 4: bir ürüne yönelik tüm abonelikleri alma</span><span class="sxs-lookup"><span data-stu-id="09649-120">Example 4: Get all subscriptions for a product</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-East-US" -ServiceName "contoso"
PS C:\>Get-AzApiManagementSubscription -Context $apimContext -ProductId "999"
```

<span data-ttu-id="09649-121">Bu komut, ürünün tüm aboneliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="09649-121">This command gets all subscriptions for the product.</span></span>

### <span data-ttu-id="09649-122">Örnek 5: bir kapsamın tüm aboneliklerini alma</span><span class="sxs-lookup"><span data-stu-id="09649-122">Example 5: Get all subscriptions for a Scope</span></span>
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

<span data-ttu-id="09649-123">Bu komut, genel API kapsamı için yapılandırılmış tüm abonelikleri alır</span><span class="sxs-lookup"><span data-stu-id="09649-123">This command gets all subscriptions which are configured for global api scope</span></span>

### <span data-ttu-id="09649-124">Örnek 5: bir ürünün ve Kullanıcı kapsamının tüm aboneliklerini alma</span><span class="sxs-lookup"><span data-stu-id="09649-124">Example 5: Get all subscriptions for a product and user scope</span></span>
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

<span data-ttu-id="09649-125">Bu komut, genel API kapsamı için yapılandırılmış tüm abonelikleri alır</span><span class="sxs-lookup"><span data-stu-id="09649-125">This command gets all subscriptions which are configured for global api scope</span></span>

## <span data-ttu-id="09649-126">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="09649-126">PARAMETERS</span></span>

### <span data-ttu-id="09649-127">-Context</span><span class="sxs-lookup"><span data-stu-id="09649-127">-Context</span></span>
<span data-ttu-id="09649-128">**Psapsananagementcontext** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="09649-128">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="09649-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09649-129">-DefaultProfile</span></span>
<span data-ttu-id="09649-130">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="09649-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="09649-131">-ÜrünKimliği</span><span class="sxs-lookup"><span data-stu-id="09649-131">-ProductId</span></span>
<span data-ttu-id="09649-132">Ürün tanımlayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="09649-132">Specifies a product identifier.</span></span>
<span data-ttu-id="09649-133">Belirtilmişse, bu cmdlet ürün tanımlayıcısının tüm aboneliklerini bulur.</span><span class="sxs-lookup"><span data-stu-id="09649-133">If specified, this cmdlet finds all subscriptions by the product identifier.</span></span>

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

### <span data-ttu-id="09649-134">-Kapsam</span><span class="sxs-lookup"><span data-stu-id="09649-134">-Scope</span></span>
<span data-ttu-id="09649-135">Tanımlama.</span><span class="sxs-lookup"><span data-stu-id="09649-135">Scope identifier.</span></span> <span data-ttu-id="09649-136">Bu, API kapsamı/apis/{apiId} veya ürün kapsamı/Products/{productivseç} veya genel API Scope/API 'leri veya genel Scope/.</span><span class="sxs-lookup"><span data-stu-id="09649-136">The Scope of the Subscription, whether it is Api Scope /apis/{apiId} or Product Scope /products/{productId} or Global API Scope /apis or Global scope /.</span></span>

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

### <span data-ttu-id="09649-137">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="09649-137">-SubscriptionId</span></span>
<span data-ttu-id="09649-138">Abonelik tanımlayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="09649-138">Specifies a subscription identifier.</span></span>
<span data-ttu-id="09649-139">Belirtilmişse, bu cmdlet tanımlayıcının tanımlayıcısını bulur.</span><span class="sxs-lookup"><span data-stu-id="09649-139">If specified, this cmdlet finds subscription by the identifier.</span></span>

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

### <span data-ttu-id="09649-140">-UserID</span><span class="sxs-lookup"><span data-stu-id="09649-140">-UserId</span></span>
<span data-ttu-id="09649-141">Kullanıcı tanımlayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="09649-141">Specifies a user identifier.</span></span>
<span data-ttu-id="09649-142">Belirtilmişse, bu cmdlet Kullanıcı tanımlayıcısının tüm aboneliklerini bulur.</span><span class="sxs-lookup"><span data-stu-id="09649-142">If specified, this cmdlet finds all subscriptions by the user identifier.</span></span>

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

### <span data-ttu-id="09649-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09649-143">CommonParameters</span></span>
<span data-ttu-id="09649-144">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="09649-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09649-145">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="09649-145">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09649-146">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="09649-146">INPUTS</span></span>

### <span data-ttu-id="09649-147">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="09649-147">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="09649-148">System. String</span><span class="sxs-lookup"><span data-stu-id="09649-148">System.String</span></span>

## <span data-ttu-id="09649-149">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="09649-149">OUTPUTS</span></span>

### <span data-ttu-id="09649-150">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementsubscription</span><span class="sxs-lookup"><span data-stu-id="09649-150">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription</span></span>

## <span data-ttu-id="09649-151">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="09649-151">NOTES</span></span>

## <span data-ttu-id="09649-152">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="09649-152">RELATED LINKS</span></span>

[<span data-ttu-id="09649-153">Yeni-Azsız abonelik</span><span class="sxs-lookup"><span data-stu-id="09649-153">New-AzApiManagementSubscription</span></span>](./New-AzApiManagementSubscription.md)

[<span data-ttu-id="09649-154">Remove-Azapsananagementsubscription</span><span class="sxs-lookup"><span data-stu-id="09649-154">Remove-AzApiManagementSubscription</span></span>](./Remove-AzApiManagementSubscription.md)

[<span data-ttu-id="09649-155">Set-Azapsananagementsubscription</span><span class="sxs-lookup"><span data-stu-id="09649-155">Set-AzApiManagementSubscription</span></span>](./Set-AzApiManagementSubscription.md)


