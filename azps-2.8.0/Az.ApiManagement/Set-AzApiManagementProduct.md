---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 223FBBA6-4405-4B7A-BA63-5F2434A2A50D
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementProduct.md
ms.openlocfilehash: a4c25514f955b4ea380458cdb1ef845d7b54eb28
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753403"
---
# <span data-ttu-id="61f89-101">Set-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="61f89-101">Set-AzApiManagementProduct</span></span>

## <span data-ttu-id="61f89-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="61f89-102">SYNOPSIS</span></span>
<span data-ttu-id="61f89-103">API yönetimi ürün ayrıntılarını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="61f89-103">Sets the API Management product details.</span></span>

## <span data-ttu-id="61f89-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="61f89-104">SYNTAX</span></span>

```
Set-AzApiManagementProduct -Context <PsApiManagementContext> -ProductId <String> [-Title <String>]
 [-Description <String>] [-LegalTerms <String>] [-SubscriptionRequired <Boolean>] [-ApprovalRequired <Boolean>]
 [-SubscriptionsLimit <Int32>] [-State <PsApiManagementProductState>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="61f89-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="61f89-105">DESCRIPTION</span></span>
<span data-ttu-id="61f89-106">**Set-Azapsananagementproduct** CMDLET 'ı API yönetimi ürün ayrıntılarını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="61f89-106">The **Set-AzApiManagementProduct** cmdlet sets the API Management product details.</span></span>

## <span data-ttu-id="61f89-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="61f89-107">EXAMPLES</span></span>

### <span data-ttu-id="61f89-108">Örnek 1: ürün ayrıntılarını güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="61f89-108">Example 1: Update the product details</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementProduct -Context $apimContext -ProductId "0123456789" -Title "Starter" -Description "Starter Product" -LegalTerms "Free for all" -SubscriptionRequired $True -State "NotPublished"
```

<span data-ttu-id="61f89-109">Bu komut API yönetimi ürün ayrıntılarını güncelleştirir, bir abonelik gerektirir ve sonra yayımdan kaldırın.</span><span class="sxs-lookup"><span data-stu-id="61f89-109">This command updates the API Management product details, requires a subscription, and then unpublishes.</span></span>

## <span data-ttu-id="61f89-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="61f89-110">PARAMETERS</span></span>

### <span data-ttu-id="61f89-111">-ApprovalRequired</span><span class="sxs-lookup"><span data-stu-id="61f89-111">-ApprovalRequired</span></span>
<span data-ttu-id="61f89-112">Ürün aboneliğinin onaylanması gerekip gerekmediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="61f89-112">Indicates whether the subscription to the product requires approval.</span></span>
<span data-ttu-id="61f89-113">Varsayılan değer **$false**.</span><span class="sxs-lookup"><span data-stu-id="61f89-113">The default value is **$False**.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61f89-114">-Context</span><span class="sxs-lookup"><span data-stu-id="61f89-114">-Context</span></span>
<span data-ttu-id="61f89-115">**Psapimanagementcontext** nesnesinin bir örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="61f89-115">Specifies an instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="61f89-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61f89-116">-DefaultProfile</span></span>
<span data-ttu-id="61f89-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="61f89-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="61f89-118">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="61f89-118">-Description</span></span>
<span data-ttu-id="61f89-119">Ürün açıklamasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="61f89-119">Specifies the product description.</span></span>

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

### <span data-ttu-id="61f89-120">-Yasalda MS</span><span class="sxs-lookup"><span data-stu-id="61f89-120">-LegalTerms</span></span>
<span data-ttu-id="61f89-121">Ürünün yasal kullanım şartlarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="61f89-121">Specifies the legal terms of use of the product.</span></span>

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

### <span data-ttu-id="61f89-122">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="61f89-122">-PassThru</span></span>
<span data-ttu-id="61f89-123">geçiş</span><span class="sxs-lookup"><span data-stu-id="61f89-123">passthru</span></span>

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

### <span data-ttu-id="61f89-124">-ÜrünKimliği</span><span class="sxs-lookup"><span data-stu-id="61f89-124">-ProductId</span></span>
<span data-ttu-id="61f89-125">Var olan ürünün tanımlayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="61f89-125">Specifies the identifier of the existing product.</span></span>

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

### <span data-ttu-id="61f89-126">Durumlu</span><span class="sxs-lookup"><span data-stu-id="61f89-126">-State</span></span>
<span data-ttu-id="61f89-127">Ürün durumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="61f89-127">Specifies the product state.</span></span>
<span data-ttu-id="61f89-128">psdx_paramvalues</span><span class="sxs-lookup"><span data-stu-id="61f89-128">psdx_paramvalues</span></span>
- <span data-ttu-id="61f89-129">Notyayımlanmadı</span><span class="sxs-lookup"><span data-stu-id="61f89-129">NotPublished</span></span>
- <span data-ttu-id="61f89-130">Yayımlanabilir</span><span class="sxs-lookup"><span data-stu-id="61f89-130">Published</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProductState]
Parameter Sets: (All)
Aliases:
Accepted values: NotPublished, Published

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61f89-131">-SubscriptionRequired</span><span class="sxs-lookup"><span data-stu-id="61f89-131">-SubscriptionRequired</span></span>
<span data-ttu-id="61f89-132">Ürünün abonelik gerektirip gerektirmediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="61f89-132">Indicates whether the product requires a subscription.</span></span>
<span data-ttu-id="61f89-133">Bu parametrenin varsayılan değeri **$true**.</span><span class="sxs-lookup"><span data-stu-id="61f89-133">The default value for this parameter is **$True**.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61f89-134">-SubscriptionsLimit</span><span class="sxs-lookup"><span data-stu-id="61f89-134">-SubscriptionsLimit</span></span>
<span data-ttu-id="61f89-135">Eşzamanlı aboneliklerin maksimum sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="61f89-135">Specifies the maximum number of simultaneous subscriptions.</span></span>
<span data-ttu-id="61f89-136">Bu parametre için varsayılan değer 1 ' dir.</span><span class="sxs-lookup"><span data-stu-id="61f89-136">The default value for this parameter is 1.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61f89-137">-Başlık</span><span class="sxs-lookup"><span data-stu-id="61f89-137">-Title</span></span>
<span data-ttu-id="61f89-138">Bu cmdlet kümelerinin ürün başlığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="61f89-138">Specifies the product title this cmdlet sets.</span></span>

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

### <span data-ttu-id="61f89-139">-Onay</span><span class="sxs-lookup"><span data-stu-id="61f89-139">-Confirm</span></span>
<span data-ttu-id="61f89-140">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="61f89-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="61f89-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="61f89-141">-WhatIf</span></span>
<span data-ttu-id="61f89-142">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="61f89-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="61f89-143">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="61f89-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="61f89-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61f89-144">CommonParameters</span></span>
<span data-ttu-id="61f89-145">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="61f89-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61f89-146">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="61f89-146">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61f89-147">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="61f89-147">INPUTS</span></span>

### <span data-ttu-id="61f89-148">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="61f89-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="61f89-149">System. String</span><span class="sxs-lookup"><span data-stu-id="61f89-149">System.String</span></span>

### <span data-ttu-id="61f89-150">System. Nullable ' 1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]</span><span class="sxs-lookup"><span data-stu-id="61f89-150">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="61f89-151">System. Nullable ' 1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]</span><span class="sxs-lookup"><span data-stu-id="61f89-151">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="61f89-152">System. Nullable ' 1 [[Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementproductstate, Microsoft. Azure. PowerShell. cmdlet</span><span class="sxs-lookup"><span data-stu-id="61f89-152">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProductState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="61f89-153">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="61f89-153">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="61f89-154">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="61f89-154">OUTPUTS</span></span>

### <span data-ttu-id="61f89-155">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementproduct</span><span class="sxs-lookup"><span data-stu-id="61f89-155">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProduct</span></span>

## <span data-ttu-id="61f89-156">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="61f89-156">NOTES</span></span>

## <span data-ttu-id="61f89-157">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="61f89-157">RELATED LINKS</span></span>

[<span data-ttu-id="61f89-158">Get-Azapsanana,</span><span class="sxs-lookup"><span data-stu-id="61f89-158">Get-AzApiManagementProduct</span></span>](./Get-AzApiManagementProduct.md)

[<span data-ttu-id="61f89-159">Yeni-Azsız ürün</span><span class="sxs-lookup"><span data-stu-id="61f89-159">New-AzApiManagementProduct</span></span>](./New-AzApiManagementProduct.md)

[<span data-ttu-id="61f89-160">Remove-Azapsananagementproduct</span><span class="sxs-lookup"><span data-stu-id="61f89-160">Remove-AzApiManagementProduct</span></span>](./Remove-AzApiManagementProduct.md)


