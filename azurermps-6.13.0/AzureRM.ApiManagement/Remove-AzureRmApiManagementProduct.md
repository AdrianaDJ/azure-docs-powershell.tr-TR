---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: D6B7F253-03CD-40BE-87D6-E4AE300A29D5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementProduct.md
ms.openlocfilehash: 61a4ab9e7a827cffce861cc9ebaf7382e16e8fcb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762330"
---
# <span data-ttu-id="d92e7-101">Remove-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="d92e7-101">Remove-AzureRmApiManagementProduct</span></span>

## <span data-ttu-id="d92e7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d92e7-102">SYNOPSIS</span></span>
<span data-ttu-id="d92e7-103">Var olan bir API yönetim ürününü kaldırır.</span><span class="sxs-lookup"><span data-stu-id="d92e7-103">Removes an existing API Management product.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d92e7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d92e7-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementProduct -Context <PsApiManagementContext> -ProductId <String> [-DeleteSubscriptions]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d92e7-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="d92e7-105">DESCRIPTION</span></span>
<span data-ttu-id="d92e7-106">**Remove-Azurermapsananagementproduct** cmdlet 'i var olan bir API yönetim ürününü kaldırır.</span><span class="sxs-lookup"><span data-stu-id="d92e7-106">The **Remove-AzureRmApiManagementProduct** cmdlet removes an existing API Management product.</span></span>

## <span data-ttu-id="d92e7-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d92e7-107">EXAMPLES</span></span>

### <span data-ttu-id="d92e7-108">Örnek 1: varolan bir ürünü ve tüm abonelikleri kaldırma</span><span class="sxs-lookup"><span data-stu-id="d92e7-108">Example 1: Remove an existing product and all subscriptions</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementProduct -Context $apimContext -Id "0123456789" -DeleteSubscriptions -Force
```

<span data-ttu-id="d92e7-109">Bu komut mevcut bir ürünü ve tüm abonelikleri kaldırır.</span><span class="sxs-lookup"><span data-stu-id="d92e7-109">This command removes an existing product and all subscriptions.</span></span>

## <span data-ttu-id="d92e7-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d92e7-110">PARAMETERS</span></span>

### <span data-ttu-id="d92e7-111">-Context</span><span class="sxs-lookup"><span data-stu-id="d92e7-111">-Context</span></span>
<span data-ttu-id="d92e7-112">**Psapimanagementcontext** nesnesinin bir örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="d92e7-112">Specifies an instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="d92e7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d92e7-113">-DefaultProfile</span></span>
<span data-ttu-id="d92e7-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d92e7-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d92e7-115">-Deleteabonelikleri</span><span class="sxs-lookup"><span data-stu-id="d92e7-115">-DeleteSubscriptions</span></span>
<span data-ttu-id="d92e7-116">Ürüne aboneliklerin silineceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="d92e7-116">Indicates whether to delete subscriptions to the product.</span></span>
<span data-ttu-id="d92e7-117">Bu parametre ve abonelikler yoksa, bir istisna atılır.</span><span class="sxs-lookup"><span data-stu-id="d92e7-117">If you do not set this parameter and subscriptions exists, an exception is thrown.</span></span>

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

### <span data-ttu-id="d92e7-118">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="d92e7-118">-PassThru</span></span>
<span data-ttu-id="d92e7-119">Bu cmdlet 'in bir $True değerini (başarılı olursa) veya $False değerini döndürmediğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="d92e7-119">Indicates that this cmdlet returns a value of $True, if it succeeds, or a value of $False, if it fails.</span></span>

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

### <span data-ttu-id="d92e7-120">-ÜrünKimliği</span><span class="sxs-lookup"><span data-stu-id="d92e7-120">-ProductId</span></span>
<span data-ttu-id="d92e7-121">Var olan ürünün tanımlayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d92e7-121">Specifies the identifier of the existing product.</span></span>

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

### <span data-ttu-id="d92e7-122">-Onay</span><span class="sxs-lookup"><span data-stu-id="d92e7-122">-Confirm</span></span>
<span data-ttu-id="d92e7-123">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d92e7-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d92e7-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d92e7-124">-WhatIf</span></span>
<span data-ttu-id="d92e7-125">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d92e7-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d92e7-126">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d92e7-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d92e7-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d92e7-127">CommonParameters</span></span>
<span data-ttu-id="d92e7-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d92e7-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d92e7-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d92e7-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d92e7-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d92e7-130">INPUTS</span></span>

### <span data-ttu-id="d92e7-131">Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext</span><span class="sxs-lookup"><span data-stu-id="d92e7-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="d92e7-132">System. String</span><span class="sxs-lookup"><span data-stu-id="d92e7-132">System.String</span></span>

### <span data-ttu-id="d92e7-133">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="d92e7-133">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="d92e7-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d92e7-134">OUTPUTS</span></span>

### <span data-ttu-id="d92e7-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d92e7-135">System.Boolean</span></span>

## <span data-ttu-id="d92e7-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d92e7-136">NOTES</span></span>

## <span data-ttu-id="d92e7-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d92e7-137">RELATED LINKS</span></span>

[<span data-ttu-id="d92e7-138">Get-azurermapsanana</span><span class="sxs-lookup"><span data-stu-id="d92e7-138">Get-AzureRmApiManagementProduct</span></span>](./Get-AzureRmApiManagementProduct.md)

[<span data-ttu-id="d92e7-139">Yeni-azurermapsanana</span><span class="sxs-lookup"><span data-stu-id="d92e7-139">New-AzureRmApiManagementProduct</span></span>](./New-AzureRmApiManagementProduct.md)

[<span data-ttu-id="d92e7-140">Set-Azurermapımanagementproduct</span><span class="sxs-lookup"><span data-stu-id="d92e7-140">Set-AzureRmApiManagementProduct</span></span>](./Set-AzureRmApiManagementProduct.md)


