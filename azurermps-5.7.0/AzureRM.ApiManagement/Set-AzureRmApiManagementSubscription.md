---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 52115C49-0229-4F2C-B7B0-02FC52C1D32D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementSubscription.md
ms.openlocfilehash: 62c1bd394dd509b81a8ea748c26c0465718926c9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593761"
---
# <span data-ttu-id="c2387-101">Set-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="c2387-101">Set-AzureRmApiManagementSubscription</span></span>

## <span data-ttu-id="c2387-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c2387-102">SYNOPSIS</span></span>
<span data-ttu-id="c2387-103">Var olan abonelik ayrıntılarını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="c2387-103">Sets existing subscription details.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c2387-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c2387-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementSubscription -Context <PsApiManagementContext> -SubscriptionId <String>
 [-Name <String>] [-PrimaryKey <String>] [-SecondaryKey <String>] [-State <PsApiManagementSubscriptionState>]
 [-ExpiresOn <DateTime>] [-StateComment <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c2387-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c2387-105">DESCRIPTION</span></span>
<span data-ttu-id="c2387-106">**Set-Azurermapsananagementsubscription** cmdlet 'i var olan abonelik ayrıntılarını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="c2387-106">The **Set-AzureRmApiManagementSubscription** cmdlet sets existing subscription details.</span></span>

## <span data-ttu-id="c2387-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c2387-107">EXAMPLES</span></span>

### <span data-ttu-id="c2387-108">Örnek 1: aboneliğin durumunu ve birincil ve ikincil anahtarlarını ayarlama</span><span class="sxs-lookup"><span data-stu-id="c2387-108">Example 1: Set the state and primary and secondary keys for a subscription</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementSubscription -Context $apimContext -SubscriptionId -0123456789 -PrimaryKey "80450f7d0b6d481382113073f67822c1" -SecondaryKey "97d6112c3a8f48d5bf0266b7a09a761c" -State "Active"
```

<span data-ttu-id="c2387-109">Bu komut abonelik için birincil ve ikincil anahtarları ayarlar ve etkinleştirir.</span><span class="sxs-lookup"><span data-stu-id="c2387-109">This command sets the primary and secondary keys for a subscription and activates it.</span></span>

## <span data-ttu-id="c2387-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c2387-110">PARAMETERS</span></span>

### <span data-ttu-id="c2387-111">-Context</span><span class="sxs-lookup"><span data-stu-id="c2387-111">-Context</span></span>
<span data-ttu-id="c2387-112">**Psapsananagementcontext** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="c2387-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="c2387-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2387-113">-DefaultProfile</span></span>
<span data-ttu-id="c2387-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c2387-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="c2387-115">-ExpiresOn</span><span class="sxs-lookup"><span data-stu-id="c2387-115">-ExpiresOn</span></span>
<span data-ttu-id="c2387-116">Abonelik son kullanım tarihini belirtir.</span><span class="sxs-lookup"><span data-stu-id="c2387-116">Specifies a subscription expiration date.</span></span>
<span data-ttu-id="c2387-117">Bu parametrenin varsayılan değeri $Null.</span><span class="sxs-lookup"><span data-stu-id="c2387-117">The default value of this parameter is $Null.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2387-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="c2387-118">-Name</span></span>
<span data-ttu-id="c2387-119">Abonelik adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c2387-119">Specifies a subscription name.</span></span>

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

### <span data-ttu-id="c2387-120">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="c2387-120">-PassThru</span></span>
<span data-ttu-id="c2387-121">geçiş</span><span class="sxs-lookup"><span data-stu-id="c2387-121">passthru</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2387-122">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="c2387-122">-PrimaryKey</span></span>
<span data-ttu-id="c2387-123">Abonelik birincil anahtarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c2387-123">Specifies the subscription primary key.</span></span>
<span data-ttu-id="c2387-124">Bu parametre belirtilmemişse otomatik olarak oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="c2387-124">This parameter is generated automatically if not specified.</span></span>
<span data-ttu-id="c2387-125">Bu parametre 1-300 karakter uzunluğunda olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="c2387-125">This parameter must be 1 to 300 characters long.</span></span>

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

### <span data-ttu-id="c2387-126">-Secondaryanahtarı</span><span class="sxs-lookup"><span data-stu-id="c2387-126">-SecondaryKey</span></span>
<span data-ttu-id="c2387-127">Abonelik ikincil anahtarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c2387-127">Specifies the subscription secondary key.</span></span>
<span data-ttu-id="c2387-128">Bu parametre belirtilmemişse otomatik olarak oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="c2387-128">This parameter is generated automatically if not specified.</span></span>
<span data-ttu-id="c2387-129">Bu parametre 1-300 karakter uzunluğunda olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="c2387-129">This parameter must be 1 to 300 characters long.</span></span>

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

### <span data-ttu-id="c2387-130">Durumlu</span><span class="sxs-lookup"><span data-stu-id="c2387-130">-State</span></span>
<span data-ttu-id="c2387-131">Abonelik durumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="c2387-131">Specifies the subscription state.</span></span>
<span data-ttu-id="c2387-132">Bu parametrenin varsayılan değeri $Null.</span><span class="sxs-lookup"><span data-stu-id="c2387-132">The default value of this parameter is $Null.</span></span>

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

### <span data-ttu-id="c2387-133">-StateComment</span><span class="sxs-lookup"><span data-stu-id="c2387-133">-StateComment</span></span>
<span data-ttu-id="c2387-134">Abonelik durumu açıklamasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c2387-134">Specifies the subscription state comment.</span></span>
<span data-ttu-id="c2387-135">Bu parametrenin varsayılan değeri $Null.</span><span class="sxs-lookup"><span data-stu-id="c2387-135">The default value of this parameter is $Null.</span></span>

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

### <span data-ttu-id="c2387-136">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="c2387-136">-SubscriptionId</span></span>
<span data-ttu-id="c2387-137">Abonelik KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="c2387-137">Specifies the subscription ID.</span></span>

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

### <span data-ttu-id="c2387-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2387-138">CommonParameters</span></span>
<span data-ttu-id="c2387-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c2387-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2387-140">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c2387-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2387-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c2387-141">INPUTS</span></span>

### <span data-ttu-id="c2387-142">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="c2387-142">None</span></span>
<span data-ttu-id="c2387-143">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="c2387-143">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c2387-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c2387-144">OUTPUTS</span></span>

### <span data-ttu-id="c2387-145">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsanana,</span><span class="sxs-lookup"><span data-stu-id="c2387-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscripition</span></span>

## <span data-ttu-id="c2387-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c2387-146">NOTES</span></span>

## <span data-ttu-id="c2387-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c2387-147">RELATED LINKS</span></span>

[<span data-ttu-id="c2387-148">Get-Azurermapımanagementsubscription</span><span class="sxs-lookup"><span data-stu-id="c2387-148">Get-AzureRmApiManagementSubscription</span></span>](./Get-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="c2387-149">Yeni-Azurermapımanagementsubscription</span><span class="sxs-lookup"><span data-stu-id="c2387-149">New-AzureRmApiManagementSubscription</span></span>](./New-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="c2387-150">Remove-Azurermapımanagementsubscription</span><span class="sxs-lookup"><span data-stu-id="c2387-150">Remove-AzureRmApiManagementSubscription</span></span>](./Remove-AzureRmApiManagementSubscription.md)


