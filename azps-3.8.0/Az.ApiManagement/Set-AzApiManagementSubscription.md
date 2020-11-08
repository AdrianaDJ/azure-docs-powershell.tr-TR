---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 52115C49-0229-4F2C-B7B0-02FC52C1D32D
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementSubscription.md
ms.openlocfilehash: 82c49524566293adcd8dcbdcb36359e83360158c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94104169"
---
# <span data-ttu-id="31445-101">Set-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="31445-101">Set-AzApiManagementSubscription</span></span>

## <span data-ttu-id="31445-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="31445-102">SYNOPSIS</span></span>
<span data-ttu-id="31445-103">Var olan abonelik ayrıntılarını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="31445-103">Sets existing subscription details.</span></span>

## <span data-ttu-id="31445-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="31445-104">SYNTAX</span></span>

### <span data-ttu-id="31445-105">ByInputObject (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="31445-105">ByInputObject (Default)</span></span>
```
Set-AzApiManagementSubscription -InputObject <PsApiManagementSubscription> [-Scope <String>] [-UserId <String>]
 [-Name <String>] [-PrimaryKey <String>] [-SecondaryKey <String>] [-State <PsApiManagementSubscriptionState>]
 [-ExpiresOn <DateTime>] [-StateComment <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="31445-106">ExpandedParameter</span><span class="sxs-lookup"><span data-stu-id="31445-106">ExpandedParameter</span></span>
```
Set-AzApiManagementSubscription -Context <PsApiManagementContext> -SubscriptionId <String> [-Scope <String>]
 [-UserId <String>] [-Name <String>] [-PrimaryKey <String>] [-SecondaryKey <String>]
 [-State <PsApiManagementSubscriptionState>] [-ExpiresOn <DateTime>] [-StateComment <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="31445-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="31445-107">DESCRIPTION</span></span>
<span data-ttu-id="31445-108">**Set-Azapsananagementsubscription** cmdlet 'i var olan abonelik ayrıntılarını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="31445-108">The **Set-AzApiManagementSubscription** cmdlet sets existing subscription details.</span></span>

## <span data-ttu-id="31445-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="31445-109">EXAMPLES</span></span>

### <span data-ttu-id="31445-110">Örnek 1: aboneliğin durumunu ve birincil ve ikincil anahtarlarını ayarlama</span><span class="sxs-lookup"><span data-stu-id="31445-110">Example 1: Set the state and primary and secondary keys for a subscription</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementSubscription -Context $apimContext -SubscriptionId -0123456789 -PrimaryKey "80450f7d0b6d481382113073f67822c1" -SecondaryKey "97d6112c3a8f48d5bf0266b7a09a761c" -State "Active"
```

<span data-ttu-id="31445-111">Bu komut abonelik için birincil ve ikincil anahtarları ayarlar ve etkinleştirir.</span><span class="sxs-lookup"><span data-stu-id="31445-111">This command sets the primary and secondary keys for a subscription and activates it.</span></span>

## <span data-ttu-id="31445-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="31445-112">PARAMETERS</span></span>

### <span data-ttu-id="31445-113">-Context</span><span class="sxs-lookup"><span data-stu-id="31445-113">-Context</span></span>
<span data-ttu-id="31445-114">**Psapsananagementcontext** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="31445-114">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="31445-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31445-115">-DefaultProfile</span></span>
<span data-ttu-id="31445-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="31445-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="31445-117">-ExpiresOn</span><span class="sxs-lookup"><span data-stu-id="31445-117">-ExpiresOn</span></span>
<span data-ttu-id="31445-118">Abonelik son kullanım tarihini belirtir.</span><span class="sxs-lookup"><span data-stu-id="31445-118">Specifies a subscription expiration date.</span></span>
<span data-ttu-id="31445-119">Bu parametrenin varsayılan değeri $Null.</span><span class="sxs-lookup"><span data-stu-id="31445-119">The default value of this parameter is $Null.</span></span>

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

### <span data-ttu-id="31445-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="31445-120">-InputObject</span></span>
<span data-ttu-id="31445-121">Psapsananagementsubscription örneği.</span><span class="sxs-lookup"><span data-stu-id="31445-121">Instance of PsApiManagementSubscription.</span></span> <span data-ttu-id="31445-122">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="31445-122">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="31445-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="31445-123">-Name</span></span>
<span data-ttu-id="31445-124">Abonelik adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="31445-124">Specifies a subscription name.</span></span>

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

### <span data-ttu-id="31445-125">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="31445-125">-PassThru</span></span>
<span data-ttu-id="31445-126">geçiş</span><span class="sxs-lookup"><span data-stu-id="31445-126">passthru</span></span>

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

### <span data-ttu-id="31445-127">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="31445-127">-PrimaryKey</span></span>
<span data-ttu-id="31445-128">Abonelik birincil anahtarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="31445-128">Specifies the subscription primary key.</span></span>
<span data-ttu-id="31445-129">Bu parametre belirtilmemişse otomatik olarak oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="31445-129">This parameter is generated automatically if not specified.</span></span>
<span data-ttu-id="31445-130">Bu parametre 1-300 karakter uzunluğunda olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="31445-130">This parameter must be 1 to 300 characters long.</span></span>

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

### <span data-ttu-id="31445-131">-Kapsam</span><span class="sxs-lookup"><span data-stu-id="31445-131">-Scope</span></span>
<span data-ttu-id="31445-132">Bu, API kapsamı/apis/{apiId} veya ürün kapsamı/Products/{productivseç} veya genel API Scope/API 'leri veya genel Scope/.</span><span class="sxs-lookup"><span data-stu-id="31445-132">The Scope of the Subscription, whether it is Api Scope /apis/{apiId} or Product Scope /products/{productId} or Global API Scope /apis or Global scope /.</span></span> <span data-ttu-id="31445-133">Bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="31445-133">This parameter is required.</span></span>

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

### <span data-ttu-id="31445-134">-Secondaryanahtarı</span><span class="sxs-lookup"><span data-stu-id="31445-134">-SecondaryKey</span></span>
<span data-ttu-id="31445-135">Abonelik ikincil anahtarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="31445-135">Specifies the subscription secondary key.</span></span>
<span data-ttu-id="31445-136">Bu parametre belirtilmemişse otomatik olarak oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="31445-136">This parameter is generated automatically if not specified.</span></span>
<span data-ttu-id="31445-137">Bu parametre 1-300 karakter uzunluğunda olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="31445-137">This parameter must be 1 to 300 characters long.</span></span>

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

### <span data-ttu-id="31445-138">Durumlu</span><span class="sxs-lookup"><span data-stu-id="31445-138">-State</span></span>
<span data-ttu-id="31445-139">Abonelik durumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="31445-139">Specifies the subscription state.</span></span>
<span data-ttu-id="31445-140">Bu parametrenin varsayılan değeri $Null.</span><span class="sxs-lookup"><span data-stu-id="31445-140">The default value of this parameter is $Null.</span></span>

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

### <span data-ttu-id="31445-141">-StateComment</span><span class="sxs-lookup"><span data-stu-id="31445-141">-StateComment</span></span>
<span data-ttu-id="31445-142">Abonelik durumu açıklamasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="31445-142">Specifies the subscription state comment.</span></span>
<span data-ttu-id="31445-143">Bu parametrenin varsayılan değeri $Null.</span><span class="sxs-lookup"><span data-stu-id="31445-143">The default value of this parameter is $Null.</span></span>

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

### <span data-ttu-id="31445-144">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="31445-144">-SubscriptionId</span></span>
<span data-ttu-id="31445-145">Abonelik KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="31445-145">Specifies the subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31445-146">-UserID</span><span class="sxs-lookup"><span data-stu-id="31445-146">-UserId</span></span>
<span data-ttu-id="31445-147">Aboneliğin sahibi.</span><span class="sxs-lookup"><span data-stu-id="31445-147">The owner of the subscription.</span></span> <span data-ttu-id="31445-148">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="31445-148">This parameter is optional.</span></span>

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

### <span data-ttu-id="31445-149">-Onay</span><span class="sxs-lookup"><span data-stu-id="31445-149">-Confirm</span></span>
<span data-ttu-id="31445-150">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="31445-150">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31445-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="31445-151">-WhatIf</span></span>
<span data-ttu-id="31445-152">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="31445-152">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="31445-153">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="31445-153">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31445-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31445-154">CommonParameters</span></span>
<span data-ttu-id="31445-155">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="31445-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31445-156">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="31445-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31445-157">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="31445-157">INPUTS</span></span>

### <span data-ttu-id="31445-158">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="31445-158">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="31445-159">System. String</span><span class="sxs-lookup"><span data-stu-id="31445-159">System.String</span></span>

### <span data-ttu-id="31445-160">System. Nullable ' 1 [[Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementsubscriptionstate, Microsoft. Azure. PowerShell. cmdlet</span><span class="sxs-lookup"><span data-stu-id="31445-160">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscriptionState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="31445-161">System. Nullable ' 1 [[System. DATETIME, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]</span><span class="sxs-lookup"><span data-stu-id="31445-161">System.Nullable\`1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="31445-162">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="31445-162">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="31445-163">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="31445-163">OUTPUTS</span></span>

### <span data-ttu-id="31445-164">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementsubscription</span><span class="sxs-lookup"><span data-stu-id="31445-164">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription</span></span>

## <span data-ttu-id="31445-165">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="31445-165">NOTES</span></span>

## <span data-ttu-id="31445-166">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="31445-166">RELATED LINKS</span></span>

[<span data-ttu-id="31445-167">Get-Azapsananagementsubscription</span><span class="sxs-lookup"><span data-stu-id="31445-167">Get-AzApiManagementSubscription</span></span>](./Get-AzApiManagementSubscription.md)

[<span data-ttu-id="31445-168">Yeni-Azsız abonelik</span><span class="sxs-lookup"><span data-stu-id="31445-168">New-AzApiManagementSubscription</span></span>](./New-AzApiManagementSubscription.md)

[<span data-ttu-id="31445-169">Remove-Azapsananagementsubscription</span><span class="sxs-lookup"><span data-stu-id="31445-169">Remove-AzApiManagementSubscription</span></span>](./Remove-AzApiManagementSubscription.md)


