---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: D6B7F253-03CD-40BE-87D6-E4AE300A29D5
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementProduct.md
ms.openlocfilehash: 505a26c48e53fe05e8724d61d5ddb66981e87ee9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587029"
---
# <span data-ttu-id="7fe94-101">Remove-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="7fe94-101">Remove-AzureRmApiManagementProduct</span></span>

## <span data-ttu-id="7fe94-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7fe94-102">SYNOPSIS</span></span>
<span data-ttu-id="7fe94-103">Var olan bir API yönetim ürününü kaldırır.</span><span class="sxs-lookup"><span data-stu-id="7fe94-103">Removes an existing API Management product.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7fe94-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7fe94-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementProduct -Context <PsApiManagementContext> -ProductId <String> [-DeleteSubscriptions]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7fe94-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="7fe94-105">DESCRIPTION</span></span>
<span data-ttu-id="7fe94-106">**Remove-Azurermapsananagementproduct** cmdlet 'i var olan bir API yönetim ürününü kaldırır.</span><span class="sxs-lookup"><span data-stu-id="7fe94-106">The **Remove-AzureRmApiManagementProduct** cmdlet removes an existing API Management product.</span></span>

## <span data-ttu-id="7fe94-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7fe94-107">EXAMPLES</span></span>

### <span data-ttu-id="7fe94-108">Örnek 1: varolan bir ürünü ve tüm abonelikleri kaldırma</span><span class="sxs-lookup"><span data-stu-id="7fe94-108">Example 1: Remove an existing product and all subscriptions</span></span>
```
PS C:\>Remove-AzureRmApiManagementProduct -Context $APImContext -Id "0123456789" -DeleteSubscriptions -Force
```

<span data-ttu-id="7fe94-109">Bu komut mevcut bir ürünü ve tüm abonelikleri kaldırır.</span><span class="sxs-lookup"><span data-stu-id="7fe94-109">This command removes an existing product and all subscriptions.</span></span>

## <span data-ttu-id="7fe94-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7fe94-110">PARAMETERS</span></span>

### <span data-ttu-id="7fe94-111">-Context</span><span class="sxs-lookup"><span data-stu-id="7fe94-111">-Context</span></span>
<span data-ttu-id="7fe94-112">**Psapimanagementcontext** nesnesinin bir örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="7fe94-112">Specifies an instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="7fe94-113">-Deleteabonelikleri</span><span class="sxs-lookup"><span data-stu-id="7fe94-113">-DeleteSubscriptions</span></span>
<span data-ttu-id="7fe94-114">Ürüne aboneliklerin silineceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="7fe94-114">Indicates whether to delete subscriptions to the product.</span></span>
<span data-ttu-id="7fe94-115">Bu parametre ve abonelikler yoksa, bir istisna atılır.</span><span class="sxs-lookup"><span data-stu-id="7fe94-115">If you do not set this parameter and subscriptions exists, an exception is thrown.</span></span>

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

### <span data-ttu-id="7fe94-116">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="7fe94-116">-PassThru</span></span>
<span data-ttu-id="7fe94-117">Bu cmdlet 'in bir $True değerini (başarılı olursa) veya $False değerini döndürmediğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="7fe94-117">Indicates that this cmdlet returns a value of $True, if it succeeds, or a value of $False, if it fails.</span></span>

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

### <span data-ttu-id="7fe94-118">-ÜrünKimliği</span><span class="sxs-lookup"><span data-stu-id="7fe94-118">-ProductId</span></span>
<span data-ttu-id="7fe94-119">Var olan ürünün tanımlayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7fe94-119">Specifies the identifier of the existing product.</span></span>

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

### <span data-ttu-id="7fe94-120">-Onay</span><span class="sxs-lookup"><span data-stu-id="7fe94-120">-Confirm</span></span>
<span data-ttu-id="7fe94-121">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="7fe94-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7fe94-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7fe94-122">-WhatIf</span></span>
<span data-ttu-id="7fe94-123">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7fe94-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7fe94-124">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="7fe94-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7fe94-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7fe94-125">-DefaultProfile</span></span>
<span data-ttu-id="7fe94-126">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7fe94-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7fe94-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7fe94-127">CommonParameters</span></span>
<span data-ttu-id="7fe94-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7fe94-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7fe94-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7fe94-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7fe94-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7fe94-130">INPUTS</span></span>

## <span data-ttu-id="7fe94-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7fe94-131">OUTPUTS</span></span>

### <span data-ttu-id="7fe94-132">bool</span><span class="sxs-lookup"><span data-stu-id="7fe94-132">bool</span></span>

## <span data-ttu-id="7fe94-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7fe94-133">NOTES</span></span>

## <span data-ttu-id="7fe94-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7fe94-134">RELATED LINKS</span></span>

[<span data-ttu-id="7fe94-135">Get-azurermapsanana</span><span class="sxs-lookup"><span data-stu-id="7fe94-135">Get-AzureRmApiManagementProduct</span></span>](./Get-AzureRmApiManagementProduct.md)

[<span data-ttu-id="7fe94-136">Yeni-azurermapsanana</span><span class="sxs-lookup"><span data-stu-id="7fe94-136">New-AzureRmApiManagementProduct</span></span>](./New-AzureRmApiManagementProduct.md)

[<span data-ttu-id="7fe94-137">Set-Azurermapımanagementproduct</span><span class="sxs-lookup"><span data-stu-id="7fe94-137">Set-AzureRmApiManagementProduct</span></span>](./Set-AzureRmApiManagementProduct.md)


