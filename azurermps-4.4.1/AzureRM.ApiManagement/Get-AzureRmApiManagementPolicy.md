---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 7BCEB0EF-1A09-4CED-9F34-CE3AB03181A7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementPolicy.md
ms.openlocfilehash: 16eed643397245fa54b2876430042335762ea048
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591252"
---
# <span data-ttu-id="3bb10-101">Get-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="3bb10-101">Get-AzureRmApiManagementPolicy</span></span>

## <span data-ttu-id="3bb10-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3bb10-102">SYNOPSIS</span></span>
<span data-ttu-id="3bb10-103">Belirtilen kapsam ilkesini alır.</span><span class="sxs-lookup"><span data-stu-id="3bb10-103">Gets the specified scope policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3bb10-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3bb10-104">SYNTAX</span></span>

### <span data-ttu-id="3bb10-105">Kiracı düzeyi (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="3bb10-105">Tenant level (Default)</span></span>
```
Get-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3bb10-106">Ürün düzeyi</span><span class="sxs-lookup"><span data-stu-id="3bb10-106">Product level</span></span>
```
Get-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>]
 -ProductId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3bb10-107">API düzeyi</span><span class="sxs-lookup"><span data-stu-id="3bb10-107">API level</span></span>
```
Get-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>]
 -ApiId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3bb10-108">İşlem düzeyi</span><span class="sxs-lookup"><span data-stu-id="3bb10-108">Operation level</span></span>
```
Get-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>]
 -ApiId <String> -OperationId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3bb10-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="3bb10-109">DESCRIPTION</span></span>
<span data-ttu-id="3bb10-110">**Get-Azurermapsananagementpolicy** cmdlet 'i, belirtilen kapsam ilkesini alır.</span><span class="sxs-lookup"><span data-stu-id="3bb10-110">The **Get-AzureRmApiManagementPolicy** cmdlet gets the specified scope policy.</span></span>

## <span data-ttu-id="3bb10-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3bb10-111">EXAMPLES</span></span>

### <span data-ttu-id="3bb10-112">Örnek 1: kiracı düzeyi ilkesini alma</span><span class="sxs-lookup"><span data-stu-id="3bb10-112">Example 1: Get the tenant level policy</span></span>
```
PS C:\>Get-AzureRmApiManagementPolicy -Context $APImContext -SaveAs "C:\contoso\policies\tenantpolicy.xml"
```

<span data-ttu-id="3bb10-113">Bu komut, kiracı düzeyi ilkesini alır ve tenantpolicy.xml adlı bir dosyaya kaydeder.</span><span class="sxs-lookup"><span data-stu-id="3bb10-113">This command gets tenant level policy and saves it to a file named tenantpolicy.xml.</span></span>

### <span data-ttu-id="3bb10-114">Örnek 2: ürün kapsamı ilkesini edinme</span><span class="sxs-lookup"><span data-stu-id="3bb10-114">Example 2: Get the product-scope policy</span></span>
```
PS C:\>Get-AzureRmApiManagementPolicy -Context $APImContext -ProductId "0123456789"
```

<span data-ttu-id="3bb10-115">Bu komut, ürün kapsam ilkesini alır</span><span class="sxs-lookup"><span data-stu-id="3bb10-115">This command gets product-scope policy</span></span>

### <span data-ttu-id="3bb10-116">Örnek 3: API kapsam ilkesini edinme</span><span class="sxs-lookup"><span data-stu-id="3bb10-116">Example 3: Get the API-scope policy</span></span>
```
PS C:\>Get-AzureRmApiManagementPolicy -Context $APImContext -ApiId "9876543210"
```

<span data-ttu-id="3bb10-117">Bu komut API kapsam ilkesini alır.</span><span class="sxs-lookup"><span data-stu-id="3bb10-117">This command gets API-scope policy.</span></span>

### <span data-ttu-id="3bb10-118">Örnek 4: işlem kapsamı ilkesini edinme</span><span class="sxs-lookup"><span data-stu-id="3bb10-118">Example 4: Get the operation-scope policy</span></span>
```
PS C:\>Get-AzureRmApiManagementPolicy -Context $APImContext -ApiId "9876543210" -OperationId "777"
```

<span data-ttu-id="3bb10-119">Bu komut, işlem kapsamı ilkesini alır.</span><span class="sxs-lookup"><span data-stu-id="3bb10-119">This command gets the operation-scope policy.</span></span>

## <span data-ttu-id="3bb10-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3bb10-120">PARAMETERS</span></span>

### <span data-ttu-id="3bb10-121">-Apııd</span><span class="sxs-lookup"><span data-stu-id="3bb10-121">-ApiId</span></span>
<span data-ttu-id="3bb10-122">Var olan API 'nin tanımlayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3bb10-122">Specifies the identifier of the existing API.</span></span>
<span data-ttu-id="3bb10-123">Bu parametreyi belirtirseniz cmdlet API kapsam ilkesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="3bb10-123">If you specify this parameter the cmdlet returns the API-scope policy.</span></span>

```yaml
Type: System.String
Parameter Sets: API level, Operation level
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3bb10-124">-Context</span><span class="sxs-lookup"><span data-stu-id="3bb10-124">-Context</span></span>
<span data-ttu-id="3bb10-125">**Psapsananagementcontext** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="3bb10-125">Specifies an instance of **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="3bb10-126">-Force</span><span class="sxs-lookup"><span data-stu-id="3bb10-126">-Force</span></span>
<span data-ttu-id="3bb10-127">ps_force</span><span class="sxs-lookup"><span data-stu-id="3bb10-127">ps_force</span></span>

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

### <span data-ttu-id="3bb10-128">Biçimli</span><span class="sxs-lookup"><span data-stu-id="3bb10-128">-Format</span></span>
<span data-ttu-id="3bb10-129">API yönetim ilkesinin biçimini belirtir.</span><span class="sxs-lookup"><span data-stu-id="3bb10-129">Specifies the format of the API management policy.</span></span>
<span data-ttu-id="3bb10-130">Bu parametre için varsayılan değer "application/vnd. MS-Azure-apim. Policy + xml" olur.</span><span class="sxs-lookup"><span data-stu-id="3bb10-130">The default value for this parameter is "application/vnd.ms-azure-apim.policy+xml".</span></span>

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

### <span data-ttu-id="3bb10-131">-OperationId</span><span class="sxs-lookup"><span data-stu-id="3bb10-131">-OperationId</span></span>
<span data-ttu-id="3bb10-132">Var olan API işleminin tanımlayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3bb10-132">Specifies the identifier of the existing API operation.</span></span>
<span data-ttu-id="3bb10-133">Bu parametreyi *Apııd* ile belirtirseniz cmdlet, operasyon kapsam ilkesi döndürüyor.</span><span class="sxs-lookup"><span data-stu-id="3bb10-133">If you specify this parameter with *ApiId* the cmdlet returns operation-scope policy.</span></span>

```yaml
Type: System.String
Parameter Sets: Operation level
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3bb10-134">-ÜrünKimliği</span><span class="sxs-lookup"><span data-stu-id="3bb10-134">-ProductId</span></span>
<span data-ttu-id="3bb10-135">Var olan bir ürünün tanımlayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3bb10-135">Specifies the identifier of an existing product.</span></span>
<span data-ttu-id="3bb10-136">Bu parametreyi belirtirseniz cmdlet, ürün kapsam ilkesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="3bb10-136">If you specify this parameter the cmdlet returns the product-scope policy.</span></span>

```yaml
Type: System.String
Parameter Sets: Product level
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3bb10-137">-SaveAs</span><span class="sxs-lookup"><span data-stu-id="3bb10-137">-SaveAs</span></span>
<span data-ttu-id="3bb10-138">Sonucun kaydedileceği dosya yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="3bb10-138">Specifies the file path to save the result to.</span></span>
<span data-ttu-id="3bb10-139">Bu parametreyi belirtmezseniz, sonuç olarak ardışık düzen gönderilir.</span><span class="sxs-lookup"><span data-stu-id="3bb10-139">If you do not specify this parameter the result is pipelined as a sting.</span></span>

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

### <span data-ttu-id="3bb10-140">-Onay</span><span class="sxs-lookup"><span data-stu-id="3bb10-140">-Confirm</span></span>
<span data-ttu-id="3bb10-141">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="3bb10-141">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bb10-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3bb10-142">-WhatIf</span></span>
<span data-ttu-id="3bb10-143">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="3bb10-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3bb10-144">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="3bb10-144">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3bb10-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3bb10-145">-DefaultProfile</span></span>
<span data-ttu-id="3bb10-146">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3bb10-146">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3bb10-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3bb10-147">CommonParameters</span></span>
<span data-ttu-id="3bb10-148">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3bb10-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3bb10-149">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3bb10-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3bb10-150">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3bb10-150">INPUTS</span></span>

## <span data-ttu-id="3bb10-151">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3bb10-151">OUTPUTS</span></span>

### <span data-ttu-id="3bb10-152">Dizisi</span><span class="sxs-lookup"><span data-stu-id="3bb10-152">String</span></span>

## <span data-ttu-id="3bb10-153">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3bb10-153">NOTES</span></span>

## <span data-ttu-id="3bb10-154">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3bb10-154">RELATED LINKS</span></span>

[<span data-ttu-id="3bb10-155">Remove-Azurermapımanagementpolicy</span><span class="sxs-lookup"><span data-stu-id="3bb10-155">Remove-AzureRmApiManagementPolicy</span></span>](./Remove-AzureRmApiManagementPolicy.md)

[<span data-ttu-id="3bb10-156">Set-Azurermapımanagementpolicy</span><span class="sxs-lookup"><span data-stu-id="3bb10-156">Set-AzureRmApiManagementPolicy</span></span>](./Set-AzureRmApiManagementPolicy.md)


