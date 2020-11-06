---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: D6B7F253-03CD-40BE-87D6-E4AE300A29D5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementProduct.md
ms.openlocfilehash: 5c5bd7d0b7df385645bdb51d684616f2c0d7eaa5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586840"
---
# <span data-ttu-id="e0658-101">Remove-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="e0658-101">Remove-AzureRmApiManagementProduct</span></span>

## <span data-ttu-id="e0658-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e0658-102">SYNOPSIS</span></span>
<span data-ttu-id="e0658-103">Var olan bir API yönetim ürününü kaldırır.</span><span class="sxs-lookup"><span data-stu-id="e0658-103">Removes an existing API Management product.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e0658-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e0658-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementProduct -Context <PsApiManagementContext> -ProductId <String> [-DeleteSubscriptions]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e0658-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e0658-105">DESCRIPTION</span></span>
<span data-ttu-id="e0658-106">**Remove-Azurermapsananagementproduct** cmdlet 'i var olan bir API yönetim ürününü kaldırır.</span><span class="sxs-lookup"><span data-stu-id="e0658-106">The **Remove-AzureRmApiManagementProduct** cmdlet removes an existing API Management product.</span></span>

## <span data-ttu-id="e0658-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e0658-107">EXAMPLES</span></span>

### <span data-ttu-id="e0658-108">Örnek 1: varolan bir ürünü ve tüm abonelikleri kaldırma</span><span class="sxs-lookup"><span data-stu-id="e0658-108">Example 1: Remove an existing product and all subscriptions</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementProduct -Context $apimContext -Id "0123456789" -DeleteSubscriptions -Force
```

<span data-ttu-id="e0658-109">Bu komut mevcut bir ürünü ve tüm abonelikleri kaldırır.</span><span class="sxs-lookup"><span data-stu-id="e0658-109">This command removes an existing product and all subscriptions.</span></span>

## <span data-ttu-id="e0658-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e0658-110">PARAMETERS</span></span>

### <span data-ttu-id="e0658-111">-Context</span><span class="sxs-lookup"><span data-stu-id="e0658-111">-Context</span></span>
<span data-ttu-id="e0658-112">**Psapimanagementcontext** nesnesinin bir örneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e0658-112">Specifies an instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="e0658-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0658-113">-DefaultProfile</span></span>
<span data-ttu-id="e0658-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e0658-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="e0658-115">-Deleteabonelikleri</span><span class="sxs-lookup"><span data-stu-id="e0658-115">-DeleteSubscriptions</span></span>
<span data-ttu-id="e0658-116">Ürüne aboneliklerin silineceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e0658-116">Indicates whether to delete subscriptions to the product.</span></span>
<span data-ttu-id="e0658-117">Bu parametre ve abonelikler yoksa, bir istisna atılır.</span><span class="sxs-lookup"><span data-stu-id="e0658-117">If you do not set this parameter and subscriptions exists, an exception is thrown.</span></span>

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

### <span data-ttu-id="e0658-118">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="e0658-118">-PassThru</span></span>
<span data-ttu-id="e0658-119">Bu cmdlet 'in bir $True değerini (başarılı olursa) veya $False değerini döndürmediğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e0658-119">Indicates that this cmdlet returns a value of $True, if it succeeds, or a value of $False, if it fails.</span></span>

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

### <span data-ttu-id="e0658-120">-ÜrünKimliği</span><span class="sxs-lookup"><span data-stu-id="e0658-120">-ProductId</span></span>
<span data-ttu-id="e0658-121">Var olan ürünün tanımlayıcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e0658-121">Specifies the identifier of the existing product.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0658-122">-Onay</span><span class="sxs-lookup"><span data-stu-id="e0658-122">-Confirm</span></span>
<span data-ttu-id="e0658-123">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e0658-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e0658-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e0658-124">-WhatIf</span></span>
<span data-ttu-id="e0658-125">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e0658-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e0658-126">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e0658-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e0658-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0658-127">CommonParameters</span></span>
<span data-ttu-id="e0658-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e0658-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0658-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e0658-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0658-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e0658-130">INPUTS</span></span>

### <span data-ttu-id="e0658-131">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="e0658-131">None</span></span>
<span data-ttu-id="e0658-132">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="e0658-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e0658-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e0658-133">OUTPUTS</span></span>

### <span data-ttu-id="e0658-134">bool</span><span class="sxs-lookup"><span data-stu-id="e0658-134">bool</span></span>

## <span data-ttu-id="e0658-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e0658-135">NOTES</span></span>

## <span data-ttu-id="e0658-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e0658-136">RELATED LINKS</span></span>

[<span data-ttu-id="e0658-137">Get-azurermapsanana</span><span class="sxs-lookup"><span data-stu-id="e0658-137">Get-AzureRmApiManagementProduct</span></span>](./Get-AzureRmApiManagementProduct.md)

[<span data-ttu-id="e0658-138">Yeni-azurermapsanana</span><span class="sxs-lookup"><span data-stu-id="e0658-138">New-AzureRmApiManagementProduct</span></span>](./New-AzureRmApiManagementProduct.md)

[<span data-ttu-id="e0658-139">Set-Azurermapımanagementproduct</span><span class="sxs-lookup"><span data-stu-id="e0658-139">Set-AzureRmApiManagementProduct</span></span>](./Set-AzureRmApiManagementProduct.md)


