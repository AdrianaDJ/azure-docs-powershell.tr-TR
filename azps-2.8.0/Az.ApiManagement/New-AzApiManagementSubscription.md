---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: B85BF332-503D-41CB-A3B7-221B85B9BE30
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSubscription.md
ms.openlocfilehash: 4074afa1c3ba0ad3d4873d290191e63bcc0c57dc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753499"
---
# <span data-ttu-id="2b53e-101">New-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="2b53e-101">New-AzApiManagementSubscription</span></span>

## <span data-ttu-id="2b53e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2b53e-102">SYNOPSIS</span></span>
<span data-ttu-id="2b53e-103">Abonelik oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2b53e-103">Creates a subscription.</span></span>

## <span data-ttu-id="2b53e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2b53e-104">SYNTAX</span></span>

### <span data-ttu-id="2b53e-105">OldSubscriptionModel (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="2b53e-105">OldSubscriptionModel (Default)</span></span>
```
New-AzApiManagementSubscription -Context <PsApiManagementContext> [-SubscriptionId <String>] -Name <String>
 -UserId <String> -ProductId <String> [-PrimaryKey <String>] [-SecondaryKey <String>] [-AllowTracing]
 [-State <PsApiManagementSubscriptionState>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2b53e-106">NewSubscriptionModel</span><span class="sxs-lookup"><span data-stu-id="2b53e-106">NewSubscriptionModel</span></span>
```
New-AzApiManagementSubscription -Context <PsApiManagementContext> [-SubscriptionId <String>] -Name <String>
 [-UserId <String>] -Scope <String> [-PrimaryKey <String>] [-SecondaryKey <String>] [-AllowTracing]
 [-State <PsApiManagementSubscriptionState>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2b53e-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="2b53e-107">DESCRIPTION</span></span>
<span data-ttu-id="2b53e-108">**Yeni-Azapsananagementsubscription** cmdlet 'i abonelik oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2b53e-108">The **New-AzApiManagementSubscription** cmdlet creates a subscription.</span></span>

## <span data-ttu-id="2b53e-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2b53e-109">EXAMPLES</span></span>

### <span data-ttu-id="2b53e-110">Örnek 1: kullanıcıya bir ürüne abone olma</span><span class="sxs-lookup"><span data-stu-id="2b53e-110">Example 1: Subscribe a user to a product</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementSubscription -Context $apimContext -UserId "777" -ProductId "999"
```

<span data-ttu-id="2b53e-111">Bu komut, var olan kullanıcıyı bir ürüne abone olur.</span><span class="sxs-lookup"><span data-stu-id="2b53e-111">This command subscribes an existing user to a product.</span></span>

### <span data-ttu-id="2b53e-112">Örnek 2: tüm API kapsamları için abonelik oluşturma</span><span class="sxs-lookup"><span data-stu-id="2b53e-112">Example 2: Create a subscription for all Api Scope</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementSubscription -Context $context -Scope "/apis" -Name "GlobalApiScope"
```

### <span data-ttu-id="2b53e-113">Örnek 3: ürün kapsamı için abonelik oluşturma</span><span class="sxs-lookup"><span data-stu-id="2b53e-113">Example 3: Create a subscription for Product Scope</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementSubscription -Context $context -Scope "/products/starter" -Name "UnlimitedProductSub"
```

## <span data-ttu-id="2b53e-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2b53e-114">PARAMETERS</span></span>

### <span data-ttu-id="2b53e-115">-AllowTracing</span><span class="sxs-lookup"><span data-stu-id="2b53e-115">-AllowTracing</span></span>
<span data-ttu-id="2b53e-116">Izlemenin abonelik düzeyinde etkinleştirilip etkinleştirilmeyeceğini belirleyen bayrak.</span><span class="sxs-lookup"><span data-stu-id="2b53e-116">Flag which determines whether Tracing can be enabled at the Subscription Level.</span></span> <span data-ttu-id="2b53e-117">Bu isteğe bağlı bir parametredir ve varsayılan $null.</span><span class="sxs-lookup"><span data-stu-id="2b53e-117">This is optional parameter and default is $null.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b53e-118">-Context</span><span class="sxs-lookup"><span data-stu-id="2b53e-118">-Context</span></span>
<span data-ttu-id="2b53e-119">**Psapsananagementcontext** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2b53e-119">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="2b53e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b53e-120">-DefaultProfile</span></span>
<span data-ttu-id="2b53e-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2b53e-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2b53e-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="2b53e-122">-Name</span></span>
<span data-ttu-id="2b53e-123">Abonelik adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2b53e-123">Specifies the subscription name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b53e-124">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="2b53e-124">-PrimaryKey</span></span>
<span data-ttu-id="2b53e-125">Abonelik birincil anahtarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2b53e-125">Specifies the subscription primary key.</span></span>
<span data-ttu-id="2b53e-126">Bu parametre belirtilmezse, anahtar otomatik olarak oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="2b53e-126">If this parameter is not specified the key is generated automatically.</span></span>
<span data-ttu-id="2b53e-127">Bu parametre 1-300 karakter uzunluğunda olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="2b53e-127">This parameter must be 1 to 300 characters long.</span></span>

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

### <span data-ttu-id="2b53e-128">-ÜrünKimliği</span><span class="sxs-lookup"><span data-stu-id="2b53e-128">-ProductId</span></span>
<span data-ttu-id="2b53e-129">Abone olunacak ürünün KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="2b53e-129">Specifies the ID of the product to which to subscribe.</span></span>

```yaml
Type: System.String
Parameter Sets: OldSubscriptionModel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b53e-130">-Kapsam</span><span class="sxs-lookup"><span data-stu-id="2b53e-130">-Scope</span></span>
<span data-ttu-id="2b53e-131">Bu, API kapsamı/apis/{apiId} veya ürün kapsamı/Products/{productivseç} veya genel API Scope/API 'leri veya genel Scope/.</span><span class="sxs-lookup"><span data-stu-id="2b53e-131">The Scope of the Subscription, whether it is Api Scope /apis/{apiId} or Product Scope /products/{productId} or Global API Scope /apis or Global scope /.</span></span> <span data-ttu-id="2b53e-132">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="2b53e-132">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: NewSubscriptionModel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b53e-133">-Secondaryanahtarı</span><span class="sxs-lookup"><span data-stu-id="2b53e-133">-SecondaryKey</span></span>
<span data-ttu-id="2b53e-134">Abonelik ikincil anahtarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2b53e-134">Specifies the subscription secondary key.</span></span>
<span data-ttu-id="2b53e-135">Bu parametre belirtilmemişse, otomatik olarak oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="2b53e-135">This parameter is generated automatically if it is not specified.</span></span>
<span data-ttu-id="2b53e-136">Bu parametre 1-300 karakter uzunluğunda olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="2b53e-136">This parameter must be 1 to 300 characters long.</span></span>

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

### <span data-ttu-id="2b53e-137">Durumlu</span><span class="sxs-lookup"><span data-stu-id="2b53e-137">-State</span></span>
<span data-ttu-id="2b53e-138">Abonelik durumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="2b53e-138">Specifies the subscription state.</span></span>
<span data-ttu-id="2b53e-139">Varsayılan değer $Null.</span><span class="sxs-lookup"><span data-stu-id="2b53e-139">The default value is $Null.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscriptionState]
Parameter Sets: (All)
Aliases:
Accepted values: Suspended, Active, Expired, Submitted, Rejected, Cancelled

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b53e-140">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="2b53e-140">-SubscriptionId</span></span>
<span data-ttu-id="2b53e-141">Abonelik KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="2b53e-141">Specifies the subscription ID.</span></span>
<span data-ttu-id="2b53e-142">Bu parametre belirtilmemişse oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="2b53e-142">This parameter is generated if not specified.</span></span>

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

### <span data-ttu-id="2b53e-143">-UserID</span><span class="sxs-lookup"><span data-stu-id="2b53e-143">-UserId</span></span>
<span data-ttu-id="2b53e-144">Abone KIMLIĞI 'ni belirtir.</span><span class="sxs-lookup"><span data-stu-id="2b53e-144">Specifies the subscriber ID.</span></span>

```yaml
Type: System.String
Parameter Sets: OldSubscriptionModel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: NewSubscriptionModel
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b53e-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b53e-145">CommonParameters</span></span>
<span data-ttu-id="2b53e-146">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2b53e-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b53e-147">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="2b53e-147">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b53e-148">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2b53e-148">INPUTS</span></span>

### <span data-ttu-id="2b53e-149">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="2b53e-149">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="2b53e-150">System. String</span><span class="sxs-lookup"><span data-stu-id="2b53e-150">System.String</span></span>

### <span data-ttu-id="2b53e-151">System. Nullable ' 1 [[Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementsubscriptionstate, Microsoft. Azure. PowerShell. cmdlet</span><span class="sxs-lookup"><span data-stu-id="2b53e-151">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscriptionState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="2b53e-152">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2b53e-152">OUTPUTS</span></span>

### <span data-ttu-id="2b53e-153">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementsubscription</span><span class="sxs-lookup"><span data-stu-id="2b53e-153">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription</span></span>

## <span data-ttu-id="2b53e-154">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2b53e-154">NOTES</span></span>

## <span data-ttu-id="2b53e-155">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2b53e-155">RELATED LINKS</span></span>

[<span data-ttu-id="2b53e-156">Get-Azapsananagementsubscription</span><span class="sxs-lookup"><span data-stu-id="2b53e-156">Get-AzApiManagementSubscription</span></span>](./Get-AzApiManagementSubscription.md)

[<span data-ttu-id="2b53e-157">Remove-Azapsananagementsubscription</span><span class="sxs-lookup"><span data-stu-id="2b53e-157">Remove-AzApiManagementSubscription</span></span>](./Remove-AzApiManagementSubscription.md)

[<span data-ttu-id="2b53e-158">Set-Azapsananagementsubscription</span><span class="sxs-lookup"><span data-stu-id="2b53e-158">Set-AzApiManagementSubscription</span></span>](./Set-AzApiManagementSubscription.md)


