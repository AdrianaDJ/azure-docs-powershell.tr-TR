---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: B85BF332-503D-41CB-A3B7-221B85B9BE30
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementSubscription.md
ms.openlocfilehash: 360bf469f5496d837d12fb6cd4fa8dba9cefd724
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593849"
---
# <span data-ttu-id="d79ee-101">New-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="d79ee-101">New-AzureRmApiManagementSubscription</span></span>

## <span data-ttu-id="d79ee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d79ee-102">SYNOPSIS</span></span>
<span data-ttu-id="d79ee-103">Abonelik oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d79ee-103">Creates a subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d79ee-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d79ee-104">SYNTAX</span></span>

```
New-AzureRmApiManagementSubscription -Context <PsApiManagementContext> [-SubscriptionId <String>]
 -Name <String> -UserId <String> -ProductId <String> [-PrimaryKey <String>] [-SecondaryKey <String>]
 [-State <PsApiManagementSubscriptionState>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d79ee-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="d79ee-105">DESCRIPTION</span></span>
<span data-ttu-id="d79ee-106">**Yeni-Azurermapsananagementsubscription** cmdlet 'i abonelik oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d79ee-106">The **New-AzureRmApiManagementSubscription** cmdlet creates a subscription.</span></span>

## <span data-ttu-id="d79ee-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d79ee-107">EXAMPLES</span></span>

### <span data-ttu-id="d79ee-108">Örnek 1: kullanıcıya bir ürüne abone olma</span><span class="sxs-lookup"><span data-stu-id="d79ee-108">Example 1: Subscribe a user to a product</span></span>
```
PS C:\>New-AzureRmApiManagementSubscription -Context $apimContext -UserId "777" -ProductId "999"
```

<span data-ttu-id="d79ee-109">Bu komut, var olan kullanıcıyı bir ürüne abone olur.</span><span class="sxs-lookup"><span data-stu-id="d79ee-109">This command subscribes an existing user to a product.</span></span>

## <span data-ttu-id="d79ee-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d79ee-110">PARAMETERS</span></span>

### <span data-ttu-id="d79ee-111">-Context</span><span class="sxs-lookup"><span data-stu-id="d79ee-111">-Context</span></span>
<span data-ttu-id="d79ee-112">**Psapsananagementcontext** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="d79ee-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="d79ee-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="d79ee-113">-Name</span></span>
<span data-ttu-id="d79ee-114">Abonelik adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d79ee-114">Specifies the subscription name.</span></span>

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

### <span data-ttu-id="d79ee-115">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="d79ee-115">-PrimaryKey</span></span>
<span data-ttu-id="d79ee-116">Abonelik birincil anahtarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d79ee-116">Specifies the subscription primary key.</span></span>
<span data-ttu-id="d79ee-117">Bu parametre belirtilmezse, anahtar otomatik olarak oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="d79ee-117">If this parameter is not specified the key is generated automatically.</span></span>
<span data-ttu-id="d79ee-118">Bu parametre 1-300 karakter uzunluğunda olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="d79ee-118">This parameter must be 1 to 300 characters long.</span></span>

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

### <span data-ttu-id="d79ee-119">-ÜrünKimliği</span><span class="sxs-lookup"><span data-stu-id="d79ee-119">-ProductId</span></span>
<span data-ttu-id="d79ee-120">Abone olunacak ürünün KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="d79ee-120">Specifies the ID of the product to which to subscribe.</span></span>

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

### <span data-ttu-id="d79ee-121">-Secondaryanahtarı</span><span class="sxs-lookup"><span data-stu-id="d79ee-121">-SecondaryKey</span></span>
<span data-ttu-id="d79ee-122">Abonelik ikincil anahtarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d79ee-122">Specifies the subscription secondary key.</span></span>
<span data-ttu-id="d79ee-123">Bu parametre belirtilmemişse, otomatik olarak oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="d79ee-123">This parameter is generated automatically if it is not specified.</span></span>
<span data-ttu-id="d79ee-124">Bu parametre 1-300 karakter uzunluğunda olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="d79ee-124">This parameter must be 1 to 300 characters long.</span></span>

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

### <span data-ttu-id="d79ee-125">Durumlu</span><span class="sxs-lookup"><span data-stu-id="d79ee-125">-State</span></span>
<span data-ttu-id="d79ee-126">Abonelik durumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="d79ee-126">Specifies the subscription state.</span></span>
<span data-ttu-id="d79ee-127">Varsayılan değer $Null.</span><span class="sxs-lookup"><span data-stu-id="d79ee-127">The default value is $Null.</span></span>

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

### <span data-ttu-id="d79ee-128">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="d79ee-128">-SubscriptionId</span></span>
<span data-ttu-id="d79ee-129">Abonelik KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="d79ee-129">Specifies the subscription ID.</span></span>
<span data-ttu-id="d79ee-130">Bu parametre belirtilmemişse oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="d79ee-130">This parameter is generated if not specified.</span></span>

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

### <span data-ttu-id="d79ee-131">-UserID</span><span class="sxs-lookup"><span data-stu-id="d79ee-131">-UserId</span></span>
<span data-ttu-id="d79ee-132">Abone KIMLIĞI 'ni belirtir.</span><span class="sxs-lookup"><span data-stu-id="d79ee-132">Specifies the subscriber ID.</span></span>

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

### <span data-ttu-id="d79ee-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d79ee-133">-DefaultProfile</span></span>
<span data-ttu-id="d79ee-134">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d79ee-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d79ee-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d79ee-135">CommonParameters</span></span>
<span data-ttu-id="d79ee-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d79ee-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d79ee-137">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d79ee-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d79ee-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d79ee-138">INPUTS</span></span>

## <span data-ttu-id="d79ee-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d79ee-139">OUTPUTS</span></span>

### <span data-ttu-id="d79ee-140">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementsubscription</span><span class="sxs-lookup"><span data-stu-id="d79ee-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription</span></span>

## <span data-ttu-id="d79ee-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d79ee-141">NOTES</span></span>

## <span data-ttu-id="d79ee-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d79ee-142">RELATED LINKS</span></span>

[<span data-ttu-id="d79ee-143">Get-Azurermapımanagementsubscription</span><span class="sxs-lookup"><span data-stu-id="d79ee-143">Get-AzureRmApiManagementSubscription</span></span>](./Get-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="d79ee-144">Remove-Azurermapımanagementsubscription</span><span class="sxs-lookup"><span data-stu-id="d79ee-144">Remove-AzureRmApiManagementSubscription</span></span>](./Remove-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="d79ee-145">Set-Azurermapımanagementsubscription</span><span class="sxs-lookup"><span data-stu-id="d79ee-145">Set-AzureRmApiManagementSubscription</span></span>](./Set-AzureRmApiManagementSubscription.md)


