---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: B85BF332-503D-41CB-A3B7-221B85B9BE30
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSubscription.md
ms.openlocfilehash: b836fec6074767e4b97188b5bb75f38d22724eb4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93917843"
---
# <span data-ttu-id="b086d-101">New-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="b086d-101">New-AzApiManagementSubscription</span></span>

## <span data-ttu-id="b086d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b086d-102">SYNOPSIS</span></span>
<span data-ttu-id="b086d-103">Abonelik oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b086d-103">Creates a subscription.</span></span>

## <span data-ttu-id="b086d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b086d-104">SYNTAX</span></span>

```
New-AzApiManagementSubscription -Context <PsApiManagementContext> [-SubscriptionId <String>] -Name <String>
 -UserId <String> -ProductId <String> [-PrimaryKey <String>] [-SecondaryKey <String>]
 [-State <PsApiManagementSubscriptionState>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b086d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b086d-105">DESCRIPTION</span></span>
<span data-ttu-id="b086d-106">**Yeni-Azapsananagementsubscription** cmdlet 'i abonelik oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b086d-106">The **New-AzApiManagementSubscription** cmdlet creates a subscription.</span></span>

## <span data-ttu-id="b086d-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b086d-107">EXAMPLES</span></span>

### <span data-ttu-id="b086d-108">Örnek 1: kullanıcıya bir ürüne abone olma</span><span class="sxs-lookup"><span data-stu-id="b086d-108">Example 1: Subscribe a user to a product</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementSubscription -Context $apimContext -UserId "777" -ProductId "999"
```

<span data-ttu-id="b086d-109">Bu komut, var olan kullanıcıyı bir ürüne abone olur.</span><span class="sxs-lookup"><span data-stu-id="b086d-109">This command subscribes an existing user to a product.</span></span>

## <span data-ttu-id="b086d-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b086d-110">PARAMETERS</span></span>

### <span data-ttu-id="b086d-111">-Context</span><span class="sxs-lookup"><span data-stu-id="b086d-111">-Context</span></span>
<span data-ttu-id="b086d-112">**Psapsananagementcontext** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b086d-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="b086d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b086d-113">-DefaultProfile</span></span>
<span data-ttu-id="b086d-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b086d-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b086d-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="b086d-115">-Name</span></span>
<span data-ttu-id="b086d-116">Abonelik adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b086d-116">Specifies the subscription name.</span></span>

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

### <span data-ttu-id="b086d-117">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="b086d-117">-PrimaryKey</span></span>
<span data-ttu-id="b086d-118">Abonelik birincil anahtarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b086d-118">Specifies the subscription primary key.</span></span>
<span data-ttu-id="b086d-119">Bu parametre belirtilmezse, anahtar otomatik olarak oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="b086d-119">If this parameter is not specified the key is generated automatically.</span></span>
<span data-ttu-id="b086d-120">Bu parametre 1-300 karakter uzunluğunda olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="b086d-120">This parameter must be 1 to 300 characters long.</span></span>

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

### <span data-ttu-id="b086d-121">-ÜrünKimliği</span><span class="sxs-lookup"><span data-stu-id="b086d-121">-ProductId</span></span>
<span data-ttu-id="b086d-122">Abone olunacak ürünün KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="b086d-122">Specifies the ID of the product to which to subscribe.</span></span>

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

### <span data-ttu-id="b086d-123">-Secondaryanahtarı</span><span class="sxs-lookup"><span data-stu-id="b086d-123">-SecondaryKey</span></span>
<span data-ttu-id="b086d-124">Abonelik ikincil anahtarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b086d-124">Specifies the subscription secondary key.</span></span>
<span data-ttu-id="b086d-125">Bu parametre belirtilmemişse, otomatik olarak oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="b086d-125">This parameter is generated automatically if it is not specified.</span></span>
<span data-ttu-id="b086d-126">Bu parametre 1-300 karakter uzunluğunda olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="b086d-126">This parameter must be 1 to 300 characters long.</span></span>

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

### <span data-ttu-id="b086d-127">Durumlu</span><span class="sxs-lookup"><span data-stu-id="b086d-127">-State</span></span>
<span data-ttu-id="b086d-128">Abonelik durumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="b086d-128">Specifies the subscription state.</span></span>
<span data-ttu-id="b086d-129">Varsayılan değer $Null.</span><span class="sxs-lookup"><span data-stu-id="b086d-129">The default value is $Null.</span></span>

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

### <span data-ttu-id="b086d-130">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="b086d-130">-SubscriptionId</span></span>
<span data-ttu-id="b086d-131">Abonelik KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="b086d-131">Specifies the subscription ID.</span></span>
<span data-ttu-id="b086d-132">Bu parametre belirtilmemişse oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="b086d-132">This parameter is generated if not specified.</span></span>

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

### <span data-ttu-id="b086d-133">-UserID</span><span class="sxs-lookup"><span data-stu-id="b086d-133">-UserId</span></span>
<span data-ttu-id="b086d-134">Abone KIMLIĞI 'ni belirtir.</span><span class="sxs-lookup"><span data-stu-id="b086d-134">Specifies the subscriber ID.</span></span>

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

### <span data-ttu-id="b086d-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b086d-135">CommonParameters</span></span>
<span data-ttu-id="b086d-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b086d-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b086d-137">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b086d-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b086d-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b086d-138">INPUTS</span></span>

### <span data-ttu-id="b086d-139">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="b086d-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="b086d-140">System. String</span><span class="sxs-lookup"><span data-stu-id="b086d-140">System.String</span></span>

### <span data-ttu-id="b086d-141">System. Nullable ' 1 [[Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementsubscriptionstate, Microsoft. Azure. PowerShell. cmdlet</span><span class="sxs-lookup"><span data-stu-id="b086d-141">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscriptionState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="b086d-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b086d-142">OUTPUTS</span></span>

### <span data-ttu-id="b086d-143">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementsubscription</span><span class="sxs-lookup"><span data-stu-id="b086d-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription</span></span>

## <span data-ttu-id="b086d-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b086d-144">NOTES</span></span>

## <span data-ttu-id="b086d-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b086d-145">RELATED LINKS</span></span>

[<span data-ttu-id="b086d-146">Get-Azapsananagementsubscription</span><span class="sxs-lookup"><span data-stu-id="b086d-146">Get-AzApiManagementSubscription</span></span>](./Get-AzApiManagementSubscription.md)

[<span data-ttu-id="b086d-147">Remove-Azapsananagementsubscription</span><span class="sxs-lookup"><span data-stu-id="b086d-147">Remove-AzApiManagementSubscription</span></span>](./Remove-AzApiManagementSubscription.md)

[<span data-ttu-id="b086d-148">Set-Azapsananagementsubscription</span><span class="sxs-lookup"><span data-stu-id="b086d-148">Set-AzApiManagementSubscription</span></span>](./Set-AzApiManagementSubscription.md)


