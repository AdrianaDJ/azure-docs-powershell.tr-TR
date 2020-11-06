---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 52115C49-0229-4F2C-B7B0-02FC52C1D32D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementSubscription.md
ms.openlocfilehash: 3b6d07577a6df05a57ed7675f5d14c847e8c33fe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588014"
---
# <span data-ttu-id="ef68d-101">Set-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="ef68d-101">Set-AzureRmApiManagementSubscription</span></span>

## <span data-ttu-id="ef68d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ef68d-102">SYNOPSIS</span></span>
<span data-ttu-id="ef68d-103">Var olan abonelik ayrıntılarını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="ef68d-103">Sets existing subscription details.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ef68d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ef68d-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementSubscription -Context <PsApiManagementContext> -SubscriptionId <String>
 [-Name <String>] [-PrimaryKey <String>] [-SecondaryKey <String>] [-State <PsApiManagementSubscriptionState>]
 [-ExpiresOn <DateTime>] [-StateComment <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ef68d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ef68d-105">DESCRIPTION</span></span>
<span data-ttu-id="ef68d-106">**Set-Azurermapsananagementsubscription** cmdlet 'i var olan abonelik ayrıntılarını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="ef68d-106">The **Set-AzureRmApiManagementSubscription** cmdlet sets existing subscription details.</span></span>

## <span data-ttu-id="ef68d-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ef68d-107">EXAMPLES</span></span>

### <span data-ttu-id="ef68d-108">Örnek 1: aboneliğin durumunu ve birincil ve ikincil anahtarlarını ayarlama</span><span class="sxs-lookup"><span data-stu-id="ef68d-108">Example 1: Set the state and primary and secondary keys for a subscription</span></span>
```
PS C:\>Set-AzureRmApiManagementSubscription -Context $apimContext -SubscriptionId -0123456789 -PrimaryKey "80450f7d0b6d481382113073f67822c1" -SencondaryKey "97d6112c3a8f48d5bf0266b7a09a761c" -State "Active"
```

<span data-ttu-id="ef68d-109">Bu komut abonelik için birincil ve ikincil anahtarları ayarlar ve etkinleştirir.</span><span class="sxs-lookup"><span data-stu-id="ef68d-109">This command sets the primary and secondary keys for a subscription and activates it.</span></span>

## <span data-ttu-id="ef68d-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ef68d-110">PARAMETERS</span></span>

### <span data-ttu-id="ef68d-111">-Context</span><span class="sxs-lookup"><span data-stu-id="ef68d-111">-Context</span></span>
<span data-ttu-id="ef68d-112">**Psapsananagementcontext** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ef68d-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="ef68d-113">-ExpiresOn</span><span class="sxs-lookup"><span data-stu-id="ef68d-113">-ExpiresOn</span></span>
<span data-ttu-id="ef68d-114">Abonelik son kullanım tarihini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ef68d-114">Specifies a subscription expiration date.</span></span>
<span data-ttu-id="ef68d-115">Bu parametrenin varsayılan değeri $Null.</span><span class="sxs-lookup"><span data-stu-id="ef68d-115">The default value of this parameter is $Null.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef68d-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="ef68d-116">-Name</span></span>
<span data-ttu-id="ef68d-117">Abonelik adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ef68d-117">Specifies a subscription name.</span></span>

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

### <span data-ttu-id="ef68d-118">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="ef68d-118">-PassThru</span></span>
<span data-ttu-id="ef68d-119">geçiş</span><span class="sxs-lookup"><span data-stu-id="ef68d-119">passthru</span></span>

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

### <span data-ttu-id="ef68d-120">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="ef68d-120">-PrimaryKey</span></span>
<span data-ttu-id="ef68d-121">Abonelik birincil anahtarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ef68d-121">Specifies the subscription primary key.</span></span>
<span data-ttu-id="ef68d-122">Bu parametre belirtilmemişse otomatik olarak oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="ef68d-122">This parameter is generated automatically if not specified.</span></span>
<span data-ttu-id="ef68d-123">Bu parametre 1-300 karakter uzunluğunda olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="ef68d-123">This parameter must be 1 to 300 characters long.</span></span>

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

### <span data-ttu-id="ef68d-124">-Secondaryanahtarı</span><span class="sxs-lookup"><span data-stu-id="ef68d-124">-SecondaryKey</span></span>
<span data-ttu-id="ef68d-125">Abonelik ikincil anahtarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ef68d-125">Specifies the subscription secondary key.</span></span>
<span data-ttu-id="ef68d-126">Bu parametre belirtilmemişse otomatik olarak oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="ef68d-126">This parameter is generated automatically if not specified.</span></span>
<span data-ttu-id="ef68d-127">Bu parametre 1-300 karakter uzunluğunda olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="ef68d-127">This parameter must be 1 to 300 characters long.</span></span>

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

### <span data-ttu-id="ef68d-128">Durumlu</span><span class="sxs-lookup"><span data-stu-id="ef68d-128">-State</span></span>
<span data-ttu-id="ef68d-129">Abonelik durumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="ef68d-129">Specifies the subscription state.</span></span>
<span data-ttu-id="ef68d-130">Bu parametrenin varsayılan değeri $Null.</span><span class="sxs-lookup"><span data-stu-id="ef68d-130">The default value of this parameter is $Null.</span></span>

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

### <span data-ttu-id="ef68d-131">-StateComment</span><span class="sxs-lookup"><span data-stu-id="ef68d-131">-StateComment</span></span>
<span data-ttu-id="ef68d-132">Abonelik durumu açıklamasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ef68d-132">Specifies the subscription state comment.</span></span>
<span data-ttu-id="ef68d-133">Bu parametrenin varsayılan değeri $Null.</span><span class="sxs-lookup"><span data-stu-id="ef68d-133">The default value of this parameter is $Null.</span></span>

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

### <span data-ttu-id="ef68d-134">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="ef68d-134">-SubscriptionId</span></span>
<span data-ttu-id="ef68d-135">Abonelik KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="ef68d-135">Specifies the subscription ID.</span></span>

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

### <span data-ttu-id="ef68d-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef68d-136">-DefaultProfile</span></span>
<span data-ttu-id="ef68d-137">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ef68d-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ef68d-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef68d-138">CommonParameters</span></span>
<span data-ttu-id="ef68d-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ef68d-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef68d-140">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ef68d-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef68d-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ef68d-141">INPUTS</span></span>

## <span data-ttu-id="ef68d-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ef68d-142">OUTPUTS</span></span>

### <span data-ttu-id="ef68d-143">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsanana,</span><span class="sxs-lookup"><span data-stu-id="ef68d-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscripition</span></span>

## <span data-ttu-id="ef68d-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ef68d-144">NOTES</span></span>

## <span data-ttu-id="ef68d-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ef68d-145">RELATED LINKS</span></span>

[<span data-ttu-id="ef68d-146">Get-Azurermapımanagementsubscription</span><span class="sxs-lookup"><span data-stu-id="ef68d-146">Get-AzureRmApiManagementSubscription</span></span>](./Get-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="ef68d-147">Yeni-Azurermapımanagementsubscription</span><span class="sxs-lookup"><span data-stu-id="ef68d-147">New-AzureRmApiManagementSubscription</span></span>](./New-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="ef68d-148">Remove-Azurermapımanagementsubscription</span><span class="sxs-lookup"><span data-stu-id="ef68d-148">Remove-AzureRmApiManagementSubscription</span></span>](./Remove-AzureRmApiManagementSubscription.md)


