---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 466AFB8C-C272-4A4F-8E13-A4DBD6EE3A85
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementPolicy.md
ms.openlocfilehash: c4f2ce8db3a799ad3d49d1c967da93a8fea93a39
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753455"
---
# <span data-ttu-id="0855f-101">Remove-AzApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="0855f-101">Remove-AzApiManagementPolicy</span></span>

## <span data-ttu-id="0855f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0855f-102">SYNOPSIS</span></span>
<span data-ttu-id="0855f-103">Belirtilen kapsamdan API yönetim ilkesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="0855f-103">Removes the API Management policy from a specified scope.</span></span>

## <span data-ttu-id="0855f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0855f-104">SYNTAX</span></span>

### <span data-ttu-id="0855f-105">RemoveTenantLevel (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="0855f-105">RemoveTenantLevel (Default)</span></span>
```
Remove-AzApiManagementPolicy -Context <PsApiManagementContext> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0855f-106">RemoveProductLevel</span><span class="sxs-lookup"><span data-stu-id="0855f-106">RemoveProductLevel</span></span>
```
Remove-AzApiManagementPolicy -Context <PsApiManagementContext> -ProductId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0855f-107">Removeapilelevel</span><span class="sxs-lookup"><span data-stu-id="0855f-107">RemoveApiLevel</span></span>
```
Remove-AzApiManagementPolicy -Context <PsApiManagementContext> -ApiId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0855f-108">RemoveOperationLevel</span><span class="sxs-lookup"><span data-stu-id="0855f-108">RemoveOperationLevel</span></span>
```
Remove-AzApiManagementPolicy -Context <PsApiManagementContext> -ApiId <String> -OperationId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0855f-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="0855f-109">DESCRIPTION</span></span>
<span data-ttu-id="0855f-110">**Remove-Azapsananagementpolicy** cmdlet 'i, BELIRTILEN kapsamdan API yönetim ilkesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="0855f-110">The **Remove-AzApiManagementPolicy** cmdlet removes the API Management policy from specified scope.</span></span>

## <span data-ttu-id="0855f-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0855f-111">EXAMPLES</span></span>

### <span data-ttu-id="0855f-112">Örnek 1: kiracı düzeyi ilkesini kaldırma</span><span class="sxs-lookup"><span data-stu-id="0855f-112">Example 1: Remove the tenant level policy</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementPolicy -Context $apimContext
```

<span data-ttu-id="0855f-113">Bu komut, kiracı düzeyi ilkesini API yönetiminden kaldırır.</span><span class="sxs-lookup"><span data-stu-id="0855f-113">This command removes tenant level policy from API Management.</span></span>

### <span data-ttu-id="0855f-114">Örnek 2: ürün kapsamı ilkesini kaldırma</span><span class="sxs-lookup"><span data-stu-id="0855f-114">Example 2: Remove the product-scope policy</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementPolicy -Context $apimContext -ProductId "0123456789"
```

<span data-ttu-id="0855f-115">Bu komut, API yönetiminden ürün kapsam ilkesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="0855f-115">This command removes product-scope policy from API Management.</span></span>

### <span data-ttu-id="0855f-116">Örnek 3: API kapsam ilkesini kaldırma</span><span class="sxs-lookup"><span data-stu-id="0855f-116">Example 3: Remove the API-scope policy</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementPolicy -Context $apimContext -ApiId "9876543210"
```

<span data-ttu-id="0855f-117">Bu komut API Yönetimi 'nden API kapsam ilkesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="0855f-117">This command removes API-scope policy from API Management.</span></span>

### <span data-ttu-id="0855f-118">Örnek 4: işlem kapsamı ilkesini kaldırma</span><span class="sxs-lookup"><span data-stu-id="0855f-118">Example 4: Remove the operation-scope policy</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementPolicy -Context $apimContext -ApiId "9876543210" -OperationId "777"
```

<span data-ttu-id="0855f-119">Bu komut, işlem kapsam ilkesini API yönetiminden kaldırır.</span><span class="sxs-lookup"><span data-stu-id="0855f-119">This command removes operation-scope policy from API Management.</span></span>

## <span data-ttu-id="0855f-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0855f-120">PARAMETERS</span></span>

### <span data-ttu-id="0855f-121">-Apııd</span><span class="sxs-lookup"><span data-stu-id="0855f-121">-ApiId</span></span>
<span data-ttu-id="0855f-122">Var olan bir API 'ın tanımlayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0855f-122">Specifies the identifier of an existing API.</span></span>
<span data-ttu-id="0855f-123">Bu parametreyi belirtirseniz cmdlet API kapsam ilkesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="0855f-123">If you specify this parameter, the cmdlet removes the API-scope policy.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveApiLevel, RemoveOperationLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0855f-124">-Context</span><span class="sxs-lookup"><span data-stu-id="0855f-124">-Context</span></span>
<span data-ttu-id="0855f-125">**Psapimanagementcontext** nesnesinin örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="0855f-125">Specifies the instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="0855f-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0855f-126">-DefaultProfile</span></span>
<span data-ttu-id="0855f-127">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0855f-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0855f-128">-OperationId</span><span class="sxs-lookup"><span data-stu-id="0855f-128">-OperationId</span></span>
<span data-ttu-id="0855f-129">Var olan bir işlemin tanımlayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0855f-129">Specifies the identifier of an existing operation.</span></span>
<span data-ttu-id="0855f-130">Bu parametreyi *Apııd* parametresiyle belirtirseniz, bu cmdlet işlem kapsamı ilkesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="0855f-130">If you specify this parameter with the *ApiId* parameter, this cmdlet removes the operation-scope policy.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveOperationLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0855f-131">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="0855f-131">-PassThru</span></span>
<span data-ttu-id="0855f-132">Bu cmdlet 'in bir $True değerini (başarılı olursa), aksi takdirde $False değerini döndürmediğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="0855f-132">Indicates that this cmdlet returns a value of $True, if it succeeds, or a value of $False, otherwise.</span></span>

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

### <span data-ttu-id="0855f-133">-ÜrünKimliği</span><span class="sxs-lookup"><span data-stu-id="0855f-133">-ProductId</span></span>
<span data-ttu-id="0855f-134">Var olan ürünün tanımlayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0855f-134">Specifies the identifier of the existing product.</span></span>
<span data-ttu-id="0855f-135">Bu parametreyi belirtirseniz, cmdlet ürün kapsam ilkesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="0855f-135">If you specify this parameter, the cmdlet removes the product-scope policy.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveProductLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0855f-136">-Onay</span><span class="sxs-lookup"><span data-stu-id="0855f-136">-Confirm</span></span>
<span data-ttu-id="0855f-137">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="0855f-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0855f-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0855f-138">-WhatIf</span></span>
<span data-ttu-id="0855f-139">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="0855f-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0855f-140">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="0855f-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0855f-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0855f-141">CommonParameters</span></span>
<span data-ttu-id="0855f-142">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0855f-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0855f-143">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="0855f-143">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0855f-144">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0855f-144">INPUTS</span></span>

### <span data-ttu-id="0855f-145">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="0855f-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="0855f-146">System. String</span><span class="sxs-lookup"><span data-stu-id="0855f-146">System.String</span></span>

### <span data-ttu-id="0855f-147">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="0855f-147">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="0855f-148">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0855f-148">OUTPUTS</span></span>

### <span data-ttu-id="0855f-149">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0855f-149">System.Boolean</span></span>

## <span data-ttu-id="0855f-150">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0855f-150">NOTES</span></span>

## <span data-ttu-id="0855f-151">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0855f-151">RELATED LINKS</span></span>

[<span data-ttu-id="0855f-152">Get-Azapsananagementpolicy</span><span class="sxs-lookup"><span data-stu-id="0855f-152">Get-AzApiManagementPolicy</span></span>](./Get-AzApiManagementPolicy.md)

[<span data-ttu-id="0855f-153">Set-Azapsananagementpolicy</span><span class="sxs-lookup"><span data-stu-id="0855f-153">Set-AzApiManagementPolicy</span></span>](./Set-AzApiManagementPolicy.md)


