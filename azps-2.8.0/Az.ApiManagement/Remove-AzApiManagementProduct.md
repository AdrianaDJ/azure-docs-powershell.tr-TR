---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: D6B7F253-03CD-40BE-87D6-E4AE300A29D5
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementProduct.md
ms.openlocfilehash: 03bc30ddfcf1543b54466dc388c70ceba330d4ec
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753452"
---
# <span data-ttu-id="118ec-101">Remove-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="118ec-101">Remove-AzApiManagementProduct</span></span>

## <span data-ttu-id="118ec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="118ec-102">SYNOPSIS</span></span>
<span data-ttu-id="118ec-103">Var olan bir API yönetim ürününü kaldırır.</span><span class="sxs-lookup"><span data-stu-id="118ec-103">Removes an existing API Management product.</span></span>

## <span data-ttu-id="118ec-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="118ec-104">SYNTAX</span></span>

```
Remove-AzApiManagementProduct -Context <PsApiManagementContext> -ProductId <String> [-DeleteSubscriptions]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="118ec-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="118ec-105">DESCRIPTION</span></span>
<span data-ttu-id="118ec-106">**Remove-Azapsananagementproduct** cmdlet 'i var olan bir API yönetim ürününü kaldırır.</span><span class="sxs-lookup"><span data-stu-id="118ec-106">The **Remove-AzApiManagementProduct** cmdlet removes an existing API Management product.</span></span>

## <span data-ttu-id="118ec-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="118ec-107">EXAMPLES</span></span>

### <span data-ttu-id="118ec-108">Örnek 1: varolan bir ürünü ve tüm abonelikleri kaldırma</span><span class="sxs-lookup"><span data-stu-id="118ec-108">Example 1: Remove an existing product and all subscriptions</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementProduct -Context $apimContext -ProductId "0123456789" -DeleteSubscriptions
```

<span data-ttu-id="118ec-109">Bu komut mevcut bir ürünü ve tüm abonelikleri kaldırır.</span><span class="sxs-lookup"><span data-stu-id="118ec-109">This command removes an existing product and all subscriptions.</span></span>

## <span data-ttu-id="118ec-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="118ec-110">PARAMETERS</span></span>

### <span data-ttu-id="118ec-111">-Context</span><span class="sxs-lookup"><span data-stu-id="118ec-111">-Context</span></span>
<span data-ttu-id="118ec-112">**Psapimanagementcontext** nesnesinin bir örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="118ec-112">Specifies an instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="118ec-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="118ec-113">-DefaultProfile</span></span>
<span data-ttu-id="118ec-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="118ec-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="118ec-115">-Deleteabonelikleri</span><span class="sxs-lookup"><span data-stu-id="118ec-115">-DeleteSubscriptions</span></span>
<span data-ttu-id="118ec-116">Ürüne aboneliklerin silineceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="118ec-116">Indicates whether to delete subscriptions to the product.</span></span>
<span data-ttu-id="118ec-117">Bu parametre ve abonelikler yoksa, bir istisna atılır.</span><span class="sxs-lookup"><span data-stu-id="118ec-117">If you do not set this parameter and subscriptions exists, an exception is thrown.</span></span>

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

### <span data-ttu-id="118ec-118">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="118ec-118">-PassThru</span></span>
<span data-ttu-id="118ec-119">Bu cmdlet 'in bir $True değerini (başarılı olursa) veya $False değerini döndürmediğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="118ec-119">Indicates that this cmdlet returns a value of $True, if it succeeds, or a value of $False, if it fails.</span></span>

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

### <span data-ttu-id="118ec-120">-ÜrünKimliği</span><span class="sxs-lookup"><span data-stu-id="118ec-120">-ProductId</span></span>
<span data-ttu-id="118ec-121">Var olan ürünün tanımlayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="118ec-121">Specifies the identifier of the existing product.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="118ec-122">-Onay</span><span class="sxs-lookup"><span data-stu-id="118ec-122">-Confirm</span></span>
<span data-ttu-id="118ec-123">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="118ec-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="118ec-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="118ec-124">-WhatIf</span></span>
<span data-ttu-id="118ec-125">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="118ec-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="118ec-126">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="118ec-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="118ec-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="118ec-127">CommonParameters</span></span>
<span data-ttu-id="118ec-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="118ec-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="118ec-129">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="118ec-129">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="118ec-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="118ec-130">INPUTS</span></span>

### <span data-ttu-id="118ec-131">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="118ec-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="118ec-132">System. String</span><span class="sxs-lookup"><span data-stu-id="118ec-132">System.String</span></span>

### <span data-ttu-id="118ec-133">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="118ec-133">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="118ec-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="118ec-134">OUTPUTS</span></span>

### <span data-ttu-id="118ec-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="118ec-135">System.Boolean</span></span>

## <span data-ttu-id="118ec-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="118ec-136">NOTES</span></span>

## <span data-ttu-id="118ec-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="118ec-137">RELATED LINKS</span></span>

[<span data-ttu-id="118ec-138">Get-Azapsanana,</span><span class="sxs-lookup"><span data-stu-id="118ec-138">Get-AzApiManagementProduct</span></span>](./Get-AzApiManagementProduct.md)

[<span data-ttu-id="118ec-139">Yeni-Azsız ürün</span><span class="sxs-lookup"><span data-stu-id="118ec-139">New-AzApiManagementProduct</span></span>](./New-AzApiManagementProduct.md)

[<span data-ttu-id="118ec-140">Set-Azapsananagementproduct</span><span class="sxs-lookup"><span data-stu-id="118ec-140">Set-AzApiManagementProduct</span></span>](./Set-AzApiManagementProduct.md)


