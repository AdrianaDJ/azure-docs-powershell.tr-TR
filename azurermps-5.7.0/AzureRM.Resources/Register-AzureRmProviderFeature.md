---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 83EE33E5-18EF-4A7A-AEF2-E93D7A3CA541
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/register-azurermproviderfeature
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Register-AzureRmProviderFeature.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Register-AzureRmProviderFeature.md
ms.openlocfilehash: b41f7cb1c5e3ebec58e3866c94d8e2c62bdf670b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588783"
---
# <span data-ttu-id="69266-101">Register-AzureRmProviderFeature</span><span class="sxs-lookup"><span data-stu-id="69266-101">Register-AzureRmProviderFeature</span></span>

## <span data-ttu-id="69266-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="69266-102">SYNOPSIS</span></span>
<span data-ttu-id="69266-103">Hesabınızda bir Azure sağlayıcı özelliği kaydeder.</span><span class="sxs-lookup"><span data-stu-id="69266-103">Registers an Azure provider feature in your account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="69266-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="69266-104">SYNTAX</span></span>

```
Register-AzureRmProviderFeature -FeatureName <String> -ProviderNamespace <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="69266-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="69266-105">DESCRIPTION</span></span>
<span data-ttu-id="69266-106">**Register-AzureRmProviderFeature** cmdlet 'i hesabınıza bir Azure sağlayıcı özelliği kaydeder.</span><span class="sxs-lookup"><span data-stu-id="69266-106">The **Register-AzureRmProviderFeature** cmdlet registers an Azure provider feature in your account.</span></span>

## <span data-ttu-id="69266-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="69266-107">EXAMPLES</span></span>

### <span data-ttu-id="69266-108">Örnek 1: bir özelliği kaydetme</span><span class="sxs-lookup"><span data-stu-id="69266-108">Example 1: Register a feature</span></span>
```
PS C:\>Register-AzureRmProviderFeature -FeatureName AllowApplicationSecurityGroups -ProviderNamespace Microsoft.Network
```

<span data-ttu-id="69266-109">Bu, Microsoft. Network için AllowApplicationSecurityGroups özelliğini hesabınıza ekler.</span><span class="sxs-lookup"><span data-stu-id="69266-109">This adds the AllowApplicationSecurityGroups feature for Microsoft.Network to your account.</span></span>

## <span data-ttu-id="69266-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="69266-110">PARAMETERS</span></span>

### <span data-ttu-id="69266-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69266-111">-DefaultProfile</span></span>
<span data-ttu-id="69266-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="69266-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="69266-113">-FeatureName</span><span class="sxs-lookup"><span data-stu-id="69266-113">-FeatureName</span></span>
<span data-ttu-id="69266-114">Bu cmdlet 'in kaydettiğinde kullandığı özelliğin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="69266-114">Specifies the name of the feature that this cmdlet registers.</span></span>

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

### <span data-ttu-id="69266-115">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="69266-115">-ProviderNamespace</span></span>
<span data-ttu-id="69266-116">Bu cmdlet 'in sağlayıcı özelliğini kaydeden bir ad alanı belirtir.</span><span class="sxs-lookup"><span data-stu-id="69266-116">Specifies a namespace for which this cmdlet registers a provider feature.</span></span>

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

### <span data-ttu-id="69266-117">-Onay</span><span class="sxs-lookup"><span data-stu-id="69266-117">-Confirm</span></span>
<span data-ttu-id="69266-118">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="69266-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="69266-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="69266-119">-WhatIf</span></span>
<span data-ttu-id="69266-120">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="69266-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="69266-121">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="69266-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="69266-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69266-122">CommonParameters</span></span>
<span data-ttu-id="69266-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="69266-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69266-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="69266-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69266-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="69266-125">INPUTS</span></span>

### <span data-ttu-id="69266-126">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="69266-126">None</span></span>
<span data-ttu-id="69266-127">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="69266-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="69266-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="69266-128">OUTPUTS</span></span>

### <span data-ttu-id="69266-129">System. Koleksiyonlar. Generic. LIST ' 1 [Microsoft. Azure. Commands. ResourceManager. cmdlet. Sdkmodeller. PSProviderFeature]</span><span class="sxs-lookup"><span data-stu-id="69266-129">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSProviderFeature]</span></span>

## <span data-ttu-id="69266-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="69266-130">NOTES</span></span>

## <span data-ttu-id="69266-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="69266-131">RELATED LINKS</span></span>

[<span data-ttu-id="69266-132">Get-AzureRmProviderFeature</span><span class="sxs-lookup"><span data-stu-id="69266-132">Get-AzureRmProviderFeature</span></span>](./Get-AzureRmProviderFeature.md)


