---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 83EE33E5-18EF-4A7A-AEF2-E93D7A3CA541
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/register-Azproviderfeature
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Register-AzProviderFeature.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Register-AzProviderFeature.md
ms.openlocfilehash: b7c2be59ecf43c117a459d489af70dac7c836094
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936375"
---
# <span data-ttu-id="694d7-101">Register-AzProviderFeature</span><span class="sxs-lookup"><span data-stu-id="694d7-101">Register-AzProviderFeature</span></span>

## <span data-ttu-id="694d7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="694d7-102">SYNOPSIS</span></span>
<span data-ttu-id="694d7-103">Hesabınızda bir Azure sağlayıcı özelliği kaydeder.</span><span class="sxs-lookup"><span data-stu-id="694d7-103">Registers an Azure provider feature in your account.</span></span>

## <span data-ttu-id="694d7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="694d7-104">SYNTAX</span></span>

```
Register-AzProviderFeature -FeatureName <String> -ProviderNamespace <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="694d7-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="694d7-105">DESCRIPTION</span></span>
<span data-ttu-id="694d7-106">**Register-AzProviderFeature** cmdlet 'i hesabınıza bir Azure sağlayıcı özelliği kaydeder.</span><span class="sxs-lookup"><span data-stu-id="694d7-106">The **Register-AzProviderFeature** cmdlet registers an Azure provider feature in your account.</span></span>

## <span data-ttu-id="694d7-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="694d7-107">EXAMPLES</span></span>

### <span data-ttu-id="694d7-108">Örnek 1: bir özelliği kaydetme</span><span class="sxs-lookup"><span data-stu-id="694d7-108">Example 1: Register a feature</span></span>
```
PS C:\>Register-AzProviderFeature -FeatureName AllowApplicationSecurityGroups -ProviderNamespace Microsoft.Network
```

<span data-ttu-id="694d7-109">Bu, Microsoft. Network için AllowApplicationSecurityGroups özelliğini hesabınıza ekler.</span><span class="sxs-lookup"><span data-stu-id="694d7-109">This adds the AllowApplicationSecurityGroups feature for Microsoft.Network to your account.</span></span>

## <span data-ttu-id="694d7-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="694d7-110">PARAMETERS</span></span>

### <span data-ttu-id="694d7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="694d7-111">-DefaultProfile</span></span>
<span data-ttu-id="694d7-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="694d7-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="694d7-113">-FeatureName</span><span class="sxs-lookup"><span data-stu-id="694d7-113">-FeatureName</span></span>
<span data-ttu-id="694d7-114">Bu cmdlet 'in kaydettiğinde kullandığı özelliğin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="694d7-114">Specifies the name of the feature that this cmdlet registers.</span></span>

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

### <span data-ttu-id="694d7-115">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="694d7-115">-ProviderNamespace</span></span>
<span data-ttu-id="694d7-116">Bu cmdlet 'in sağlayıcı özelliğini kaydeden bir ad alanı belirtir.</span><span class="sxs-lookup"><span data-stu-id="694d7-116">Specifies a namespace for which this cmdlet registers a provider feature.</span></span>

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

### <span data-ttu-id="694d7-117">-Onay</span><span class="sxs-lookup"><span data-stu-id="694d7-117">-Confirm</span></span>
<span data-ttu-id="694d7-118">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="694d7-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="694d7-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="694d7-119">-WhatIf</span></span>
<span data-ttu-id="694d7-120">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="694d7-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="694d7-121">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="694d7-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="694d7-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="694d7-122">CommonParameters</span></span>
<span data-ttu-id="694d7-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="694d7-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="694d7-124">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="694d7-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="694d7-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="694d7-125">INPUTS</span></span>

## <span data-ttu-id="694d7-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="694d7-126">OUTPUTS</span></span>

## <span data-ttu-id="694d7-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="694d7-127">NOTES</span></span>

## <span data-ttu-id="694d7-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="694d7-128">RELATED LINKS</span></span>

[<span data-ttu-id="694d7-129">Get-AzProviderFeature</span><span class="sxs-lookup"><span data-stu-id="694d7-129">Get-AzProviderFeature</span></span>](./Get-AzProviderFeature.md)


