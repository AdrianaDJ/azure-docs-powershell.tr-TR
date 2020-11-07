---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 223FBBA6-4405-4B7A-BA63-5F2434A2A50D
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementProduct.md
ms.openlocfilehash: f60bf40cd6226979955f71e413be3914fc05c417
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93917668"
---
# <span data-ttu-id="ddc4f-101">Set-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="ddc4f-101">Set-AzApiManagementProduct</span></span>

## <span data-ttu-id="ddc4f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ddc4f-102">SYNOPSIS</span></span>
<span data-ttu-id="ddc4f-103">API yönetimi ürün ayrıntılarını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="ddc4f-103">Sets the API Management product details.</span></span>

## <span data-ttu-id="ddc4f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ddc4f-104">SYNTAX</span></span>

```
Set-AzApiManagementProduct -Context <PsApiManagementContext> -ProductId <String> [-Title <String>]
 [-Description <String>] [-LegalTerms <String>] [-SubscriptionRequired <Boolean>] [-ApprovalRequired <Boolean>]
 [-SubscriptionsLimit <Int32>] [-State <PsApiManagementProductState>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ddc4f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ddc4f-105">DESCRIPTION</span></span>
<span data-ttu-id="ddc4f-106">**Set-Azapsananagementproduct** CMDLET 'ı API yönetimi ürün ayrıntılarını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="ddc4f-106">The **Set-AzApiManagementProduct** cmdlet sets the API Management product details.</span></span>

## <span data-ttu-id="ddc4f-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ddc4f-107">EXAMPLES</span></span>

### <span data-ttu-id="ddc4f-108">Örnek 1: ürün ayrıntılarını güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="ddc4f-108">Example 1: Update the product details</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementProduct -Context $apimContext -ProductId "0123456789" -Title "Starter" -Description "Starter Product" -LegalTerms "Free for all" -SubscriptionRequired $True -State "NotPublished"
```

<span data-ttu-id="ddc4f-109">Bu komut API yönetimi ürün ayrıntılarını güncelleştirir, bir abonelik gerektirir ve sonra yayımdan kaldırın.</span><span class="sxs-lookup"><span data-stu-id="ddc4f-109">This command updates the API Management product details, requires a subscription, and then unpublishes.</span></span>

## <span data-ttu-id="ddc4f-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ddc4f-110">PARAMETERS</span></span>

### <span data-ttu-id="ddc4f-111">-ApprovalRequired</span><span class="sxs-lookup"><span data-stu-id="ddc4f-111">-ApprovalRequired</span></span>
<span data-ttu-id="ddc4f-112">Ürün aboneliğinin onaylanması gerekip gerekmediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="ddc4f-112">Indicates whether the subscription to the product requires approval.</span></span>
<span data-ttu-id="ddc4f-113">Varsayılan değer **$false**.</span><span class="sxs-lookup"><span data-stu-id="ddc4f-113">The default value is **$False**.</span></span>

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

### <span data-ttu-id="ddc4f-114">-Context</span><span class="sxs-lookup"><span data-stu-id="ddc4f-114">-Context</span></span>
<span data-ttu-id="ddc4f-115">**Psapimanagementcontext** nesnesinin bir örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ddc4f-115">Specifies an instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="ddc4f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ddc4f-116">-DefaultProfile</span></span>
<span data-ttu-id="ddc4f-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ddc4f-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ddc4f-118">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="ddc4f-118">-Description</span></span>
<span data-ttu-id="ddc4f-119">Ürün açıklamasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ddc4f-119">Specifies the product description.</span></span>

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

### <span data-ttu-id="ddc4f-120">-Yasalda MS</span><span class="sxs-lookup"><span data-stu-id="ddc4f-120">-LegalTerms</span></span>
<span data-ttu-id="ddc4f-121">Ürünün yasal kullanım şartlarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ddc4f-121">Specifies the legal terms of use of the product.</span></span>

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

### <span data-ttu-id="ddc4f-122">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="ddc4f-122">-PassThru</span></span>
<span data-ttu-id="ddc4f-123">geçiş</span><span class="sxs-lookup"><span data-stu-id="ddc4f-123">passthru</span></span>

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

### <span data-ttu-id="ddc4f-124">-ÜrünKimliği</span><span class="sxs-lookup"><span data-stu-id="ddc4f-124">-ProductId</span></span>
<span data-ttu-id="ddc4f-125">Var olan ürünün tanımlayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ddc4f-125">Specifies the identifier of the existing product.</span></span>

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

### <span data-ttu-id="ddc4f-126">Durumlu</span><span class="sxs-lookup"><span data-stu-id="ddc4f-126">-State</span></span>
<span data-ttu-id="ddc4f-127">Ürün durumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="ddc4f-127">Specifies the product state.</span></span>
<span data-ttu-id="ddc4f-128">psdx_paramvalues</span><span class="sxs-lookup"><span data-stu-id="ddc4f-128">psdx_paramvalues</span></span>
- <span data-ttu-id="ddc4f-129">Notyayımlanmadı</span><span class="sxs-lookup"><span data-stu-id="ddc4f-129">NotPublished</span></span>
- <span data-ttu-id="ddc4f-130">Yayımlanabilir</span><span class="sxs-lookup"><span data-stu-id="ddc4f-130">Published</span></span>

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

### <span data-ttu-id="ddc4f-131">-SubscriptionRequired</span><span class="sxs-lookup"><span data-stu-id="ddc4f-131">-SubscriptionRequired</span></span>
<span data-ttu-id="ddc4f-132">Ürünün abonelik gerektirip gerektirmediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="ddc4f-132">Indicates whether the product requires a subscription.</span></span>
<span data-ttu-id="ddc4f-133">Bu parametrenin varsayılan değeri **$true**.</span><span class="sxs-lookup"><span data-stu-id="ddc4f-133">The default value for this parameter is **$True**.</span></span>

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

### <span data-ttu-id="ddc4f-134">-SubscriptionsLimit</span><span class="sxs-lookup"><span data-stu-id="ddc4f-134">-SubscriptionsLimit</span></span>
<span data-ttu-id="ddc4f-135">Eşzamanlı aboneliklerin maksimum sayısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ddc4f-135">Specifies the maximum number of simultaneous subscriptions.</span></span>
<span data-ttu-id="ddc4f-136">Bu parametre için varsayılan değer 1 ' dir.</span><span class="sxs-lookup"><span data-stu-id="ddc4f-136">The default value for this parameter is 1.</span></span>

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

### <span data-ttu-id="ddc4f-137">-Başlık</span><span class="sxs-lookup"><span data-stu-id="ddc4f-137">-Title</span></span>
<span data-ttu-id="ddc4f-138">Bu cmdlet kümelerinin ürün başlığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ddc4f-138">Specifies the product title this cmdlet sets.</span></span>

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

### <span data-ttu-id="ddc4f-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ddc4f-139">CommonParameters</span></span>
<span data-ttu-id="ddc4f-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ddc4f-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ddc4f-141">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ddc4f-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ddc4f-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ddc4f-142">INPUTS</span></span>

### <span data-ttu-id="ddc4f-143">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="ddc4f-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="ddc4f-144">System. String</span><span class="sxs-lookup"><span data-stu-id="ddc4f-144">System.String</span></span>

### <span data-ttu-id="ddc4f-145">System. Nullable ' 1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]</span><span class="sxs-lookup"><span data-stu-id="ddc4f-145">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="ddc4f-146">System. Nullable ' 1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]</span><span class="sxs-lookup"><span data-stu-id="ddc4f-146">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="ddc4f-147">System. Nullable ' 1 [[Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementproductstate, Microsoft. Azure. PowerShell. cmdlet</span><span class="sxs-lookup"><span data-stu-id="ddc4f-147">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProductState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="ddc4f-148">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="ddc4f-148">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="ddc4f-149">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ddc4f-149">OUTPUTS</span></span>

### <span data-ttu-id="ddc4f-150">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementproduct</span><span class="sxs-lookup"><span data-stu-id="ddc4f-150">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProduct</span></span>

## <span data-ttu-id="ddc4f-151">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ddc4f-151">NOTES</span></span>

## <span data-ttu-id="ddc4f-152">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ddc4f-152">RELATED LINKS</span></span>

[<span data-ttu-id="ddc4f-153">Get-Azapsanana,</span><span class="sxs-lookup"><span data-stu-id="ddc4f-153">Get-AzApiManagementProduct</span></span>](./Get-AzApiManagementProduct.md)

[<span data-ttu-id="ddc4f-154">Yeni-Azsız ürün</span><span class="sxs-lookup"><span data-stu-id="ddc4f-154">New-AzApiManagementProduct</span></span>](./New-AzApiManagementProduct.md)

[<span data-ttu-id="ddc4f-155">Remove-Azapsananagementproduct</span><span class="sxs-lookup"><span data-stu-id="ddc4f-155">Remove-AzApiManagementProduct</span></span>](./Remove-AzApiManagementProduct.md)


