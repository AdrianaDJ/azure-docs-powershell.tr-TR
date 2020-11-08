---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 83EE33E5-18EF-4A7A-AEF2-E93D7A3CA541
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/register-azurermproviderfeature
schema: 2.0.0
ms.openlocfilehash: 2371ea9a50af1d23144560acbf4fd88679f0e50d
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939844"
---
# <span data-ttu-id="f23e0-101">Register-AzureRmProviderFeature</span><span class="sxs-lookup"><span data-stu-id="f23e0-101">Register-AzureRmProviderFeature</span></span>

## <span data-ttu-id="f23e0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f23e0-102">SYNOPSIS</span></span>
<span data-ttu-id="f23e0-103">Hesabınızda bir Azure sağlayıcı özelliği kaydeder.</span><span class="sxs-lookup"><span data-stu-id="f23e0-103">Registers an Azure provider feature in your account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f23e0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f23e0-104">SYNTAX</span></span>

```
Register-AzureRmProviderFeature -FeatureName <String> -ProviderNamespace <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f23e0-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f23e0-105">DESCRIPTION</span></span>
<span data-ttu-id="f23e0-106">**Register-AzureRmProviderFeature** cmdlet 'i hesabınıza bir Azure sağlayıcı özelliği kaydeder.</span><span class="sxs-lookup"><span data-stu-id="f23e0-106">The **Register-AzureRmProviderFeature** cmdlet registers an Azure provider feature in your account.</span></span>

## <span data-ttu-id="f23e0-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f23e0-107">EXAMPLES</span></span>

### <span data-ttu-id="f23e0-108">Örnek 1: bir özelliği kaydetme</span><span class="sxs-lookup"><span data-stu-id="f23e0-108">Example 1: Register a feature</span></span>
```
PS C:\>Register-AzureRmProviderFeature -FeatureName AllowApplicationSecurityGroups -ProviderNamespace Microsoft.Network
```

<span data-ttu-id="f23e0-109">Bu, Microsoft. Network için AllowApplicationSecurityGroups özelliğini hesabınıza ekler.</span><span class="sxs-lookup"><span data-stu-id="f23e0-109">This adds the AllowApplicationSecurityGroups feature for Microsoft.Network to your account.</span></span>

## <span data-ttu-id="f23e0-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f23e0-110">PARAMETERS</span></span>

### <span data-ttu-id="f23e0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f23e0-111">-DefaultProfile</span></span>
<span data-ttu-id="f23e0-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="f23e0-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f23e0-113">-FeatureName</span><span class="sxs-lookup"><span data-stu-id="f23e0-113">-FeatureName</span></span>
<span data-ttu-id="f23e0-114">Bu cmdlet 'in kaydettiğinde kullandığı özelliğin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f23e0-114">Specifies the name of the feature that this cmdlet registers.</span></span>

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

### <span data-ttu-id="f23e0-115">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="f23e0-115">-ProviderNamespace</span></span>
<span data-ttu-id="f23e0-116">Bu cmdlet 'in sağlayıcı özelliğini kaydeden bir ad alanı belirtir.</span><span class="sxs-lookup"><span data-stu-id="f23e0-116">Specifies a namespace for which this cmdlet registers a provider feature.</span></span>

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

### <span data-ttu-id="f23e0-117">-Onay</span><span class="sxs-lookup"><span data-stu-id="f23e0-117">-Confirm</span></span>
<span data-ttu-id="f23e0-118">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f23e0-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f23e0-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f23e0-119">-WhatIf</span></span>
<span data-ttu-id="f23e0-120">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f23e0-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f23e0-121">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="f23e0-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f23e0-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f23e0-122">CommonParameters</span></span>
<span data-ttu-id="f23e0-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f23e0-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f23e0-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f23e0-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f23e0-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f23e0-125">INPUTS</span></span>

## <span data-ttu-id="f23e0-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f23e0-126">OUTPUTS</span></span>

## <span data-ttu-id="f23e0-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f23e0-127">NOTES</span></span>

## <span data-ttu-id="f23e0-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f23e0-128">RELATED LINKS</span></span>

[<span data-ttu-id="f23e0-129">Get-AzureRmProviderFeature</span><span class="sxs-lookup"><span data-stu-id="f23e0-129">Get-AzureRmProviderFeature</span></span>](./Get-AzureRmProviderFeature.md)

