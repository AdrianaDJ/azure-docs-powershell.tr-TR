---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 7BCEB0EF-1A09-4CED-9F34-CE3AB03181A7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementPolicy.md
ms.openlocfilehash: fcf88fcb9b54adec01b8a04b50f557b6a74e7ca8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573098"
---
# <span data-ttu-id="3d3dc-101">Get-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="3d3dc-101">Get-AzureRmApiManagementPolicy</span></span>

## <span data-ttu-id="3d3dc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3d3dc-102">SYNOPSIS</span></span>
<span data-ttu-id="3d3dc-103">Belirtilen kapsam ilkesini alır.</span><span class="sxs-lookup"><span data-stu-id="3d3dc-103">Gets the specified scope policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3d3dc-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3d3dc-104">SYNTAX</span></span>

### <span data-ttu-id="3d3dc-105">GetTenantLevel (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="3d3dc-105">GetTenantLevel (Default)</span></span>
```
Get-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3d3dc-106">GetProductLevel</span><span class="sxs-lookup"><span data-stu-id="3d3dc-106">GetProductLevel</span></span>
```
Get-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>]
 -ProductId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3d3dc-107">Getapi</span><span class="sxs-lookup"><span data-stu-id="3d3dc-107">GetApiLevel</span></span>
```
Get-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>]
 -ApiId <String> [-ApiRevision <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3d3dc-108">Getoperationdüzeyi</span><span class="sxs-lookup"><span data-stu-id="3d3dc-108">GetOperationLevel</span></span>
```
Get-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>]
 -ApiId <String> [-ApiRevision <String>] -OperationId <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3d3dc-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="3d3dc-109">DESCRIPTION</span></span>
<span data-ttu-id="3d3dc-110">**Get-Azurermapsananagementpolicy** cmdlet 'i, belirtilen kapsam ilkesini alır.</span><span class="sxs-lookup"><span data-stu-id="3d3dc-110">The **Get-AzureRmApiManagementPolicy** cmdlet gets the specified scope policy.</span></span>

## <span data-ttu-id="3d3dc-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3d3dc-111">EXAMPLES</span></span>

### <span data-ttu-id="3d3dc-112">Örnek 1: kiracı düzeyi ilkesini alma</span><span class="sxs-lookup"><span data-stu-id="3d3dc-112">Example 1: Get the tenant level policy</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementPolicy -Context $apimContext -SaveAs "C:\contoso\policies\tenantpolicy.xml"
```

<span data-ttu-id="3d3dc-113">Bu komut, kiracı düzeyi ilkesini alır ve tenantpolicy.xml adlı bir dosyaya kaydeder.</span><span class="sxs-lookup"><span data-stu-id="3d3dc-113">This command gets tenant level policy and saves it to a file named tenantpolicy.xml.</span></span>

### <span data-ttu-id="3d3dc-114">Örnek 2: ürün kapsamı ilkesini edinme</span><span class="sxs-lookup"><span data-stu-id="3d3dc-114">Example 2: Get the product-scope policy</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementPolicy -Context $apimContext -ProductId "0123456789"
```

<span data-ttu-id="3d3dc-115">Bu komut, ürün kapsam ilkesini alır</span><span class="sxs-lookup"><span data-stu-id="3d3dc-115">This command gets product-scope policy</span></span>

### <span data-ttu-id="3d3dc-116">Örnek 3: API kapsam ilkesini edinme</span><span class="sxs-lookup"><span data-stu-id="3d3dc-116">Example 3: Get the API-scope policy</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementPolicy -Context $apimContext -ApiId "9876543210"
```

<span data-ttu-id="3d3dc-117">Bu komut API kapsam ilkesini alır.</span><span class="sxs-lookup"><span data-stu-id="3d3dc-117">This command gets API-scope policy.</span></span>

### <span data-ttu-id="3d3dc-118">Örnek 4: işlem kapsamı ilkesini edinme</span><span class="sxs-lookup"><span data-stu-id="3d3dc-118">Example 4: Get the operation-scope policy</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementPolicy -Context $apimContext -ApiId "9876543210" -OperationId "777"
```

<span data-ttu-id="3d3dc-119">Bu komut, işlem kapsamı ilkesini alır.</span><span class="sxs-lookup"><span data-stu-id="3d3dc-119">This command gets the operation-scope policy.</span></span>

## <span data-ttu-id="3d3dc-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3d3dc-120">PARAMETERS</span></span>

### <span data-ttu-id="3d3dc-121">-Apııd</span><span class="sxs-lookup"><span data-stu-id="3d3dc-121">-ApiId</span></span>
<span data-ttu-id="3d3dc-122">Var olan API 'nin tanımlayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3d3dc-122">Specifies the identifier of the existing API.</span></span>
<span data-ttu-id="3d3dc-123">Bu parametreyi belirtirseniz cmdlet API kapsam ilkesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="3d3dc-123">If you specify this parameter the cmdlet returns the API-scope policy.</span></span>

```yaml
Type: System.String
Parameter Sets: GetApiLevel, GetOperationLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d3dc-124">-Apırevision</span><span class="sxs-lookup"><span data-stu-id="3d3dc-124">-ApiRevision</span></span>
<span data-ttu-id="3d3dc-125">API düzeltme tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="3d3dc-125">Identifier of API Revision.</span></span> <span data-ttu-id="3d3dc-126">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="3d3dc-126">This parameter is optional.</span></span> <span data-ttu-id="3d3dc-127">Belirtilmemişse, ilke geçerli etkin API düzeltmesidir.</span><span class="sxs-lookup"><span data-stu-id="3d3dc-127">If not specified, the policy will be retrieved from the currently active api revision.</span></span>

```yaml
Type: System.String
Parameter Sets: GetApiLevel, GetOperationLevel
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d3dc-128">-Context</span><span class="sxs-lookup"><span data-stu-id="3d3dc-128">-Context</span></span>
<span data-ttu-id="3d3dc-129">**Psapsananagementcontext** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="3d3dc-129">Specifies an instance of **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="3d3dc-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d3dc-130">-DefaultProfile</span></span>
<span data-ttu-id="3d3dc-131">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3d3dc-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3d3dc-132">-Force</span><span class="sxs-lookup"><span data-stu-id="3d3dc-132">-Force</span></span>
<span data-ttu-id="3d3dc-133">ps_force</span><span class="sxs-lookup"><span data-stu-id="3d3dc-133">ps_force</span></span>

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

### <span data-ttu-id="3d3dc-134">Biçimli</span><span class="sxs-lookup"><span data-stu-id="3d3dc-134">-Format</span></span>
<span data-ttu-id="3d3dc-135">API yönetim ilkesinin biçimini belirtir.</span><span class="sxs-lookup"><span data-stu-id="3d3dc-135">Specifies the format of the API management policy.</span></span>
<span data-ttu-id="3d3dc-136">Bu parametre için varsayılan değer "application/vnd. MS-Azure-apim. Policy + xml" olur.</span><span class="sxs-lookup"><span data-stu-id="3d3dc-136">The default value for this parameter is "application/vnd.ms-azure-apim.policy+xml".</span></span>

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

### <span data-ttu-id="3d3dc-137">-OperationId</span><span class="sxs-lookup"><span data-stu-id="3d3dc-137">-OperationId</span></span>
<span data-ttu-id="3d3dc-138">Var olan API işleminin tanımlayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3d3dc-138">Specifies the identifier of the existing API operation.</span></span>
<span data-ttu-id="3d3dc-139">Bu parametreyi *Apııd* ile belirtirseniz cmdlet, operasyon kapsam ilkesi döndürüyor.</span><span class="sxs-lookup"><span data-stu-id="3d3dc-139">If you specify this parameter with *ApiId* the cmdlet returns operation-scope policy.</span></span>

```yaml
Type: System.String
Parameter Sets: GetOperationLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d3dc-140">-ÜrünKimliği</span><span class="sxs-lookup"><span data-stu-id="3d3dc-140">-ProductId</span></span>
<span data-ttu-id="3d3dc-141">Var olan bir ürünün tanımlayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3d3dc-141">Specifies the identifier of an existing product.</span></span>
<span data-ttu-id="3d3dc-142">Bu parametreyi belirtirseniz cmdlet, ürün kapsam ilkesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="3d3dc-142">If you specify this parameter the cmdlet returns the product-scope policy.</span></span>

```yaml
Type: System.String
Parameter Sets: GetProductLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d3dc-143">-SaveAs</span><span class="sxs-lookup"><span data-stu-id="3d3dc-143">-SaveAs</span></span>
<span data-ttu-id="3d3dc-144">Sonucun kaydedileceği dosya yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="3d3dc-144">Specifies the file path to save the result to.</span></span>
<span data-ttu-id="3d3dc-145">Bu parametreyi belirtmezseniz, sonuç olarak ardışık düzen gönderilir.</span><span class="sxs-lookup"><span data-stu-id="3d3dc-145">If you do not specify this parameter the result is pipelined as a sting.</span></span>

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

### <span data-ttu-id="3d3dc-146">-Onay</span><span class="sxs-lookup"><span data-stu-id="3d3dc-146">-Confirm</span></span>
<span data-ttu-id="3d3dc-147">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="3d3dc-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3d3dc-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3d3dc-148">-WhatIf</span></span>
<span data-ttu-id="3d3dc-149">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="3d3dc-149">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3d3dc-150">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="3d3dc-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3d3dc-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d3dc-151">CommonParameters</span></span>
<span data-ttu-id="3d3dc-152">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3d3dc-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d3dc-153">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3d3dc-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d3dc-154">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3d3dc-154">INPUTS</span></span>

### <span data-ttu-id="3d3dc-155">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="3d3dc-155">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="3d3dc-156">System. String</span><span class="sxs-lookup"><span data-stu-id="3d3dc-156">System.String</span></span>

### <span data-ttu-id="3d3dc-157">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="3d3dc-157">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="3d3dc-158">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3d3dc-158">OUTPUTS</span></span>

### <span data-ttu-id="3d3dc-159">System. String</span><span class="sxs-lookup"><span data-stu-id="3d3dc-159">System.String</span></span>

## <span data-ttu-id="3d3dc-160">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3d3dc-160">NOTES</span></span>

## <span data-ttu-id="3d3dc-161">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3d3dc-161">RELATED LINKS</span></span>

[<span data-ttu-id="3d3dc-162">Remove-Azurermapımanagementpolicy</span><span class="sxs-lookup"><span data-stu-id="3d3dc-162">Remove-AzureRmApiManagementPolicy</span></span>](./Remove-AzureRmApiManagementPolicy.md)

[<span data-ttu-id="3d3dc-163">Set-Azurermapımanagementpolicy</span><span class="sxs-lookup"><span data-stu-id="3d3dc-163">Set-AzureRmApiManagementPolicy</span></span>](./Set-AzureRmApiManagementPolicy.md)


