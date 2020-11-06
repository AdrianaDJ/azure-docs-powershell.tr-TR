---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 6CD1C2B8-0416-4FF3-81B0-0C9E59AE6CF9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementPolicy.md
ms.openlocfilehash: 8073df3946f5bf42ee8b0e5f2c7ae7881e905eaa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591209"
---
# <span data-ttu-id="29deb-101">Set-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="29deb-101">Set-AzureRmApiManagementPolicy</span></span>

## <span data-ttu-id="29deb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="29deb-102">SYNOPSIS</span></span>
<span data-ttu-id="29deb-103">API yönetimi için belirtilen kapsam ilkesini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="29deb-103">Sets the specified scope policy for API Management.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="29deb-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="29deb-104">SYNTAX</span></span>

### <span data-ttu-id="29deb-105">Kiracı düzeyi (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="29deb-105">Tenant level (Default)</span></span>
```
Set-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-Policy <String>]
 [-PolicyFilePath <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="29deb-106">Ürün düzeyi</span><span class="sxs-lookup"><span data-stu-id="29deb-106">Product level</span></span>
```
Set-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] -ProductId <String>
 [-Policy <String>] [-PolicyFilePath <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="29deb-107">API düzeyi</span><span class="sxs-lookup"><span data-stu-id="29deb-107">API level</span></span>
```
Set-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] -ApiId <String>
 [-Policy <String>] [-PolicyFilePath <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="29deb-108">İşlem düzeyi</span><span class="sxs-lookup"><span data-stu-id="29deb-108">Operation level</span></span>
```
Set-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] -ApiId <String>
 -OperationId <String> [-Policy <String>] [-PolicyFilePath <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="29deb-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="29deb-109">DESCRIPTION</span></span>
<span data-ttu-id="29deb-110">**Set-Azurermapsananagementpolicy** cmdlet 'ı, API yönetimi için belirtilen kapsam ilkesini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="29deb-110">The **Set-AzureRmApiManagementPolicy** cmdlet sets the specified scope policy for API Management.</span></span>

## <span data-ttu-id="29deb-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="29deb-111">EXAMPLES</span></span>

### <span data-ttu-id="29deb-112">Örnek 1: kiracı düzeyi ilkesini ayarlama</span><span class="sxs-lookup"><span data-stu-id="29deb-112">Example 1: Set the tenant level policy</span></span>
```
PS C:\>Set-AzureRmApiManagementPolicy -Context $APImContext -PolicyFilePath "C:\contoso\policies\tenantpolicy.xml"
```

<span data-ttu-id="29deb-113">Bu komut tenantpolicy.xml adlı dosyadan kiracı düzeyi ilkesini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="29deb-113">This command sets the tenant level policy from a file named tenantpolicy.xml.</span></span>

### <span data-ttu-id="29deb-114">Örnek 2: ürün kapsamı ilkesi ayarlama</span><span class="sxs-lookup"><span data-stu-id="29deb-114">Example 2: Set a product-scope policy</span></span>
```
PS C:\>Set-AzureRmApiManagementPolicy -Context $APImContext -ProductId "0123456789" -Policy $PolicyString
```

<span data-ttu-id="29deb-115">Bu komut API yönetimi için ürün kapsamı ilkesini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="29deb-115">This command sets the product-scope policy for API Management.</span></span>

### <span data-ttu-id="29deb-116">Örnek 3: API kapsam ilkesini ayarlama</span><span class="sxs-lookup"><span data-stu-id="29deb-116">Example 3: Set API-scope policy</span></span>
```
PS C:\>Get-AzureRmApiManagementPolicy -Context $APImContext -ApiId "9876543210" -Policy $PolicyString
```

<span data-ttu-id="29deb-117">Bu komut API yönetimi için API kapsam ilkesini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="29deb-117">This command sets API-scope policy for API Management.</span></span>

### <span data-ttu-id="29deb-118">Örnek 4: set Operation-kapsam ilkesi</span><span class="sxs-lookup"><span data-stu-id="29deb-118">Example 4: Set operation-scope policy</span></span>
```
PS C:\>Set-AzureRmApiManagementPolicy -Context $APImContext -ApiId "9876543210" -OperationId "777" -Policy $PolicyString
```

<span data-ttu-id="29deb-119">Bu komut API yönetimi için işlem kapsam ilkesini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="29deb-119">This command sets operation-scope policy for API Management.</span></span>

## <span data-ttu-id="29deb-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="29deb-120">PARAMETERS</span></span>

### <span data-ttu-id="29deb-121">-Apııd</span><span class="sxs-lookup"><span data-stu-id="29deb-121">-ApiId</span></span>
<span data-ttu-id="29deb-122">Var olan API 'nin tanımlayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="29deb-122">Specifies the identifier of the existing API.</span></span>
<span data-ttu-id="29deb-123">Bu parametreyi belirtirseniz cmdlet API kapsam ilkesini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="29deb-123">If you specify this parameter, the cmdlet sets the API-scope policy.</span></span>

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

### <span data-ttu-id="29deb-124">-Context</span><span class="sxs-lookup"><span data-stu-id="29deb-124">-Context</span></span>
<span data-ttu-id="29deb-125">**Psapsananagementcontext** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="29deb-125">Specifies the instance of **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="29deb-126">Biçimli</span><span class="sxs-lookup"><span data-stu-id="29deb-126">-Format</span></span>
<span data-ttu-id="29deb-127">İlkenin biçimini belirtir.</span><span class="sxs-lookup"><span data-stu-id="29deb-127">Specifies the format of the policy.</span></span>
<span data-ttu-id="29deb-128">Varsayılan değer "application/vnd. MS-Azure-apim. Policy + xml" değeridir.</span><span class="sxs-lookup"><span data-stu-id="29deb-128">The default value is "application/vnd.ms-azure-apim.policy+xml".</span></span>

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

### <span data-ttu-id="29deb-129">-OperationId</span><span class="sxs-lookup"><span data-stu-id="29deb-129">-OperationId</span></span>
<span data-ttu-id="29deb-130">Var olan işlemin tanımlayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="29deb-130">Specifies the identifier of the existing operation.</span></span>
<span data-ttu-id="29deb-131">Apııd ile belirtilirse, işlem kapsam ilkesini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="29deb-131">If specified with ApiId will set operation-scope policy.</span></span>
<span data-ttu-id="29deb-132">Bu parametreler gereklidir.</span><span class="sxs-lookup"><span data-stu-id="29deb-132">This parameters is required.</span></span>

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

### <span data-ttu-id="29deb-133">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="29deb-133">-PassThru</span></span>
<span data-ttu-id="29deb-134">geçiş</span><span class="sxs-lookup"><span data-stu-id="29deb-134">passthru</span></span>

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

### <span data-ttu-id="29deb-135">-İlke</span><span class="sxs-lookup"><span data-stu-id="29deb-135">-Policy</span></span>
<span data-ttu-id="29deb-136">İlke belgesini dize olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="29deb-136">Specifies the policy document as a string.</span></span>
<span data-ttu-id="29deb-137">- *PolicyFilePath* belirtilmemişse bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="29deb-137">This parameter is required if the - *PolicyFilePath* is not specified.</span></span>

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

### <span data-ttu-id="29deb-138">-PolicyFilePath</span><span class="sxs-lookup"><span data-stu-id="29deb-138">-PolicyFilePath</span></span>
<span data-ttu-id="29deb-139">İlke belge dosyası yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="29deb-139">Specifies the policy document file path.</span></span>
<span data-ttu-id="29deb-140">Bu parametre, *ilke* parametresi belirtilmemişse gereklidir.</span><span class="sxs-lookup"><span data-stu-id="29deb-140">This parameter is required if the *Policy* parameter is not specified.</span></span>

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

### <span data-ttu-id="29deb-141">-ÜrünKimliği</span><span class="sxs-lookup"><span data-stu-id="29deb-141">-ProductId</span></span>
<span data-ttu-id="29deb-142">Var olan ürünün tanımlayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="29deb-142">Specifies the identifier of the existing product.</span></span>
<span data-ttu-id="29deb-143">Bu parametre belirtilirse cmdlet, ürün kapsam ilkesini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="29deb-143">If this parameter is specified, the cmdlet sets the product-scope policy.</span></span>

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

### <span data-ttu-id="29deb-144">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29deb-144">-DefaultProfile</span></span>
<span data-ttu-id="29deb-145">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="29deb-145">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="29deb-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29deb-146">CommonParameters</span></span>
<span data-ttu-id="29deb-147">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="29deb-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29deb-148">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="29deb-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29deb-149">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="29deb-149">INPUTS</span></span>

## <span data-ttu-id="29deb-150">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="29deb-150">OUTPUTS</span></span>

### <span data-ttu-id="29deb-151">bool</span><span class="sxs-lookup"><span data-stu-id="29deb-151">bool</span></span>

## <span data-ttu-id="29deb-152">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="29deb-152">NOTES</span></span>

## <span data-ttu-id="29deb-153">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="29deb-153">RELATED LINKS</span></span>

[<span data-ttu-id="29deb-154">Get-Azurermapımanagementpolicy</span><span class="sxs-lookup"><span data-stu-id="29deb-154">Get-AzureRmApiManagementPolicy</span></span>](./Get-AzureRmApiManagementPolicy.md)

[<span data-ttu-id="29deb-155">Remove-Azurermapımanagementpolicy</span><span class="sxs-lookup"><span data-stu-id="29deb-155">Remove-AzureRmApiManagementPolicy</span></span>](./Remove-AzureRmApiManagementPolicy.md)


