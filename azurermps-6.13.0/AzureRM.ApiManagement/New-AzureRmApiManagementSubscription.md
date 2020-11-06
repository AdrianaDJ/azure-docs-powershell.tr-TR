---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: B85BF332-503D-41CB-A3B7-221B85B9BE30
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementSubscription.md
ms.openlocfilehash: 2600f8f4039e0d719df2f393ffa16d42a712634a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573077"
---
# <span data-ttu-id="c7121-101">New-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="c7121-101">New-AzureRmApiManagementSubscription</span></span>

## <span data-ttu-id="c7121-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c7121-102">SYNOPSIS</span></span>
<span data-ttu-id="c7121-103">Abonelik oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c7121-103">Creates a subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c7121-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c7121-104">SYNTAX</span></span>

```
New-AzureRmApiManagementSubscription -Context <PsApiManagementContext> [-SubscriptionId <String>]
 -Name <String> -UserId <String> -ProductId <String> [-PrimaryKey <String>] [-SecondaryKey <String>]
 [-State <PsApiManagementSubscriptionState>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c7121-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c7121-105">DESCRIPTION</span></span>
<span data-ttu-id="c7121-106">**Yeni-Azurermapsananagementsubscription** cmdlet 'i abonelik oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c7121-106">The **New-AzureRmApiManagementSubscription** cmdlet creates a subscription.</span></span>

## <span data-ttu-id="c7121-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c7121-107">EXAMPLES</span></span>

### <span data-ttu-id="c7121-108">Örnek 1: kullanıcıya bir ürüne abone olma</span><span class="sxs-lookup"><span data-stu-id="c7121-108">Example 1: Subscribe a user to a product</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzureRmApiManagementSubscription -Context $apimContext -UserId "777" -ProductId "999"
```

<span data-ttu-id="c7121-109">Bu komut, var olan kullanıcıyı bir ürüne abone olur.</span><span class="sxs-lookup"><span data-stu-id="c7121-109">This command subscribes an existing user to a product.</span></span>

## <span data-ttu-id="c7121-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c7121-110">PARAMETERS</span></span>

### <span data-ttu-id="c7121-111">-Context</span><span class="sxs-lookup"><span data-stu-id="c7121-111">-Context</span></span>
<span data-ttu-id="c7121-112">**Psapsananagementcontext** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="c7121-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="c7121-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7121-113">-DefaultProfile</span></span>
<span data-ttu-id="c7121-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c7121-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c7121-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="c7121-115">-Name</span></span>
<span data-ttu-id="c7121-116">Abonelik adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c7121-116">Specifies the subscription name.</span></span>

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

### <span data-ttu-id="c7121-117">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="c7121-117">-PrimaryKey</span></span>
<span data-ttu-id="c7121-118">Abonelik birincil anahtarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c7121-118">Specifies the subscription primary key.</span></span>
<span data-ttu-id="c7121-119">Bu parametre belirtilmezse, anahtar otomatik olarak oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="c7121-119">If this parameter is not specified the key is generated automatically.</span></span>
<span data-ttu-id="c7121-120">Bu parametre 1-300 karakter uzunluğunda olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="c7121-120">This parameter must be 1 to 300 characters long.</span></span>

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

### <span data-ttu-id="c7121-121">-ÜrünKimliği</span><span class="sxs-lookup"><span data-stu-id="c7121-121">-ProductId</span></span>
<span data-ttu-id="c7121-122">Abone olunacak ürünün KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="c7121-122">Specifies the ID of the product to which to subscribe.</span></span>

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

### <span data-ttu-id="c7121-123">-Secondaryanahtarı</span><span class="sxs-lookup"><span data-stu-id="c7121-123">-SecondaryKey</span></span>
<span data-ttu-id="c7121-124">Abonelik ikincil anahtarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c7121-124">Specifies the subscription secondary key.</span></span>
<span data-ttu-id="c7121-125">Bu parametre belirtilmemişse, otomatik olarak oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="c7121-125">This parameter is generated automatically if it is not specified.</span></span>
<span data-ttu-id="c7121-126">Bu parametre 1-300 karakter uzunluğunda olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="c7121-126">This parameter must be 1 to 300 characters long.</span></span>

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

### <span data-ttu-id="c7121-127">Durumlu</span><span class="sxs-lookup"><span data-stu-id="c7121-127">-State</span></span>
<span data-ttu-id="c7121-128">Abonelik durumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="c7121-128">Specifies the subscription state.</span></span>
<span data-ttu-id="c7121-129">Varsayılan değer $Null.</span><span class="sxs-lookup"><span data-stu-id="c7121-129">The default value is $Null.</span></span>

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

### <span data-ttu-id="c7121-130">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="c7121-130">-SubscriptionId</span></span>
<span data-ttu-id="c7121-131">Abonelik KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="c7121-131">Specifies the subscription ID.</span></span>
<span data-ttu-id="c7121-132">Bu parametre belirtilmemişse oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="c7121-132">This parameter is generated if not specified.</span></span>

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

### <span data-ttu-id="c7121-133">-UserID</span><span class="sxs-lookup"><span data-stu-id="c7121-133">-UserId</span></span>
<span data-ttu-id="c7121-134">Abone KIMLIĞI 'ni belirtir.</span><span class="sxs-lookup"><span data-stu-id="c7121-134">Specifies the subscriber ID.</span></span>

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

### <span data-ttu-id="c7121-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7121-135">CommonParameters</span></span>
<span data-ttu-id="c7121-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c7121-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7121-137">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c7121-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7121-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c7121-138">INPUTS</span></span>

### <span data-ttu-id="c7121-139">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="c7121-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="c7121-140">System. String</span><span class="sxs-lookup"><span data-stu-id="c7121-140">System.String</span></span>

### <span data-ttu-id="c7121-141">System. Nullable ' 1 [[Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. PsApiManagementSubscriptionState, Microsoft. Azure. Commands</span><span class="sxs-lookup"><span data-stu-id="c7121-141">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscriptionState, Microsoft.Azure.Commands.ApiManagement.ServiceManagement, Version=6.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="c7121-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c7121-142">OUTPUTS</span></span>

### <span data-ttu-id="c7121-143">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementsubscription</span><span class="sxs-lookup"><span data-stu-id="c7121-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription</span></span>

## <span data-ttu-id="c7121-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c7121-144">NOTES</span></span>

## <span data-ttu-id="c7121-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c7121-145">RELATED LINKS</span></span>

[<span data-ttu-id="c7121-146">Get-Azurermapımanagementsubscription</span><span class="sxs-lookup"><span data-stu-id="c7121-146">Get-AzureRmApiManagementSubscription</span></span>](./Get-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="c7121-147">Remove-Azurermapımanagementsubscription</span><span class="sxs-lookup"><span data-stu-id="c7121-147">Remove-AzureRmApiManagementSubscription</span></span>](./Remove-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="c7121-148">Set-Azurermapımanagementsubscription</span><span class="sxs-lookup"><span data-stu-id="c7121-148">Set-AzureRmApiManagementSubscription</span></span>](./Set-AzureRmApiManagementSubscription.md)


