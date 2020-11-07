---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 6CD1C2B8-0416-4FF3-81B0-0C9E59AE6CF9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementPolicy.md
ms.openlocfilehash: 0f9ee1c2190dbc3d657ecc52cd85b6af8b0cac4b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762660"
---
# <span data-ttu-id="737bc-101">Set-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="737bc-101">Set-AzureRmApiManagementPolicy</span></span>

## <span data-ttu-id="737bc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="737bc-102">SYNOPSIS</span></span>
<span data-ttu-id="737bc-103">API yönetimi için belirtilen kapsam ilkesini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="737bc-103">Sets the specified scope policy for API Management.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="737bc-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="737bc-104">SYNTAX</span></span>

### <span data-ttu-id="737bc-105">SetTenantLevel (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="737bc-105">SetTenantLevel (Default)</span></span>
```
Set-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-Policy <String>]
 [-PolicyFilePath <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="737bc-106">SetProductLevel</span><span class="sxs-lookup"><span data-stu-id="737bc-106">SetProductLevel</span></span>
```
Set-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] -ProductId <String>
 [-Policy <String>] [-PolicyFilePath <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="737bc-107">Setapi</span><span class="sxs-lookup"><span data-stu-id="737bc-107">SetApiLevel</span></span>
```
Set-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] -ApiId <String>
 [-Policy <String>] [-PolicyFilePath <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="737bc-108">SetOperationLevel</span><span class="sxs-lookup"><span data-stu-id="737bc-108">SetOperationLevel</span></span>
```
Set-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] -ApiId <String>
 -OperationId <String> [-Policy <String>] [-PolicyFilePath <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="737bc-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="737bc-109">DESCRIPTION</span></span>
<span data-ttu-id="737bc-110">**Set-Azurermapsananagementpolicy** cmdlet 'ı, API yönetimi için belirtilen kapsam ilkesini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="737bc-110">The **Set-AzureRmApiManagementPolicy** cmdlet sets the specified scope policy for API Management.</span></span>

## <span data-ttu-id="737bc-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="737bc-111">EXAMPLES</span></span>

### <span data-ttu-id="737bc-112">Örnek 1: kiracı düzeyi ilkesini ayarlama</span><span class="sxs-lookup"><span data-stu-id="737bc-112">Example 1: Set the tenant level policy</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementPolicy -Context $apimContext -PolicyFilePath "C:\contoso\policies\tenantpolicy.xml"
```

<span data-ttu-id="737bc-113">Bu komut tenantpolicy.xml adlı dosyadan kiracı düzeyi ilkesini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="737bc-113">This command sets the tenant level policy from a file named tenantpolicy.xml.</span></span>

### <span data-ttu-id="737bc-114">Örnek 2: ürün kapsamı ilkesi ayarlama</span><span class="sxs-lookup"><span data-stu-id="737bc-114">Example 2: Set a product-scope policy</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementPolicy -Context $apimContext -ProductId "0123456789" -Policy $PolicyString
```

<span data-ttu-id="737bc-115">Bu komut API yönetimi için ürün kapsamı ilkesini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="737bc-115">This command sets the product-scope policy for API Management.</span></span>

### <span data-ttu-id="737bc-116">Örnek 3: API kapsam ilkesini ayarlama</span><span class="sxs-lookup"><span data-stu-id="737bc-116">Example 3: Set API-scope policy</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementPolicy -Context $apimContext -ApiId "9876543210" -Policy $PolicyString
```

<span data-ttu-id="737bc-117">Bu komut API yönetimi için API kapsam ilkesini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="737bc-117">This command sets API-scope policy for API Management.</span></span>

### <span data-ttu-id="737bc-118">Örnek 4: set Operation-kapsam ilkesi</span><span class="sxs-lookup"><span data-stu-id="737bc-118">Example 4: Set operation-scope policy</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementPolicy -Context $apimContext -ApiId "9876543210" -OperationId "777" -Policy $PolicyString
```

<span data-ttu-id="737bc-119">Bu komut API yönetimi için işlem kapsam ilkesini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="737bc-119">This command sets operation-scope policy for API Management.</span></span>

## <span data-ttu-id="737bc-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="737bc-120">PARAMETERS</span></span>

### <span data-ttu-id="737bc-121">-Apııd</span><span class="sxs-lookup"><span data-stu-id="737bc-121">-ApiId</span></span>
<span data-ttu-id="737bc-122">Var olan API 'nin tanımlayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="737bc-122">Specifies the identifier of the existing API.</span></span>
<span data-ttu-id="737bc-123">Bu parametreyi belirtirseniz cmdlet API kapsam ilkesini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="737bc-123">If you specify this parameter, the cmdlet sets the API-scope policy.</span></span>

```yaml
Type: String
Parameter Sets: SetApiLevel, SetOperationLevel
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="737bc-124">-Context</span><span class="sxs-lookup"><span data-stu-id="737bc-124">-Context</span></span>
<span data-ttu-id="737bc-125">**Psapsananagementcontext** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="737bc-125">Specifies the instance of **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="737bc-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="737bc-126">-DefaultProfile</span></span>
<span data-ttu-id="737bc-127">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="737bc-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="737bc-128">Biçimli</span><span class="sxs-lookup"><span data-stu-id="737bc-128">-Format</span></span>
<span data-ttu-id="737bc-129">İlkenin biçimini belirtir.</span><span class="sxs-lookup"><span data-stu-id="737bc-129">Specifies the format of the policy.</span></span>
<span data-ttu-id="737bc-130">Varsayılan değer "application/vnd. MS-Azure-apim. Policy + xml" değeridir.</span><span class="sxs-lookup"><span data-stu-id="737bc-130">The default value is "application/vnd.ms-azure-apim.policy+xml".</span></span>

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

### <span data-ttu-id="737bc-131">-OperationId</span><span class="sxs-lookup"><span data-stu-id="737bc-131">-OperationId</span></span>
<span data-ttu-id="737bc-132">Var olan işlemin tanımlayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="737bc-132">Specifies the identifier of the existing operation.</span></span>
<span data-ttu-id="737bc-133">Apııd ile belirtilirse, işlem kapsam ilkesini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="737bc-133">If specified with ApiId will set operation-scope policy.</span></span>
<span data-ttu-id="737bc-134">Bu parametreler gereklidir.</span><span class="sxs-lookup"><span data-stu-id="737bc-134">This parameters is required.</span></span>

```yaml
Type: String
Parameter Sets: SetOperationLevel
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="737bc-135">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="737bc-135">-PassThru</span></span>
<span data-ttu-id="737bc-136">geçiş</span><span class="sxs-lookup"><span data-stu-id="737bc-136">passthru</span></span>

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

### <span data-ttu-id="737bc-137">-İlke</span><span class="sxs-lookup"><span data-stu-id="737bc-137">-Policy</span></span>
<span data-ttu-id="737bc-138">İlke belgesini dize olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="737bc-138">Specifies the policy document as a string.</span></span>
<span data-ttu-id="737bc-139">- *PolicyFilePath* belirtilmemişse bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="737bc-139">This parameter is required if the - *PolicyFilePath* is not specified.</span></span>

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

### <span data-ttu-id="737bc-140">-PolicyFilePath</span><span class="sxs-lookup"><span data-stu-id="737bc-140">-PolicyFilePath</span></span>
<span data-ttu-id="737bc-141">İlke belge dosyası yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="737bc-141">Specifies the policy document file path.</span></span>
<span data-ttu-id="737bc-142">Bu parametre, *ilke* parametresi belirtilmemişse gereklidir.</span><span class="sxs-lookup"><span data-stu-id="737bc-142">This parameter is required if the *Policy* parameter is not specified.</span></span>

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

### <span data-ttu-id="737bc-143">-ÜrünKimliği</span><span class="sxs-lookup"><span data-stu-id="737bc-143">-ProductId</span></span>
<span data-ttu-id="737bc-144">Var olan ürünün tanımlayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="737bc-144">Specifies the identifier of the existing product.</span></span>
<span data-ttu-id="737bc-145">Bu parametre belirtilirse cmdlet, ürün kapsam ilkesini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="737bc-145">If this parameter is specified, the cmdlet sets the product-scope policy.</span></span>

```yaml
Type: String
Parameter Sets: SetProductLevel
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="737bc-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="737bc-146">CommonParameters</span></span>
<span data-ttu-id="737bc-147">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="737bc-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="737bc-148">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="737bc-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="737bc-149">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="737bc-149">INPUTS</span></span>

### <span data-ttu-id="737bc-150">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="737bc-150">None</span></span>
<span data-ttu-id="737bc-151">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="737bc-151">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="737bc-152">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="737bc-152">OUTPUTS</span></span>

### <span data-ttu-id="737bc-153">bool</span><span class="sxs-lookup"><span data-stu-id="737bc-153">bool</span></span>

## <span data-ttu-id="737bc-154">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="737bc-154">NOTES</span></span>

## <span data-ttu-id="737bc-155">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="737bc-155">RELATED LINKS</span></span>

[<span data-ttu-id="737bc-156">Get-Azurermapımanagementpolicy</span><span class="sxs-lookup"><span data-stu-id="737bc-156">Get-AzureRmApiManagementPolicy</span></span>](./Get-AzureRmApiManagementPolicy.md)

[<span data-ttu-id="737bc-157">Remove-Azurermapımanagementpolicy</span><span class="sxs-lookup"><span data-stu-id="737bc-157">Remove-AzureRmApiManagementPolicy</span></span>](./Remove-AzureRmApiManagementPolicy.md)


