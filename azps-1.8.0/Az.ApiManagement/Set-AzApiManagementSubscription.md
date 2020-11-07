---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 52115C49-0229-4F2C-B7B0-02FC52C1D32D
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementSubscription.md
ms.openlocfilehash: cbdc876368f55ace6f77c04172dc2f0a53b0a7f6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93761666"
---
# <span data-ttu-id="7a53f-101">Set-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="7a53f-101">Set-AzApiManagementSubscription</span></span>

## <span data-ttu-id="7a53f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7a53f-102">SYNOPSIS</span></span>
<span data-ttu-id="7a53f-103">Var olan abonelik ayrıntılarını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="7a53f-103">Sets existing subscription details.</span></span>

## <span data-ttu-id="7a53f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7a53f-104">SYNTAX</span></span>

```
Set-AzApiManagementSubscription -Context <PsApiManagementContext> -SubscriptionId <String> [-Name <String>]
 [-PrimaryKey <String>] [-SecondaryKey <String>] [-State <PsApiManagementSubscriptionState>]
 [-ExpiresOn <DateTime>] [-StateComment <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7a53f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="7a53f-105">DESCRIPTION</span></span>
<span data-ttu-id="7a53f-106">**Set-Azapsananagementsubscription** cmdlet 'i var olan abonelik ayrıntılarını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="7a53f-106">The **Set-AzApiManagementSubscription** cmdlet sets existing subscription details.</span></span>

## <span data-ttu-id="7a53f-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7a53f-107">EXAMPLES</span></span>

### <span data-ttu-id="7a53f-108">Örnek 1: aboneliğin durumunu ve birincil ve ikincil anahtarlarını ayarlama</span><span class="sxs-lookup"><span data-stu-id="7a53f-108">Example 1: Set the state and primary and secondary keys for a subscription</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementSubscription -Context $apimContext -SubscriptionId -0123456789 -PrimaryKey "80450f7d0b6d481382113073f67822c1" -SecondaryKey "97d6112c3a8f48d5bf0266b7a09a761c" -State "Active"
```

<span data-ttu-id="7a53f-109">Bu komut abonelik için birincil ve ikincil anahtarları ayarlar ve etkinleştirir.</span><span class="sxs-lookup"><span data-stu-id="7a53f-109">This command sets the primary and secondary keys for a subscription and activates it.</span></span>

## <span data-ttu-id="7a53f-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7a53f-110">PARAMETERS</span></span>

### <span data-ttu-id="7a53f-111">-Context</span><span class="sxs-lookup"><span data-stu-id="7a53f-111">-Context</span></span>
<span data-ttu-id="7a53f-112">**Psapsananagementcontext** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="7a53f-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="7a53f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a53f-113">-DefaultProfile</span></span>
<span data-ttu-id="7a53f-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7a53f-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7a53f-115">-ExpiresOn</span><span class="sxs-lookup"><span data-stu-id="7a53f-115">-ExpiresOn</span></span>
<span data-ttu-id="7a53f-116">Abonelik son kullanım tarihini belirtir.</span><span class="sxs-lookup"><span data-stu-id="7a53f-116">Specifies a subscription expiration date.</span></span>
<span data-ttu-id="7a53f-117">Bu parametrenin varsayılan değeri $Null.</span><span class="sxs-lookup"><span data-stu-id="7a53f-117">The default value of this parameter is $Null.</span></span>

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

### <span data-ttu-id="7a53f-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="7a53f-118">-Name</span></span>
<span data-ttu-id="7a53f-119">Abonelik adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7a53f-119">Specifies a subscription name.</span></span>

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

### <span data-ttu-id="7a53f-120">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="7a53f-120">-PassThru</span></span>
<span data-ttu-id="7a53f-121">geçiş</span><span class="sxs-lookup"><span data-stu-id="7a53f-121">passthru</span></span>

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

### <span data-ttu-id="7a53f-122">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="7a53f-122">-PrimaryKey</span></span>
<span data-ttu-id="7a53f-123">Abonelik birincil anahtarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7a53f-123">Specifies the subscription primary key.</span></span>
<span data-ttu-id="7a53f-124">Bu parametre belirtilmemişse otomatik olarak oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="7a53f-124">This parameter is generated automatically if not specified.</span></span>
<span data-ttu-id="7a53f-125">Bu parametre 1-300 karakter uzunluğunda olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="7a53f-125">This parameter must be 1 to 300 characters long.</span></span>

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

### <span data-ttu-id="7a53f-126">-Secondaryanahtarı</span><span class="sxs-lookup"><span data-stu-id="7a53f-126">-SecondaryKey</span></span>
<span data-ttu-id="7a53f-127">Abonelik ikincil anahtarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7a53f-127">Specifies the subscription secondary key.</span></span>
<span data-ttu-id="7a53f-128">Bu parametre belirtilmemişse otomatik olarak oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="7a53f-128">This parameter is generated automatically if not specified.</span></span>
<span data-ttu-id="7a53f-129">Bu parametre 1-300 karakter uzunluğunda olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="7a53f-129">This parameter must be 1 to 300 characters long.</span></span>

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

### <span data-ttu-id="7a53f-130">Durumlu</span><span class="sxs-lookup"><span data-stu-id="7a53f-130">-State</span></span>
<span data-ttu-id="7a53f-131">Abonelik durumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="7a53f-131">Specifies the subscription state.</span></span>
<span data-ttu-id="7a53f-132">Bu parametrenin varsayılan değeri $Null.</span><span class="sxs-lookup"><span data-stu-id="7a53f-132">The default value of this parameter is $Null.</span></span>

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

### <span data-ttu-id="7a53f-133">-StateComment</span><span class="sxs-lookup"><span data-stu-id="7a53f-133">-StateComment</span></span>
<span data-ttu-id="7a53f-134">Abonelik durumu açıklamasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7a53f-134">Specifies the subscription state comment.</span></span>
<span data-ttu-id="7a53f-135">Bu parametrenin varsayılan değeri $Null.</span><span class="sxs-lookup"><span data-stu-id="7a53f-135">The default value of this parameter is $Null.</span></span>

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

### <span data-ttu-id="7a53f-136">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="7a53f-136">-SubscriptionId</span></span>
<span data-ttu-id="7a53f-137">Abonelik KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="7a53f-137">Specifies the subscription ID.</span></span>

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

### <span data-ttu-id="7a53f-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a53f-138">CommonParameters</span></span>
<span data-ttu-id="7a53f-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7a53f-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a53f-140">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7a53f-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a53f-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7a53f-141">INPUTS</span></span>

### <span data-ttu-id="7a53f-142">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="7a53f-142">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="7a53f-143">System. String</span><span class="sxs-lookup"><span data-stu-id="7a53f-143">System.String</span></span>

### <span data-ttu-id="7a53f-144">System. Nullable ' 1 [[Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementsubscriptionstate, Microsoft. Azure. PowerShell. cmdlet</span><span class="sxs-lookup"><span data-stu-id="7a53f-144">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscriptionState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="7a53f-145">System. Nullable ' 1 [[System. DATETIME, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]</span><span class="sxs-lookup"><span data-stu-id="7a53f-145">System.Nullable\`1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="7a53f-146">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="7a53f-146">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="7a53f-147">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7a53f-147">OUTPUTS</span></span>

### <span data-ttu-id="7a53f-148">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementsubscription</span><span class="sxs-lookup"><span data-stu-id="7a53f-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription</span></span>

## <span data-ttu-id="7a53f-149">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7a53f-149">NOTES</span></span>

## <span data-ttu-id="7a53f-150">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7a53f-150">RELATED LINKS</span></span>

[<span data-ttu-id="7a53f-151">Get-Azapsananagementsubscription</span><span class="sxs-lookup"><span data-stu-id="7a53f-151">Get-AzApiManagementSubscription</span></span>](./Get-AzApiManagementSubscription.md)

[<span data-ttu-id="7a53f-152">Yeni-Azsız abonelik</span><span class="sxs-lookup"><span data-stu-id="7a53f-152">New-AzApiManagementSubscription</span></span>](./New-AzApiManagementSubscription.md)

[<span data-ttu-id="7a53f-153">Remove-Azapsananagementsubscription</span><span class="sxs-lookup"><span data-stu-id="7a53f-153">Remove-AzApiManagementSubscription</span></span>](./Remove-AzApiManagementSubscription.md)


