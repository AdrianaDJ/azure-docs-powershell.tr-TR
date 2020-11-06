---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: B85BF332-503D-41CB-A3B7-221B85B9BE30
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementSubscription.md
ms.openlocfilehash: 08685a84817f55e030a62b0b98ddc35be9f05843
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590545"
---
# <span data-ttu-id="6d659-101">New-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="6d659-101">New-AzureRmApiManagementSubscription</span></span>

## <span data-ttu-id="6d659-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6d659-102">SYNOPSIS</span></span>
<span data-ttu-id="6d659-103">Abonelik oluşturur.</span><span class="sxs-lookup"><span data-stu-id="6d659-103">Creates a subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6d659-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6d659-104">SYNTAX</span></span>

```
New-AzureRmApiManagementSubscription -Context <PsApiManagementContext> [-SubscriptionId <String>]
 -Name <String> -UserId <String> -ProductId <String> [-PrimaryKey <String>] [-SecondaryKey <String>]
 [-State <PsApiManagementSubscriptionState>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6d659-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="6d659-105">DESCRIPTION</span></span>
<span data-ttu-id="6d659-106">**Yeni-Azurermapsananagementsubscription** cmdlet 'i abonelik oluşturur.</span><span class="sxs-lookup"><span data-stu-id="6d659-106">The **New-AzureRmApiManagementSubscription** cmdlet creates a subscription.</span></span>

## <span data-ttu-id="6d659-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6d659-107">EXAMPLES</span></span>

### <span data-ttu-id="6d659-108">Örnek 1: kullanıcıya bir ürüne abone olma</span><span class="sxs-lookup"><span data-stu-id="6d659-108">Example 1: Subscribe a user to a product</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzureRmApiManagementSubscription -Context $apimContext -UserId "777" -ProductId "999"
```

<span data-ttu-id="6d659-109">Bu komut, var olan kullanıcıyı bir ürüne abone olur.</span><span class="sxs-lookup"><span data-stu-id="6d659-109">This command subscribes an existing user to a product.</span></span>

## <span data-ttu-id="6d659-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6d659-110">PARAMETERS</span></span>

### <span data-ttu-id="6d659-111">-Context</span><span class="sxs-lookup"><span data-stu-id="6d659-111">-Context</span></span>
<span data-ttu-id="6d659-112">**Psapsananagementcontext** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="6d659-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="6d659-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d659-113">-DefaultProfile</span></span>
<span data-ttu-id="6d659-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6d659-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="6d659-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="6d659-115">-Name</span></span>
<span data-ttu-id="6d659-116">Abonelik adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6d659-116">Specifies the subscription name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d659-117">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="6d659-117">-PrimaryKey</span></span>
<span data-ttu-id="6d659-118">Abonelik birincil anahtarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6d659-118">Specifies the subscription primary key.</span></span>
<span data-ttu-id="6d659-119">Bu parametre belirtilmezse, anahtar otomatik olarak oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="6d659-119">If this parameter is not specified the key is generated automatically.</span></span>
<span data-ttu-id="6d659-120">Bu parametre 1-300 karakter uzunluğunda olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="6d659-120">This parameter must be 1 to 300 characters long.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d659-121">-ÜrünKimliği</span><span class="sxs-lookup"><span data-stu-id="6d659-121">-ProductId</span></span>
<span data-ttu-id="6d659-122">Abone olunacak ürünün KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="6d659-122">Specifies the ID of the product to which to subscribe.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d659-123">-Secondaryanahtarı</span><span class="sxs-lookup"><span data-stu-id="6d659-123">-SecondaryKey</span></span>
<span data-ttu-id="6d659-124">Abonelik ikincil anahtarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6d659-124">Specifies the subscription secondary key.</span></span>
<span data-ttu-id="6d659-125">Bu parametre belirtilmemişse, otomatik olarak oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="6d659-125">This parameter is generated automatically if it is not specified.</span></span>
<span data-ttu-id="6d659-126">Bu parametre 1-300 karakter uzunluğunda olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="6d659-126">This parameter must be 1 to 300 characters long.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d659-127">Durumlu</span><span class="sxs-lookup"><span data-stu-id="6d659-127">-State</span></span>
<span data-ttu-id="6d659-128">Abonelik durumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="6d659-128">Specifies the subscription state.</span></span>
<span data-ttu-id="6d659-129">Varsayılan değer $Null.</span><span class="sxs-lookup"><span data-stu-id="6d659-129">The default value is $Null.</span></span>

```yaml
Type: PsApiManagementSubscriptionState
Parameter Sets: (All)
Aliases: 
Accepted values: Suspended, Active, Expired, Submitted, Rejected, Cancelled

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d659-130">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="6d659-130">-SubscriptionId</span></span>
<span data-ttu-id="6d659-131">Abonelik KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="6d659-131">Specifies the subscription ID.</span></span>
<span data-ttu-id="6d659-132">Bu parametre belirtilmemişse oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="6d659-132">This parameter is generated if not specified.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d659-133">-UserID</span><span class="sxs-lookup"><span data-stu-id="6d659-133">-UserId</span></span>
<span data-ttu-id="6d659-134">Abone KIMLIĞI 'ni belirtir.</span><span class="sxs-lookup"><span data-stu-id="6d659-134">Specifies the subscriber ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d659-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d659-135">CommonParameters</span></span>
<span data-ttu-id="6d659-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6d659-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d659-137">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6d659-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d659-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6d659-138">INPUTS</span></span>

### <span data-ttu-id="6d659-139">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="6d659-139">None</span></span>
<span data-ttu-id="6d659-140">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="6d659-140">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="6d659-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6d659-141">OUTPUTS</span></span>

### <span data-ttu-id="6d659-142">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementsubscription</span><span class="sxs-lookup"><span data-stu-id="6d659-142">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription</span></span>

## <span data-ttu-id="6d659-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6d659-143">NOTES</span></span>

## <span data-ttu-id="6d659-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6d659-144">RELATED LINKS</span></span>

[<span data-ttu-id="6d659-145">Get-Azurermapımanagementsubscription</span><span class="sxs-lookup"><span data-stu-id="6d659-145">Get-AzureRmApiManagementSubscription</span></span>](./Get-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="6d659-146">Remove-Azurermapımanagementsubscription</span><span class="sxs-lookup"><span data-stu-id="6d659-146">Remove-AzureRmApiManagementSubscription</span></span>](./Remove-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="6d659-147">Set-Azurermapımanagementsubscription</span><span class="sxs-lookup"><span data-stu-id="6d659-147">Set-AzureRmApiManagementSubscription</span></span>](./Set-AzureRmApiManagementSubscription.md)


