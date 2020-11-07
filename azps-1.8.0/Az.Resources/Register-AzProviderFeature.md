---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 83EE33E5-18EF-4A7A-AEF2-E93D7A3CA541
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/register-azproviderfeature
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Register-AzProviderFeature.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Register-AzProviderFeature.md
ms.openlocfilehash: 57a01f831ab92b7ae8ca45fbf9535ed4fa7df0a1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93759373"
---
# <span data-ttu-id="d2bfe-101">Register-AzProviderFeature</span><span class="sxs-lookup"><span data-stu-id="d2bfe-101">Register-AzProviderFeature</span></span>

## <span data-ttu-id="d2bfe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d2bfe-102">SYNOPSIS</span></span>
<span data-ttu-id="d2bfe-103">Hesabınızda bir Azure sağlayıcı özelliği kaydeder.</span><span class="sxs-lookup"><span data-stu-id="d2bfe-103">Registers an Azure provider feature in your account.</span></span>

## <span data-ttu-id="d2bfe-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d2bfe-104">SYNTAX</span></span>

```
Register-AzProviderFeature -FeatureName <String> -ProviderNamespace <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d2bfe-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="d2bfe-105">DESCRIPTION</span></span>
<span data-ttu-id="d2bfe-106">**Register-AzProviderFeature** cmdlet 'i hesabınıza bir Azure sağlayıcı özelliği kaydeder.</span><span class="sxs-lookup"><span data-stu-id="d2bfe-106">The **Register-AzProviderFeature** cmdlet registers an Azure provider feature in your account.</span></span>

## <span data-ttu-id="d2bfe-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d2bfe-107">EXAMPLES</span></span>

### <span data-ttu-id="d2bfe-108">Örnek 1: bir özelliği kaydetme</span><span class="sxs-lookup"><span data-stu-id="d2bfe-108">Example 1: Register a feature</span></span>
```
PS C:\>Register-AzProviderFeature -FeatureName AllowApplicationSecurityGroups -ProviderNamespace Microsoft.Network
```

<span data-ttu-id="d2bfe-109">Bu, Microsoft. Network için AllowApplicationSecurityGroups özelliğini hesabınıza ekler.</span><span class="sxs-lookup"><span data-stu-id="d2bfe-109">This adds the AllowApplicationSecurityGroups feature for Microsoft.Network to your account.</span></span>

## <span data-ttu-id="d2bfe-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d2bfe-110">PARAMETERS</span></span>

### <span data-ttu-id="d2bfe-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2bfe-111">-DefaultProfile</span></span>
<span data-ttu-id="d2bfe-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="d2bfe-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d2bfe-113">-FeatureName</span><span class="sxs-lookup"><span data-stu-id="d2bfe-113">-FeatureName</span></span>
<span data-ttu-id="d2bfe-114">Bu cmdlet 'in kaydettiğinde kullandığı özelliğin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d2bfe-114">Specifies the name of the feature that this cmdlet registers.</span></span>

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

### <span data-ttu-id="d2bfe-115">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="d2bfe-115">-ProviderNamespace</span></span>
<span data-ttu-id="d2bfe-116">Bu cmdlet 'in sağlayıcı özelliğini kaydeden bir ad alanı belirtir.</span><span class="sxs-lookup"><span data-stu-id="d2bfe-116">Specifies a namespace for which this cmdlet registers a provider feature.</span></span>

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

### <span data-ttu-id="d2bfe-117">-Onay</span><span class="sxs-lookup"><span data-stu-id="d2bfe-117">-Confirm</span></span>
<span data-ttu-id="d2bfe-118">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d2bfe-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d2bfe-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d2bfe-119">-WhatIf</span></span>
<span data-ttu-id="d2bfe-120">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d2bfe-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d2bfe-121">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d2bfe-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d2bfe-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2bfe-122">CommonParameters</span></span>
<span data-ttu-id="d2bfe-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d2bfe-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2bfe-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2bfe-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2bfe-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d2bfe-125">INPUTS</span></span>

### <span data-ttu-id="d2bfe-126">System. String</span><span class="sxs-lookup"><span data-stu-id="d2bfe-126">System.String</span></span>

## <span data-ttu-id="d2bfe-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d2bfe-127">OUTPUTS</span></span>

### <span data-ttu-id="d2bfe-128">Microsoft. Azure. Commands. ResourceManager. cmdlet. Sdkmodeller. PSProviderFeature</span><span class="sxs-lookup"><span data-stu-id="d2bfe-128">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSProviderFeature</span></span>

## <span data-ttu-id="d2bfe-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d2bfe-129">NOTES</span></span>

## <span data-ttu-id="d2bfe-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d2bfe-130">RELATED LINKS</span></span>

[<span data-ttu-id="d2bfe-131">Get-AzProviderFeature</span><span class="sxs-lookup"><span data-stu-id="d2bfe-131">Get-AzProviderFeature</span></span>](./Get-AzProviderFeature.md)


