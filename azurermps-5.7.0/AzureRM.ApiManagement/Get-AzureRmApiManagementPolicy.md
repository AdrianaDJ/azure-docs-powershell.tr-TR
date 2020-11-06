---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 7BCEB0EF-1A09-4CED-9F34-CE3AB03181A7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementPolicy.md
ms.openlocfilehash: 31b38d07aea51ad1e6bd097cc0c9f7f342e1bfb2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589927"
---
# <span data-ttu-id="d8b55-101">Get-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="d8b55-101">Get-AzureRmApiManagementPolicy</span></span>

## <span data-ttu-id="d8b55-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d8b55-102">SYNOPSIS</span></span>
<span data-ttu-id="d8b55-103">Belirtilen kapsam ilkesini alır.</span><span class="sxs-lookup"><span data-stu-id="d8b55-103">Gets the specified scope policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d8b55-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d8b55-104">SYNTAX</span></span>

### <span data-ttu-id="d8b55-105">GetTenantLevel (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="d8b55-105">GetTenantLevel (Default)</span></span>
```
Get-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d8b55-106">GetProductLevel</span><span class="sxs-lookup"><span data-stu-id="d8b55-106">GetProductLevel</span></span>
```
Get-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>]
 -ProductId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d8b55-107">Getapi</span><span class="sxs-lookup"><span data-stu-id="d8b55-107">GetApiLevel</span></span>
```
Get-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>]
 -ApiId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d8b55-108">Getoperationdüzeyi</span><span class="sxs-lookup"><span data-stu-id="d8b55-108">GetOperationLevel</span></span>
```
Get-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>]
 -ApiId <String> -OperationId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d8b55-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="d8b55-109">DESCRIPTION</span></span>
<span data-ttu-id="d8b55-110">**Get-Azurermapsananagementpolicy** cmdlet 'i, belirtilen kapsam ilkesini alır.</span><span class="sxs-lookup"><span data-stu-id="d8b55-110">The **Get-AzureRmApiManagementPolicy** cmdlet gets the specified scope policy.</span></span>

## <span data-ttu-id="d8b55-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d8b55-111">EXAMPLES</span></span>

### <span data-ttu-id="d8b55-112">Örnek 1: kiracı düzeyi ilkesini alma</span><span class="sxs-lookup"><span data-stu-id="d8b55-112">Example 1: Get the tenant level policy</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementPolicy -Context $apimContext -SaveAs "C:\contoso\policies\tenantpolicy.xml"
```

<span data-ttu-id="d8b55-113">Bu komut, kiracı düzeyi ilkesini alır ve tenantpolicy.xml adlı bir dosyaya kaydeder.</span><span class="sxs-lookup"><span data-stu-id="d8b55-113">This command gets tenant level policy and saves it to a file named tenantpolicy.xml.</span></span>

### <span data-ttu-id="d8b55-114">Örnek 2: ürün kapsamı ilkesini edinme</span><span class="sxs-lookup"><span data-stu-id="d8b55-114">Example 2: Get the product-scope policy</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementPolicy -Context $apimContext -ProductId "0123456789"
```

<span data-ttu-id="d8b55-115">Bu komut, ürün kapsam ilkesini alır</span><span class="sxs-lookup"><span data-stu-id="d8b55-115">This command gets product-scope policy</span></span>

### <span data-ttu-id="d8b55-116">Örnek 3: API kapsam ilkesini edinme</span><span class="sxs-lookup"><span data-stu-id="d8b55-116">Example 3: Get the API-scope policy</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementPolicy -Context $apimContext -ApiId "9876543210"
```

<span data-ttu-id="d8b55-117">Bu komut API kapsam ilkesini alır.</span><span class="sxs-lookup"><span data-stu-id="d8b55-117">This command gets API-scope policy.</span></span>

### <span data-ttu-id="d8b55-118">Örnek 4: işlem kapsamı ilkesini edinme</span><span class="sxs-lookup"><span data-stu-id="d8b55-118">Example 4: Get the operation-scope policy</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementPolicy -Context $apimContext -ApiId "9876543210" -OperationId "777"
```

<span data-ttu-id="d8b55-119">Bu komut, işlem kapsamı ilkesini alır.</span><span class="sxs-lookup"><span data-stu-id="d8b55-119">This command gets the operation-scope policy.</span></span>

## <span data-ttu-id="d8b55-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d8b55-120">PARAMETERS</span></span>

### <span data-ttu-id="d8b55-121">-Apııd</span><span class="sxs-lookup"><span data-stu-id="d8b55-121">-ApiId</span></span>
<span data-ttu-id="d8b55-122">Var olan API 'nin tanımlayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d8b55-122">Specifies the identifier of the existing API.</span></span>
<span data-ttu-id="d8b55-123">Bu parametreyi belirtirseniz cmdlet API kapsam ilkesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="d8b55-123">If you specify this parameter the cmdlet returns the API-scope policy.</span></span>

```yaml
Type: String
Parameter Sets: GetApiLevel, GetOperationLevel
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8b55-124">-Context</span><span class="sxs-lookup"><span data-stu-id="d8b55-124">-Context</span></span>
<span data-ttu-id="d8b55-125">**Psapsananagementcontext** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="d8b55-125">Specifies an instance of **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="d8b55-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8b55-126">-DefaultProfile</span></span>
<span data-ttu-id="d8b55-127">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d8b55-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="d8b55-128">-Force</span><span class="sxs-lookup"><span data-stu-id="d8b55-128">-Force</span></span>
<span data-ttu-id="d8b55-129">ps_force</span><span class="sxs-lookup"><span data-stu-id="d8b55-129">ps_force</span></span>

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

### <span data-ttu-id="d8b55-130">Biçimli</span><span class="sxs-lookup"><span data-stu-id="d8b55-130">-Format</span></span>
<span data-ttu-id="d8b55-131">API yönetim ilkesinin biçimini belirtir.</span><span class="sxs-lookup"><span data-stu-id="d8b55-131">Specifies the format of the API management policy.</span></span>
<span data-ttu-id="d8b55-132">Bu parametre için varsayılan değer "application/vnd. MS-Azure-apim. Policy + xml" olur.</span><span class="sxs-lookup"><span data-stu-id="d8b55-132">The default value for this parameter is "application/vnd.ms-azure-apim.policy+xml".</span></span>

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

### <span data-ttu-id="d8b55-133">-OperationId</span><span class="sxs-lookup"><span data-stu-id="d8b55-133">-OperationId</span></span>
<span data-ttu-id="d8b55-134">Var olan API işleminin tanımlayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d8b55-134">Specifies the identifier of the existing API operation.</span></span>
<span data-ttu-id="d8b55-135">Bu parametreyi *Apııd* ile belirtirseniz cmdlet, operasyon kapsam ilkesi döndürüyor.</span><span class="sxs-lookup"><span data-stu-id="d8b55-135">If you specify this parameter with *ApiId* the cmdlet returns operation-scope policy.</span></span>

```yaml
Type: String
Parameter Sets: GetOperationLevel
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8b55-136">-ÜrünKimliği</span><span class="sxs-lookup"><span data-stu-id="d8b55-136">-ProductId</span></span>
<span data-ttu-id="d8b55-137">Var olan bir ürünün tanımlayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d8b55-137">Specifies the identifier of an existing product.</span></span>
<span data-ttu-id="d8b55-138">Bu parametreyi belirtirseniz cmdlet, ürün kapsam ilkesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="d8b55-138">If you specify this parameter the cmdlet returns the product-scope policy.</span></span>

```yaml
Type: String
Parameter Sets: GetProductLevel
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8b55-139">-SaveAs</span><span class="sxs-lookup"><span data-stu-id="d8b55-139">-SaveAs</span></span>
<span data-ttu-id="d8b55-140">Sonucun kaydedileceği dosya yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="d8b55-140">Specifies the file path to save the result to.</span></span>
<span data-ttu-id="d8b55-141">Bu parametreyi belirtmezseniz, sonuç olarak ardışık düzen gönderilir.</span><span class="sxs-lookup"><span data-stu-id="d8b55-141">If you do not specify this parameter the result is pipelined as a sting.</span></span>

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

### <span data-ttu-id="d8b55-142">-Onay</span><span class="sxs-lookup"><span data-stu-id="d8b55-142">-Confirm</span></span>
<span data-ttu-id="d8b55-143">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d8b55-143">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8b55-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d8b55-144">-WhatIf</span></span>
<span data-ttu-id="d8b55-145">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d8b55-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d8b55-146">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d8b55-146">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8b55-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8b55-147">CommonParameters</span></span>
<span data-ttu-id="d8b55-148">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d8b55-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8b55-149">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8b55-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8b55-150">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d8b55-150">INPUTS</span></span>

### <span data-ttu-id="d8b55-151">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="d8b55-151">None</span></span>
<span data-ttu-id="d8b55-152">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="d8b55-152">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d8b55-153">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d8b55-153">OUTPUTS</span></span>

### <span data-ttu-id="d8b55-154">Dizisi</span><span class="sxs-lookup"><span data-stu-id="d8b55-154">String</span></span>

## <span data-ttu-id="d8b55-155">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d8b55-155">NOTES</span></span>

## <span data-ttu-id="d8b55-156">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d8b55-156">RELATED LINKS</span></span>

[<span data-ttu-id="d8b55-157">Remove-Azurermapımanagementpolicy</span><span class="sxs-lookup"><span data-stu-id="d8b55-157">Remove-AzureRmApiManagementPolicy</span></span>](./Remove-AzureRmApiManagementPolicy.md)

[<span data-ttu-id="d8b55-158">Set-Azurermapımanagementpolicy</span><span class="sxs-lookup"><span data-stu-id="d8b55-158">Set-AzureRmApiManagementPolicy</span></span>](./Set-AzureRmApiManagementPolicy.md)


