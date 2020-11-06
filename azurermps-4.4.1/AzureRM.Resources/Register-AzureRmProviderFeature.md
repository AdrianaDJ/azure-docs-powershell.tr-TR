---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 83EE33E5-18EF-4A7A-AEF2-E93D7A3CA541
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Register-AzureRmProviderFeature.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Register-AzureRmProviderFeature.md
ms.openlocfilehash: b519108918f2c26d86807302314a4defed1a0050
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592566"
---
# <span data-ttu-id="fa9d6-101">Register-AzureRmProviderFeature</span><span class="sxs-lookup"><span data-stu-id="fa9d6-101">Register-AzureRmProviderFeature</span></span>

## <span data-ttu-id="fa9d6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fa9d6-102">SYNOPSIS</span></span>
<span data-ttu-id="fa9d6-103">Hesabınızda bir Azure sağlayıcı özelliği kaydeder.</span><span class="sxs-lookup"><span data-stu-id="fa9d6-103">Registers an Azure provider feature in your account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fa9d6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fa9d6-104">SYNTAX</span></span>

```
Register-AzureRmProviderFeature -FeatureName <String> -ProviderNamespace <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fa9d6-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="fa9d6-105">DESCRIPTION</span></span>
<span data-ttu-id="fa9d6-106">**Register-AzureRmProviderFeature** cmdlet 'i hesabınıza bir Azure sağlayıcı özelliği kaydeder.</span><span class="sxs-lookup"><span data-stu-id="fa9d6-106">The **Register-AzureRmProviderFeature** cmdlet registers an Azure provider feature in your account.</span></span>

## <span data-ttu-id="fa9d6-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fa9d6-107">EXAMPLES</span></span>

## <span data-ttu-id="fa9d6-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fa9d6-108">PARAMETERS</span></span>

### <span data-ttu-id="fa9d6-109">-FeatureName</span><span class="sxs-lookup"><span data-stu-id="fa9d6-109">-FeatureName</span></span>
<span data-ttu-id="fa9d6-110">Bu cmdlet 'in kaydettiğinde kullandığı özelliğin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fa9d6-110">Specifies the name of the feature that this cmdlet registers.</span></span>

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

### <span data-ttu-id="fa9d6-111">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="fa9d6-111">-ProviderNamespace</span></span>
<span data-ttu-id="fa9d6-112">Bu cmdlet 'in sağlayıcı özelliğini kaydeden bir ad alanı belirtir.</span><span class="sxs-lookup"><span data-stu-id="fa9d6-112">Specifies a namespace for which this cmdlet registers a provider feature.</span></span>

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

### <span data-ttu-id="fa9d6-113">-Onay</span><span class="sxs-lookup"><span data-stu-id="fa9d6-113">-Confirm</span></span>
<span data-ttu-id="fa9d6-114">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="fa9d6-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fa9d6-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fa9d6-115">-WhatIf</span></span>
<span data-ttu-id="fa9d6-116">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="fa9d6-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fa9d6-117">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="fa9d6-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fa9d6-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa9d6-118">-DefaultProfile</span></span>
<span data-ttu-id="fa9d6-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="fa9d6-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fa9d6-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa9d6-120">CommonParameters</span></span>
<span data-ttu-id="fa9d6-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fa9d6-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa9d6-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fa9d6-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa9d6-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fa9d6-123">INPUTS</span></span>

## <span data-ttu-id="fa9d6-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fa9d6-124">OUTPUTS</span></span>

### <span data-ttu-id="fa9d6-125">System. Koleksiyonlar. Generic. LIST ' 1 [Microsoft. Azure. Commands. ResourceManager. cmdlet. Sdkmodeller. PSProviderFeature]</span><span class="sxs-lookup"><span data-stu-id="fa9d6-125">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSProviderFeature]</span></span>

## <span data-ttu-id="fa9d6-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fa9d6-126">NOTES</span></span>

## <span data-ttu-id="fa9d6-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fa9d6-127">RELATED LINKS</span></span>

[<span data-ttu-id="fa9d6-128">Get-AzureRmProviderFeature</span><span class="sxs-lookup"><span data-stu-id="fa9d6-128">Get-AzureRmProviderFeature</span></span>](./Get-AzureRmProviderFeature.md)


