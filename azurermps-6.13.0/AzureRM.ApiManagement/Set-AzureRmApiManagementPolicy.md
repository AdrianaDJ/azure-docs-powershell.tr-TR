---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 6CD1C2B8-0416-4FF3-81B0-0C9E59AE6CF9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementPolicy.md
ms.openlocfilehash: 75bb963195244a5a1a27ca004eb2795b6b5bb556
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587336"
---
# <span data-ttu-id="c130f-101">Set-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="c130f-101">Set-AzureRmApiManagementPolicy</span></span>

## <span data-ttu-id="c130f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c130f-102">SYNOPSIS</span></span>
<span data-ttu-id="c130f-103">API yönetimi için belirtilen kapsam ilkesini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="c130f-103">Sets the specified scope policy for API Management.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c130f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c130f-104">SYNTAX</span></span>

### <span data-ttu-id="c130f-105">SetTenantLevel (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="c130f-105">SetTenantLevel (Default)</span></span>
```
Set-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-Policy <String>]
 [-PolicyFilePath <String>] [-PolicyUrl <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c130f-106">SetProductLevel</span><span class="sxs-lookup"><span data-stu-id="c130f-106">SetProductLevel</span></span>
```
Set-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] -ProductId <String>
 [-Policy <String>] [-PolicyFilePath <String>] [-PolicyUrl <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c130f-107">Setapi</span><span class="sxs-lookup"><span data-stu-id="c130f-107">SetApiLevel</span></span>
```
Set-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] -ApiId <String>
 [-ApiRevision <String>] [-Policy <String>] [-PolicyFilePath <String>] [-PolicyUrl <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c130f-108">SetOperationLevel</span><span class="sxs-lookup"><span data-stu-id="c130f-108">SetOperationLevel</span></span>
```
Set-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] -ApiId <String>
 [-ApiRevision <String>] -OperationId <String> [-Policy <String>] [-PolicyFilePath <String>]
 [-PolicyUrl <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c130f-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="c130f-109">DESCRIPTION</span></span>
<span data-ttu-id="c130f-110">**Set-Azurermapsananagementpolicy** cmdlet 'ı, API yönetimi için belirtilen kapsam ilkesini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="c130f-110">The **Set-AzureRmApiManagementPolicy** cmdlet sets the specified scope policy for API Management.</span></span>

## <span data-ttu-id="c130f-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c130f-111">EXAMPLES</span></span>

### <span data-ttu-id="c130f-112">Örnek 1: kiracı düzeyi ilkesini ayarlama</span><span class="sxs-lookup"><span data-stu-id="c130f-112">Example 1: Set the tenant level policy</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementPolicy -Context $apimContext -PolicyFilePath "C:\contoso\policies\tenantpolicy.xml"
```

<span data-ttu-id="c130f-113">Bu komut tenantpolicy.xml adlı dosyadan kiracı düzeyi ilkesini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="c130f-113">This command sets the tenant level policy from a file named tenantpolicy.xml.</span></span>

### <span data-ttu-id="c130f-114">Örnek 2: ürün kapsamı ilkesi ayarlama</span><span class="sxs-lookup"><span data-stu-id="c130f-114">Example 2: Set a product-scope policy</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementPolicy -Context $apimContext -ProductId "0123456789" -Policy $PolicyString
```

<span data-ttu-id="c130f-115">Bu komut API yönetimi için ürün kapsamı ilkesini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="c130f-115">This command sets the product-scope policy for API Management.</span></span>

### <span data-ttu-id="c130f-116">Örnek 3: API kapsam ilkesini ayarlama</span><span class="sxs-lookup"><span data-stu-id="c130f-116">Example 3: Set API-scope policy</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementPolicy -Context $apimContext -ApiId "9876543210" -Policy $PolicyString
```

<span data-ttu-id="c130f-117">Bu komut API yönetimi için API kapsam ilkesini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="c130f-117">This command sets API-scope policy for API Management.</span></span>

### <span data-ttu-id="c130f-118">Örnek 4: set Operation-kapsam ilkesi</span><span class="sxs-lookup"><span data-stu-id="c130f-118">Example 4: Set operation-scope policy</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementPolicy -Context $apimContext -ApiId "9876543210" -OperationId "777" -Policy $PolicyString
```

<span data-ttu-id="c130f-119">Bu komut API yönetimi için işlem kapsam ilkesini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="c130f-119">This command sets operation-scope policy for API Management.</span></span>

## <span data-ttu-id="c130f-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c130f-120">PARAMETERS</span></span>

### <span data-ttu-id="c130f-121">-Apııd</span><span class="sxs-lookup"><span data-stu-id="c130f-121">-ApiId</span></span>
<span data-ttu-id="c130f-122">Var olan API 'nin tanımlayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c130f-122">Specifies the identifier of the existing API.</span></span>
<span data-ttu-id="c130f-123">Bu parametreyi belirtirseniz cmdlet API kapsam ilkesini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="c130f-123">If you specify this parameter, the cmdlet sets the API-scope policy.</span></span>

```yaml
Type: System.String
Parameter Sets: SetApiLevel, SetOperationLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c130f-124">-Apırevision</span><span class="sxs-lookup"><span data-stu-id="c130f-124">-ApiRevision</span></span>
<span data-ttu-id="c130f-125">API düzeltme tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="c130f-125">Identifier of API Revision.</span></span> <span data-ttu-id="c130f-126">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="c130f-126">This parameter is optional.</span></span> <span data-ttu-id="c130f-127">Belirtilmemişse, ilke etkin API düzeltmesinde güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="c130f-127">If not specified, the policy will be updated in the currently active api revision.</span></span>

```yaml
Type: System.String
Parameter Sets: SetApiLevel, SetOperationLevel
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c130f-128">-Context</span><span class="sxs-lookup"><span data-stu-id="c130f-128">-Context</span></span>
<span data-ttu-id="c130f-129">**Psapsananagementcontext** örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="c130f-129">Specifies the instance of **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="c130f-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c130f-130">-DefaultProfile</span></span>
<span data-ttu-id="c130f-131">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c130f-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c130f-132">Biçimli</span><span class="sxs-lookup"><span data-stu-id="c130f-132">-Format</span></span>
<span data-ttu-id="c130f-133">İlkenin biçimini belirtir.</span><span class="sxs-lookup"><span data-stu-id="c130f-133">Specifies the format of the policy.</span></span> <span data-ttu-id="c130f-134">Kullanıldığında `application/vnd.ms-azure-apim.policy+xml` , ilkenin içerdiği Ifadeler XML kaçışlı olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="c130f-134">When using `application/vnd.ms-azure-apim.policy+xml`, expressions contained within the policy must be XML-escaped.</span></span> <span data-ttu-id="c130f-135">Bunu kullanırken `application/vnd.ms-azure-apim.policy.raw+xml` , ILKENIN **not** XML kaçılması gerekmez.</span><span class="sxs-lookup"><span data-stu-id="c130f-135">When using `application/vnd.ms-azure-apim.policy.raw+xml` it is **not** necessary for the policy to be XML-escaped.</span></span>
<span data-ttu-id="c130f-136">Varsayılan değer `application/vnd.ms-azure-apim.policy+xml` .</span><span class="sxs-lookup"><span data-stu-id="c130f-136">The default value is `application/vnd.ms-azure-apim.policy+xml`.</span></span>
<span data-ttu-id="c130f-137">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="c130f-137">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: application/vnd.ms-azure-apim.policy.raw+xml, application/vnd.ms-azure-apim.policy+xml

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c130f-138">-OperationId</span><span class="sxs-lookup"><span data-stu-id="c130f-138">-OperationId</span></span>
<span data-ttu-id="c130f-139">Var olan işlemin tanımlayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c130f-139">Specifies the identifier of the existing operation.</span></span>
<span data-ttu-id="c130f-140">Apııd ile belirtilirse, işlem kapsam ilkesini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="c130f-140">If specified with ApiId will set operation-scope policy.</span></span>
<span data-ttu-id="c130f-141">Bu parametreler gereklidir.</span><span class="sxs-lookup"><span data-stu-id="c130f-141">This parameters is required.</span></span>

```yaml
Type: System.String
Parameter Sets: SetOperationLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c130f-142">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="c130f-142">-PassThru</span></span>
<span data-ttu-id="c130f-143">geçiş</span><span class="sxs-lookup"><span data-stu-id="c130f-143">passthru</span></span>

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

### <span data-ttu-id="c130f-144">-İlke</span><span class="sxs-lookup"><span data-stu-id="c130f-144">-Policy</span></span>
<span data-ttu-id="c130f-145">İlke belgesini dize olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="c130f-145">Specifies the policy document as a string.</span></span>
<span data-ttu-id="c130f-146">- *PolicyFilePath* belirtilmemişse bu parametre gereklidir.</span><span class="sxs-lookup"><span data-stu-id="c130f-146">This parameter is required if the - *PolicyFilePath* is not specified.</span></span>

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

### <span data-ttu-id="c130f-147">-PolicyFilePath</span><span class="sxs-lookup"><span data-stu-id="c130f-147">-PolicyFilePath</span></span>
<span data-ttu-id="c130f-148">İlke belge dosyası yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="c130f-148">Specifies the policy document file path.</span></span>
<span data-ttu-id="c130f-149">Bu parametre, *ilke* parametresi belirtilmemişse gereklidir.</span><span class="sxs-lookup"><span data-stu-id="c130f-149">This parameter is required if the *Policy* parameter is not specified.</span></span>

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

### <span data-ttu-id="c130f-150">-PolicyUrl</span><span class="sxs-lookup"><span data-stu-id="c130f-150">-PolicyUrl</span></span>
<span data-ttu-id="c130f-151">Ilke belgesinin barındırıldığı URL.</span><span class="sxs-lookup"><span data-stu-id="c130f-151">The Url where the Policy document is hosted.</span></span> <span data-ttu-id="c130f-152">Bu parametre,-Policy veya-PolicyFilePath belirtilmezse gereklidir.</span><span class="sxs-lookup"><span data-stu-id="c130f-152">This parameter is required if -Policy or -PolicyFilePath is not specified.</span></span>

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

### <span data-ttu-id="c130f-153">-ÜrünKimliği</span><span class="sxs-lookup"><span data-stu-id="c130f-153">-ProductId</span></span>
<span data-ttu-id="c130f-154">Var olan ürünün tanımlayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c130f-154">Specifies the identifier of the existing product.</span></span>
<span data-ttu-id="c130f-155">Bu parametre belirtilirse cmdlet, ürün kapsam ilkesini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="c130f-155">If this parameter is specified, the cmdlet sets the product-scope policy.</span></span>

```yaml
Type: System.String
Parameter Sets: SetProductLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c130f-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c130f-156">CommonParameters</span></span>
<span data-ttu-id="c130f-157">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c130f-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c130f-158">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c130f-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c130f-159">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c130f-159">INPUTS</span></span>

### <span data-ttu-id="c130f-160">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="c130f-160">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="c130f-161">System. String</span><span class="sxs-lookup"><span data-stu-id="c130f-161">System.String</span></span>

### <span data-ttu-id="c130f-162">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="c130f-162">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="c130f-163">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c130f-163">OUTPUTS</span></span>

### <span data-ttu-id="c130f-164">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c130f-164">System.Boolean</span></span>

## <span data-ttu-id="c130f-165">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c130f-165">NOTES</span></span>

## <span data-ttu-id="c130f-166">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c130f-166">RELATED LINKS</span></span>

[<span data-ttu-id="c130f-167">Get-Azurermapımanagementpolicy</span><span class="sxs-lookup"><span data-stu-id="c130f-167">Get-AzureRmApiManagementPolicy</span></span>](./Get-AzureRmApiManagementPolicy.md)

[<span data-ttu-id="c130f-168">Remove-Azurermapımanagementpolicy</span><span class="sxs-lookup"><span data-stu-id="c130f-168">Remove-AzureRmApiManagementPolicy</span></span>](./Remove-AzureRmApiManagementPolicy.md)


