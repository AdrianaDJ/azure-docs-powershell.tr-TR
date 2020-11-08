---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 7BCEB0EF-1A09-4CED-9F34-CE3AB03181A7
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementPolicy.md
ms.openlocfilehash: dc0d985203d51c705c40b423d0b6c9f381fa87e4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94097403"
---
# <span data-ttu-id="ec459-101">Get-AzApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="ec459-101">Get-AzApiManagementPolicy</span></span>

## <span data-ttu-id="ec459-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ec459-102">SYNOPSIS</span></span>
<span data-ttu-id="ec459-103">Belirtilen kapsam ilkesini alır.</span><span class="sxs-lookup"><span data-stu-id="ec459-103">Gets the specified scope policy.</span></span>

## <span data-ttu-id="ec459-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ec459-104">SYNTAX</span></span>

### <span data-ttu-id="ec459-105">GetTenantLevel (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="ec459-105">GetTenantLevel (Default)</span></span>
```
Get-AzApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ec459-106">GetProductLevel</span><span class="sxs-lookup"><span data-stu-id="ec459-106">GetProductLevel</span></span>
```
Get-AzApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>]
 -ProductId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ec459-107">Getapi</span><span class="sxs-lookup"><span data-stu-id="ec459-107">GetApiLevel</span></span>
```
Get-AzApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>]
 -ApiId <String> [-ApiRevision <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ec459-108">Getoperationdüzeyi</span><span class="sxs-lookup"><span data-stu-id="ec459-108">GetOperationLevel</span></span>
```
Get-AzApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>]
 -ApiId <String> [-ApiRevision <String>] -OperationId <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ec459-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="ec459-109">DESCRIPTION</span></span>
<span data-ttu-id="ec459-110">**Get-Azapsananagementpolicy** cmdlet 'i, belirtilen kapsam ilkesini alır.</span><span class="sxs-lookup"><span data-stu-id="ec459-110">The **Get-AzApiManagementPolicy** cmdlet gets the specified scope policy.</span></span>

## <span data-ttu-id="ec459-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ec459-111">EXAMPLES</span></span>

### <span data-ttu-id="ec459-112">Örnek 1: kiracı düzeyi ilkesini alma</span><span class="sxs-lookup"><span data-stu-id="ec459-112">Example 1: Get the tenant level policy</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementPolicy -Context $apimContext -SaveAs "C:\contoso\policies\tenantpolicy.xml"
```

<span data-ttu-id="ec459-113">Bu komut, kiracı düzeyi ilkesini alır ve tenantpolicy.xml adlı bir dosyaya kaydeder.</span><span class="sxs-lookup"><span data-stu-id="ec459-113">This command gets tenant level policy and saves it to a file named tenantpolicy.xml.</span></span>

### <span data-ttu-id="ec459-114">Örnek 2: ürün kapsamı ilkesini edinme</span><span class="sxs-lookup"><span data-stu-id="ec459-114">Example 2: Get the product-scope policy</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementPolicy -Context $apimContext -ProductId "0123456789"
```

<span data-ttu-id="ec459-115">Bu komut, ürün kapsam ilkesini alır</span><span class="sxs-lookup"><span data-stu-id="ec459-115">This command gets product-scope policy</span></span>

### <span data-ttu-id="ec459-116">Örnek 3: API kapsam ilkesini edinme</span><span class="sxs-lookup"><span data-stu-id="ec459-116">Example 3: Get the API-scope policy</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementPolicy -Context $apimContext -ApiId "9876543210"
```

<span data-ttu-id="ec459-117">Bu komut API kapsam ilkesini alır.</span><span class="sxs-lookup"><span data-stu-id="ec459-117">This command gets API-scope policy.</span></span>

### <span data-ttu-id="ec459-118">Örnek 4: işlem kapsamı ilkesini edinme</span><span class="sxs-lookup"><span data-stu-id="ec459-118">Example 4: Get the operation-scope policy</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementPolicy -Context $apimContext -ApiId "9876543210" -OperationId "777"
```

<span data-ttu-id="ec459-119">Bu komut, işlem kapsamı ilkesini alır.</span><span class="sxs-lookup"><span data-stu-id="ec459-119">This command gets the operation-scope policy.</span></span>

### <span data-ttu-id="ec459-120">Örnek 5: RawXml biçiminde kiracı kapsam ilkesini edinme</span><span class="sxs-lookup"><span data-stu-id="ec459-120">Example 5: Get the Tenant scope policy in RawXml format</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS c:\> Get-AzApiManagementPolicy -Context $context -Format rawxml

<policies>
        <inbound>
                <set-header name="correlationid" exists-action="skip">
                        <value>@{
                var guidBinary = new byte[16];
                Array.Copy(Guid.NewGuid().ToByteArray(), 0, guidBinary, 0, 10);
                long time = DateTime.Now.Ticks;
                byte[] bytes = new byte[6];
                unchecked
                {
                       bytes[5] = (byte)(time >> 40);
                       bytes[4] = (byte)(time >> 32);
                       bytes[3] = (byte)(time >> 24);
                       bytes[2] = (byte)(time >> 16);
                       bytes[1] = (byte)(time >> 8);
                       bytes[0] = (byte)(time);
                }
                Array.Copy(bytes, 0, guidBinary, 10, 6);
                return new Guid(guidBinary).ToString();
            }
            </value>
                </set-header>
        </inbound>
        <backend>
                <forward-request />
        </backend>
        <outbound />
        <on-error />
</policies>
```

<span data-ttu-id="ec459-121">Bu komut, kiracı kapsam ilkesini XML dışında kaçan biçimde alır.</span><span class="sxs-lookup"><span data-stu-id="ec459-121">This command gets the tenant-scope policy in Non-Xml escaped format.</span></span>

## <span data-ttu-id="ec459-122">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ec459-122">PARAMETERS</span></span>

### <span data-ttu-id="ec459-123">-Apııd</span><span class="sxs-lookup"><span data-stu-id="ec459-123">-ApiId</span></span>
<span data-ttu-id="ec459-124">Var olan API 'nin tanımlayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ec459-124">Specifies the identifier of the existing API.</span></span>
<span data-ttu-id="ec459-125">Bu parametreyi belirtirseniz cmdlet API kapsam ilkesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="ec459-125">If you specify this parameter the cmdlet returns the API-scope policy.</span></span>

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

### <span data-ttu-id="ec459-126">-Apırevision</span><span class="sxs-lookup"><span data-stu-id="ec459-126">-ApiRevision</span></span>
<span data-ttu-id="ec459-127">API düzeltme tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="ec459-127">Identifier of API Revision.</span></span> <span data-ttu-id="ec459-128">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="ec459-128">This parameter is optional.</span></span> <span data-ttu-id="ec459-129">Belirtilmemişse, ilke geçerli etkin API düzeltmesidir.</span><span class="sxs-lookup"><span data-stu-id="ec459-129">If not specified, the policy will be retrieved from the currently active api revision.</span></span>

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

### <span data-ttu-id="ec459-130">-Context</span><span class="sxs-lookup"><span data-stu-id="ec459-130">-Context</span></span>
<span data-ttu-id="ec459-131">**Psapsananagementcontext** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ec459-131">Specifies an instance of **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="ec459-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec459-132">-DefaultProfile</span></span>
<span data-ttu-id="ec459-133">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ec459-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ec459-134">-Force</span><span class="sxs-lookup"><span data-stu-id="ec459-134">-Force</span></span>
<span data-ttu-id="ec459-135">ps_force</span><span class="sxs-lookup"><span data-stu-id="ec459-135">ps_force</span></span>

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

### <span data-ttu-id="ec459-136">Biçimli</span><span class="sxs-lookup"><span data-stu-id="ec459-136">-Format</span></span>
<span data-ttu-id="ec459-137">API yönetim ilkesinin biçimini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ec459-137">Specifies the format of the API management policy.</span></span>
<span data-ttu-id="ec459-138">Bu parametre için varsayılan değer "xml" olur.</span><span class="sxs-lookup"><span data-stu-id="ec459-138">The default value for this parameter is "xml".</span></span>

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

### <span data-ttu-id="ec459-139">-OperationId</span><span class="sxs-lookup"><span data-stu-id="ec459-139">-OperationId</span></span>
<span data-ttu-id="ec459-140">Var olan API işleminin tanımlayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ec459-140">Specifies the identifier of the existing API operation.</span></span>
<span data-ttu-id="ec459-141">Bu parametreyi *Apııd* ile belirtirseniz cmdlet, operasyon kapsam ilkesi döndürüyor.</span><span class="sxs-lookup"><span data-stu-id="ec459-141">If you specify this parameter with *ApiId* the cmdlet returns operation-scope policy.</span></span>

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

### <span data-ttu-id="ec459-142">-ÜrünKimliği</span><span class="sxs-lookup"><span data-stu-id="ec459-142">-ProductId</span></span>
<span data-ttu-id="ec459-143">Var olan bir ürünün tanımlayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ec459-143">Specifies the identifier of an existing product.</span></span>
<span data-ttu-id="ec459-144">Bu parametreyi belirtirseniz cmdlet, ürün kapsam ilkesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="ec459-144">If you specify this parameter the cmdlet returns the product-scope policy.</span></span>

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

### <span data-ttu-id="ec459-145">-SaveAs</span><span class="sxs-lookup"><span data-stu-id="ec459-145">-SaveAs</span></span>
<span data-ttu-id="ec459-146">Sonucun kaydedileceği dosya yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="ec459-146">Specifies the file path to save the result to.</span></span>
<span data-ttu-id="ec459-147">Bu parametreyi belirtmezseniz, sonuç olarak ardışık düzen gönderilir.</span><span class="sxs-lookup"><span data-stu-id="ec459-147">If you do not specify this parameter the result is pipelined as a sting.</span></span>

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

### <span data-ttu-id="ec459-148">-Onay</span><span class="sxs-lookup"><span data-stu-id="ec459-148">-Confirm</span></span>
<span data-ttu-id="ec459-149">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ec459-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ec459-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ec459-150">-WhatIf</span></span>
<span data-ttu-id="ec459-151">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ec459-151">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ec459-152">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ec459-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ec459-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec459-153">CommonParameters</span></span>
<span data-ttu-id="ec459-154">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ec459-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec459-155">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="ec459-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec459-156">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ec459-156">INPUTS</span></span>

### <span data-ttu-id="ec459-157">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="ec459-157">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="ec459-158">System. String</span><span class="sxs-lookup"><span data-stu-id="ec459-158">System.String</span></span>

### <span data-ttu-id="ec459-159">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="ec459-159">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="ec459-160">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ec459-160">OUTPUTS</span></span>

### <span data-ttu-id="ec459-161">System. String</span><span class="sxs-lookup"><span data-stu-id="ec459-161">System.String</span></span>

## <span data-ttu-id="ec459-162">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ec459-162">NOTES</span></span>

## <span data-ttu-id="ec459-163">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ec459-163">RELATED LINKS</span></span>

[<span data-ttu-id="ec459-164">Remove-Azapsananagementpolicy</span><span class="sxs-lookup"><span data-stu-id="ec459-164">Remove-AzApiManagementPolicy</span></span>](./Remove-AzApiManagementPolicy.md)

[<span data-ttu-id="ec459-165">Set-Azapsananagementpolicy</span><span class="sxs-lookup"><span data-stu-id="ec459-165">Set-AzApiManagementPolicy</span></span>](./Set-AzApiManagementPolicy.md)


