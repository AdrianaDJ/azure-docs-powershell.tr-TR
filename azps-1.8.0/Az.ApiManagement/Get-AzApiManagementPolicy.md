---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 7BCEB0EF-1A09-4CED-9F34-CE3AB03181A7
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementPolicy.md
ms.openlocfilehash: 0da4e2168ccc7f5a62aa4265af3b7823dd4cb050
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93751156"
---
# <span data-ttu-id="1fb42-101">Get-AzApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="1fb42-101">Get-AzApiManagementPolicy</span></span>

## <span data-ttu-id="1fb42-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1fb42-102">SYNOPSIS</span></span>
<span data-ttu-id="1fb42-103">Belirtilen kapsam ilkesini alır.</span><span class="sxs-lookup"><span data-stu-id="1fb42-103">Gets the specified scope policy.</span></span>

## <span data-ttu-id="1fb42-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1fb42-104">SYNTAX</span></span>

### <span data-ttu-id="1fb42-105">GetTenantLevel (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="1fb42-105">GetTenantLevel (Default)</span></span>
```
Get-AzApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1fb42-106">GetProductLevel</span><span class="sxs-lookup"><span data-stu-id="1fb42-106">GetProductLevel</span></span>
```
Get-AzApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>]
 -ProductId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1fb42-107">Getapi</span><span class="sxs-lookup"><span data-stu-id="1fb42-107">GetApiLevel</span></span>
```
Get-AzApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>]
 -ApiId <String> [-ApiRevision <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1fb42-108">Getoperationdüzeyi</span><span class="sxs-lookup"><span data-stu-id="1fb42-108">GetOperationLevel</span></span>
```
Get-AzApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>]
 -ApiId <String> [-ApiRevision <String>] -OperationId <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1fb42-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="1fb42-109">DESCRIPTION</span></span>
<span data-ttu-id="1fb42-110">**Get-Azapsananagementpolicy** cmdlet 'i, belirtilen kapsam ilkesini alır.</span><span class="sxs-lookup"><span data-stu-id="1fb42-110">The **Get-AzApiManagementPolicy** cmdlet gets the specified scope policy.</span></span>

## <span data-ttu-id="1fb42-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1fb42-111">EXAMPLES</span></span>

### <span data-ttu-id="1fb42-112">Örnek 1: kiracı düzeyi ilkesini alma</span><span class="sxs-lookup"><span data-stu-id="1fb42-112">Example 1: Get the tenant level policy</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementPolicy -Context $apimContext -SaveAs "C:\contoso\policies\tenantpolicy.xml"
```

<span data-ttu-id="1fb42-113">Bu komut, kiracı düzeyi ilkesini alır ve tenantpolicy.xml adlı bir dosyaya kaydeder.</span><span class="sxs-lookup"><span data-stu-id="1fb42-113">This command gets tenant level policy and saves it to a file named tenantpolicy.xml.</span></span>

### <span data-ttu-id="1fb42-114">Örnek 2: ürün kapsamı ilkesini edinme</span><span class="sxs-lookup"><span data-stu-id="1fb42-114">Example 2: Get the product-scope policy</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementPolicy -Context $apimContext -ProductId "0123456789"
```

<span data-ttu-id="1fb42-115">Bu komut, ürün kapsam ilkesini alır</span><span class="sxs-lookup"><span data-stu-id="1fb42-115">This command gets product-scope policy</span></span>

### <span data-ttu-id="1fb42-116">Örnek 3: API kapsam ilkesini edinme</span><span class="sxs-lookup"><span data-stu-id="1fb42-116">Example 3: Get the API-scope policy</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementPolicy -Context $apimContext -ApiId "9876543210"
```

<span data-ttu-id="1fb42-117">Bu komut API kapsam ilkesini alır.</span><span class="sxs-lookup"><span data-stu-id="1fb42-117">This command gets API-scope policy.</span></span>

### <span data-ttu-id="1fb42-118">Örnek 4: işlem kapsamı ilkesini edinme</span><span class="sxs-lookup"><span data-stu-id="1fb42-118">Example 4: Get the operation-scope policy</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementPolicy -Context $apimContext -ApiId "9876543210" -OperationId "777"
```

<span data-ttu-id="1fb42-119">Bu komut, işlem kapsamı ilkesini alır.</span><span class="sxs-lookup"><span data-stu-id="1fb42-119">This command gets the operation-scope policy.</span></span>

## <span data-ttu-id="1fb42-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1fb42-120">PARAMETERS</span></span>

### <span data-ttu-id="1fb42-121">-Apııd</span><span class="sxs-lookup"><span data-stu-id="1fb42-121">-ApiId</span></span>
<span data-ttu-id="1fb42-122">Var olan API 'nin tanımlayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1fb42-122">Specifies the identifier of the existing API.</span></span>
<span data-ttu-id="1fb42-123">Bu parametreyi belirtirseniz cmdlet API kapsam ilkesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="1fb42-123">If you specify this parameter the cmdlet returns the API-scope policy.</span></span>

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

### <span data-ttu-id="1fb42-124">-Apırevision</span><span class="sxs-lookup"><span data-stu-id="1fb42-124">-ApiRevision</span></span>
<span data-ttu-id="1fb42-125">API düzeltme tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="1fb42-125">Identifier of API Revision.</span></span> <span data-ttu-id="1fb42-126">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="1fb42-126">This parameter is optional.</span></span> <span data-ttu-id="1fb42-127">Belirtilmemişse, ilke geçerli etkin API düzeltmesidir.</span><span class="sxs-lookup"><span data-stu-id="1fb42-127">If not specified, the policy will be retrieved from the currently active api revision.</span></span>

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

### <span data-ttu-id="1fb42-128">-Context</span><span class="sxs-lookup"><span data-stu-id="1fb42-128">-Context</span></span>
<span data-ttu-id="1fb42-129">**Psapsananagementcontext** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="1fb42-129">Specifies an instance of **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="1fb42-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1fb42-130">-DefaultProfile</span></span>
<span data-ttu-id="1fb42-131">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1fb42-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1fb42-132">-Force</span><span class="sxs-lookup"><span data-stu-id="1fb42-132">-Force</span></span>
<span data-ttu-id="1fb42-133">ps_force</span><span class="sxs-lookup"><span data-stu-id="1fb42-133">ps_force</span></span>

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

### <span data-ttu-id="1fb42-134">Biçimli</span><span class="sxs-lookup"><span data-stu-id="1fb42-134">-Format</span></span>
<span data-ttu-id="1fb42-135">API yönetim ilkesinin biçimini belirtir.</span><span class="sxs-lookup"><span data-stu-id="1fb42-135">Specifies the format of the API management policy.</span></span>
<span data-ttu-id="1fb42-136">Bu parametre için varsayılan değer "application/vnd. MS-az-apim. Policy + xml" olur.</span><span class="sxs-lookup"><span data-stu-id="1fb42-136">The default value for this parameter is "application/vnd.ms-az-apim.policy+xml".</span></span>

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

### <span data-ttu-id="1fb42-137">-OperationId</span><span class="sxs-lookup"><span data-stu-id="1fb42-137">-OperationId</span></span>
<span data-ttu-id="1fb42-138">Var olan API işleminin tanımlayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1fb42-138">Specifies the identifier of the existing API operation.</span></span>
<span data-ttu-id="1fb42-139">Bu parametreyi *Apııd* ile belirtirseniz cmdlet, operasyon kapsam ilkesi döndürüyor.</span><span class="sxs-lookup"><span data-stu-id="1fb42-139">If you specify this parameter with *ApiId* the cmdlet returns operation-scope policy.</span></span>

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

### <span data-ttu-id="1fb42-140">-ÜrünKimliği</span><span class="sxs-lookup"><span data-stu-id="1fb42-140">-ProductId</span></span>
<span data-ttu-id="1fb42-141">Var olan bir ürünün tanımlayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1fb42-141">Specifies the identifier of an existing product.</span></span>
<span data-ttu-id="1fb42-142">Bu parametreyi belirtirseniz cmdlet, ürün kapsam ilkesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="1fb42-142">If you specify this parameter the cmdlet returns the product-scope policy.</span></span>

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

### <span data-ttu-id="1fb42-143">-SaveAs</span><span class="sxs-lookup"><span data-stu-id="1fb42-143">-SaveAs</span></span>
<span data-ttu-id="1fb42-144">Sonucun kaydedileceği dosya yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="1fb42-144">Specifies the file path to save the result to.</span></span>
<span data-ttu-id="1fb42-145">Bu parametreyi belirtmezseniz, sonuç olarak ardışık düzen gönderilir.</span><span class="sxs-lookup"><span data-stu-id="1fb42-145">If you do not specify this parameter the result is pipelined as a sting.</span></span>

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

### <span data-ttu-id="1fb42-146">-Onay</span><span class="sxs-lookup"><span data-stu-id="1fb42-146">-Confirm</span></span>
<span data-ttu-id="1fb42-147">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="1fb42-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1fb42-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1fb42-148">-WhatIf</span></span>
<span data-ttu-id="1fb42-149">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="1fb42-149">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1fb42-150">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="1fb42-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1fb42-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1fb42-151">CommonParameters</span></span>
<span data-ttu-id="1fb42-152">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1fb42-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1fb42-153">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1fb42-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1fb42-154">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1fb42-154">INPUTS</span></span>

### <span data-ttu-id="1fb42-155">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="1fb42-155">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="1fb42-156">System. String</span><span class="sxs-lookup"><span data-stu-id="1fb42-156">System.String</span></span>

### <span data-ttu-id="1fb42-157">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="1fb42-157">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="1fb42-158">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1fb42-158">OUTPUTS</span></span>

### <span data-ttu-id="1fb42-159">System. String</span><span class="sxs-lookup"><span data-stu-id="1fb42-159">System.String</span></span>

## <span data-ttu-id="1fb42-160">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1fb42-160">NOTES</span></span>

## <span data-ttu-id="1fb42-161">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1fb42-161">RELATED LINKS</span></span>

[<span data-ttu-id="1fb42-162">Remove-Azapsananagementpolicy</span><span class="sxs-lookup"><span data-stu-id="1fb42-162">Remove-AzApiManagementPolicy</span></span>](./Remove-AzApiManagementPolicy.md)

[<span data-ttu-id="1fb42-163">Set-Azapsananagementpolicy</span><span class="sxs-lookup"><span data-stu-id="1fb42-163">Set-AzApiManagementPolicy</span></span>](./Set-AzApiManagementPolicy.md)


