---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/unregister-azproviderfeature
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Unregister-AzProviderFeature.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Unregister-AzProviderFeature.md
ms.openlocfilehash: 6cb27f66871038fa1849671391e1d7d9f8f3ccd7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94266393"
---
# <span data-ttu-id="ad2aa-101">Unregister-AzProviderFeature</span><span class="sxs-lookup"><span data-stu-id="ad2aa-101">Unregister-AzProviderFeature</span></span>

## <span data-ttu-id="ad2aa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ad2aa-102">SYNOPSIS</span></span>
<span data-ttu-id="ad2aa-103">Hesabınızdaki bir Azure sağlayıcı özelliğinin kaydını siler.</span><span class="sxs-lookup"><span data-stu-id="ad2aa-103">Unregisters an Azure provider feature in your account.</span></span>

## <span data-ttu-id="ad2aa-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ad2aa-104">SYNTAX</span></span>

```
Unregister-AzProviderFeature -FeatureName <String> -ProviderNamespace <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ad2aa-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ad2aa-105">DESCRIPTION</span></span>
<span data-ttu-id="ad2aa-106">**Unregister-AzProviderFeature** cmdlet 'i hesabınızdaki bir Azure sağlayıcı özelliğinin kaydını siler.</span><span class="sxs-lookup"><span data-stu-id="ad2aa-106">The **Unregister-AzProviderFeature** cmdlet unregisters an Azure provider feature in your account.</span></span>

## <span data-ttu-id="ad2aa-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ad2aa-107">EXAMPLES</span></span>

### <span data-ttu-id="ad2aa-108">Örnek 1: özelliğin kaydını silme</span><span class="sxs-lookup"><span data-stu-id="ad2aa-108">Example 1: Unregister a feature</span></span>
```
PS C:\>Unregister-AzProviderFeature -FeatureName AllowApplicationSecurityGroups -ProviderNamespace Microsoft.Network
```

<span data-ttu-id="ad2aa-109">Bu işlem, Microsoft. Network için AllowApplicationSecurityGroups özelliğinin hesabınızdan kaydını siler.</span><span class="sxs-lookup"><span data-stu-id="ad2aa-109">This unregisters the AllowApplicationSecurityGroups feature for Microsoft.Network from your account.</span></span>

## <span data-ttu-id="ad2aa-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ad2aa-110">PARAMETERS</span></span>

### <span data-ttu-id="ad2aa-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad2aa-111">-DefaultProfile</span></span>
<span data-ttu-id="ad2aa-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ad2aa-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad2aa-113">-FeatureName</span><span class="sxs-lookup"><span data-stu-id="ad2aa-113">-FeatureName</span></span>
<span data-ttu-id="ad2aa-114">Özellik adı.</span><span class="sxs-lookup"><span data-stu-id="ad2aa-114">The feature name.</span></span>

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

### <span data-ttu-id="ad2aa-115">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="ad2aa-115">-ProviderNamespace</span></span>
<span data-ttu-id="ad2aa-116">Kaynak sağlayıcı ad alanı.</span><span class="sxs-lookup"><span data-stu-id="ad2aa-116">The resource provider namespace.</span></span>

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

### <span data-ttu-id="ad2aa-117">-Onay</span><span class="sxs-lookup"><span data-stu-id="ad2aa-117">-Confirm</span></span>
<span data-ttu-id="ad2aa-118">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ad2aa-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad2aa-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad2aa-119">-WhatIf</span></span>
<span data-ttu-id="ad2aa-120">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ad2aa-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ad2aa-121">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ad2aa-121">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad2aa-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad2aa-122">CommonParameters</span></span>
<span data-ttu-id="ad2aa-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ad2aa-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad2aa-124">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="ad2aa-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad2aa-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ad2aa-125">INPUTS</span></span>

### <span data-ttu-id="ad2aa-126">System. String</span><span class="sxs-lookup"><span data-stu-id="ad2aa-126">System.String</span></span>

## <span data-ttu-id="ad2aa-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ad2aa-127">OUTPUTS</span></span>

### <span data-ttu-id="ad2aa-128">Microsoft. Azure. Commands. ResourceManager. cmdlet. Sdkmodeller. PSProviderFeature</span><span class="sxs-lookup"><span data-stu-id="ad2aa-128">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSProviderFeature</span></span>

## <span data-ttu-id="ad2aa-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ad2aa-129">NOTES</span></span>

## <span data-ttu-id="ad2aa-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ad2aa-130">RELATED LINKS</span></span>
