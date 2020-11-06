---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 466AFB8C-C272-4A4F-8E13-A4DBD6EE3A85
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementPolicy.md
ms.openlocfilehash: 67cff03f8531ff71170fe565d5da411ca5b4f127
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586843"
---
# <span data-ttu-id="67e15-101">Remove-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="67e15-101">Remove-AzureRmApiManagementPolicy</span></span>

## <span data-ttu-id="67e15-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="67e15-102">SYNOPSIS</span></span>
<span data-ttu-id="67e15-103">Belirtilen kapsamdan API yönetim ilkesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="67e15-103">Removes the API Management policy from a specified scope.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="67e15-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="67e15-104">SYNTAX</span></span>

### <span data-ttu-id="67e15-105">RemoveTenantLevel (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="67e15-105">RemoveTenantLevel (Default)</span></span>
```
Remove-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="67e15-106">RemoveProductLevel</span><span class="sxs-lookup"><span data-stu-id="67e15-106">RemoveProductLevel</span></span>
```
Remove-AzureRmApiManagementPolicy -Context <PsApiManagementContext> -ProductId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="67e15-107">Removeapilelevel</span><span class="sxs-lookup"><span data-stu-id="67e15-107">RemoveApiLevel</span></span>
```
Remove-AzureRmApiManagementPolicy -Context <PsApiManagementContext> -ApiId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="67e15-108">RemoveOperationLevel</span><span class="sxs-lookup"><span data-stu-id="67e15-108">RemoveOperationLevel</span></span>
```
Remove-AzureRmApiManagementPolicy -Context <PsApiManagementContext> -ApiId <String> -OperationId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="67e15-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="67e15-109">DESCRIPTION</span></span>
<span data-ttu-id="67e15-110">**Remove-Azurermapsananagementpolicy** cmdlet 'i, BELIRTILEN kapsamdan API yönetim ilkesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="67e15-110">The **Remove-AzureRmApiManagementPolicy** cmdlet removes the API Management policy from specified scope.</span></span>

## <span data-ttu-id="67e15-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="67e15-111">EXAMPLES</span></span>

### <span data-ttu-id="67e15-112">Örnek 1: kiracı düzeyi ilkesini kaldırma</span><span class="sxs-lookup"><span data-stu-id="67e15-112">Example 1: Remove the tenant level policy</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementPolicy -Context $apimContext
```

<span data-ttu-id="67e15-113">Bu komut, kiracı düzeyi ilkesini API yönetiminden kaldırır.</span><span class="sxs-lookup"><span data-stu-id="67e15-113">This command removes tenant level policy from API Management.</span></span>

### <span data-ttu-id="67e15-114">Örnek 2: ürün kapsamı ilkesini kaldırma</span><span class="sxs-lookup"><span data-stu-id="67e15-114">Example 2: Remove the product-scope policy</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementPolicy -Context $apimContext -ProductId "0123456789"
```

<span data-ttu-id="67e15-115">Bu komut, API yönetiminden ürün kapsam ilkesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="67e15-115">This command removes product-scope policy from API Management.</span></span>

### <span data-ttu-id="67e15-116">Örnek 3: API kapsam ilkesini kaldırma</span><span class="sxs-lookup"><span data-stu-id="67e15-116">Example 3: Remove the API-scope policy</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementPolicy -Context $apimContext -ApiId "9876543210"
```

<span data-ttu-id="67e15-117">Bu komut API Yönetimi 'nden API kapsam ilkesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="67e15-117">This command removes API-scope policy from API Management.</span></span>

### <span data-ttu-id="67e15-118">Örnek 4: işlem kapsamı ilkesini kaldırma</span><span class="sxs-lookup"><span data-stu-id="67e15-118">Example 4: Remove the operation-scope policy</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementPolicy -Context $apimContext -ApiId "9876543210" -OperationId "777"
```

<span data-ttu-id="67e15-119">Bu komut, işlem kapsam ilkesini API yönetiminden kaldırır.</span><span class="sxs-lookup"><span data-stu-id="67e15-119">This command removes operation-scope policy from API Management.</span></span>

## <span data-ttu-id="67e15-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="67e15-120">PARAMETERS</span></span>

### <span data-ttu-id="67e15-121">-Apııd</span><span class="sxs-lookup"><span data-stu-id="67e15-121">-ApiId</span></span>
<span data-ttu-id="67e15-122">Var olan bir API 'ın tanımlayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="67e15-122">Specifies the identifier of an existing API.</span></span>
<span data-ttu-id="67e15-123">Bu parametreyi belirtirseniz cmdlet API kapsam ilkesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="67e15-123">If you specify this parameter, the cmdlet removes the API-scope policy.</span></span>

```yaml
Type: String
Parameter Sets: RemoveApiLevel, RemoveOperationLevel
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67e15-124">-Context</span><span class="sxs-lookup"><span data-stu-id="67e15-124">-Context</span></span>
<span data-ttu-id="67e15-125">**Psapimanagementcontext** nesnesinin örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="67e15-125">Specifies the instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="67e15-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67e15-126">-DefaultProfile</span></span>
<span data-ttu-id="67e15-127">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="67e15-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="67e15-128">-OperationId</span><span class="sxs-lookup"><span data-stu-id="67e15-128">-OperationId</span></span>
<span data-ttu-id="67e15-129">Var olan bir işlemin tanımlayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="67e15-129">Specifies the identifier of an existing operation.</span></span>
<span data-ttu-id="67e15-130">Bu parametreyi *Apııd* parametresiyle belirtirseniz, bu cmdlet işlem kapsamı ilkesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="67e15-130">If you specify this parameter with the *ApiId* parameter, this cmdlet removes the operation-scope policy.</span></span>

```yaml
Type: String
Parameter Sets: RemoveOperationLevel
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67e15-131">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="67e15-131">-PassThru</span></span>
<span data-ttu-id="67e15-132">Bu cmdlet 'in bir $True değerini (başarılı olursa), aksi takdirde $False değerini döndürmediğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="67e15-132">Indicates that this cmdlet returns a value of $True, if it succeeds, or a value of $False, otherwise.</span></span>

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

### <span data-ttu-id="67e15-133">-ÜrünKimliği</span><span class="sxs-lookup"><span data-stu-id="67e15-133">-ProductId</span></span>
<span data-ttu-id="67e15-134">Var olan ürünün tanımlayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="67e15-134">Specifies the identifier of the existing product.</span></span>
<span data-ttu-id="67e15-135">Bu parametreyi belirtirseniz, cmdlet ürün kapsam ilkesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="67e15-135">If you specify this parameter, the cmdlet removes the product-scope policy.</span></span>

```yaml
Type: String
Parameter Sets: RemoveProductLevel
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67e15-136">-Onay</span><span class="sxs-lookup"><span data-stu-id="67e15-136">-Confirm</span></span>
<span data-ttu-id="67e15-137">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="67e15-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="67e15-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="67e15-138">-WhatIf</span></span>
<span data-ttu-id="67e15-139">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="67e15-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="67e15-140">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="67e15-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="67e15-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67e15-141">CommonParameters</span></span>
<span data-ttu-id="67e15-142">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="67e15-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67e15-143">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67e15-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67e15-144">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="67e15-144">INPUTS</span></span>

### <span data-ttu-id="67e15-145">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="67e15-145">None</span></span>
<span data-ttu-id="67e15-146">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="67e15-146">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="67e15-147">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="67e15-147">OUTPUTS</span></span>

### <span data-ttu-id="67e15-148">Boole</span><span class="sxs-lookup"><span data-stu-id="67e15-148">Boolean</span></span>

## <span data-ttu-id="67e15-149">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="67e15-149">NOTES</span></span>

## <span data-ttu-id="67e15-150">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="67e15-150">RELATED LINKS</span></span>

[<span data-ttu-id="67e15-151">Get-Azurermapımanagementpolicy</span><span class="sxs-lookup"><span data-stu-id="67e15-151">Get-AzureRmApiManagementPolicy</span></span>](./Get-AzureRmApiManagementPolicy.md)

[<span data-ttu-id="67e15-152">Set-Azurermapımanagementpolicy</span><span class="sxs-lookup"><span data-stu-id="67e15-152">Set-AzureRmApiManagementPolicy</span></span>](./Set-AzureRmApiManagementPolicy.md)


