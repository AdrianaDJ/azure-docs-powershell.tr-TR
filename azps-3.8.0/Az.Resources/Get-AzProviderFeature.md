---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 2970E81E-A788-4829-B1FF-B522A91DE4B1
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azproviderfeature
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzProviderFeature.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzProviderFeature.md
ms.openlocfilehash: db18420623c85bcee9f7e52031d1645097dc2fe0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098098"
---
# <span data-ttu-id="7d8d5-101">Get-AzProviderFeature</span><span class="sxs-lookup"><span data-stu-id="7d8d5-101">Get-AzProviderFeature</span></span>

## <span data-ttu-id="7d8d5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7d8d5-102">SYNOPSIS</span></span>
<span data-ttu-id="7d8d5-103">Azure sağlayıcı özellikleri hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="7d8d5-103">Gets information about Azure provider features.</span></span>

## <span data-ttu-id="7d8d5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7d8d5-104">SYNTAX</span></span>

### <span data-ttu-id="7d8d5-105">ListAvailableParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="7d8d5-105">ListAvailableParameterSet (Default)</span></span>
```
Get-AzProviderFeature [-ProviderNamespace <String>] [-ListAvailable] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7d8d5-106">GetFeature</span><span class="sxs-lookup"><span data-stu-id="7d8d5-106">GetFeature</span></span>
```
Get-AzProviderFeature -ProviderNamespace <String> -FeatureName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7d8d5-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="7d8d5-107">DESCRIPTION</span></span>
<span data-ttu-id="7d8d5-108">**Get-AzProviderFeature** cmdlet 'i Azure sağlayıcı özelliklerinin özellik adını, sağlayıcı adını ve kayıt durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="7d8d5-108">The **Get-AzProviderFeature** cmdlet gets the feature name, provider name, and registration status for Azure provider features.</span></span>

## <span data-ttu-id="7d8d5-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7d8d5-109">EXAMPLES</span></span>

### <span data-ttu-id="7d8d5-110">Örnek 1: kullanılabilir tüm özellikleri alma</span><span class="sxs-lookup"><span data-stu-id="7d8d5-110">Example 1: Get all available features</span></span>
```
PS C:\>Get-AzProviderFeature -ListAvailable
```

<span data-ttu-id="7d8d5-111">Bu komut kullanılabilir tüm özellikleri alır.</span><span class="sxs-lookup"><span data-stu-id="7d8d5-111">This command gets all available features.</span></span>

### <span data-ttu-id="7d8d5-112">Örnek 2: belirli bir özellikle ilgili bilgileri alma</span><span class="sxs-lookup"><span data-stu-id="7d8d5-112">Example 2: Get information about a specific feature</span></span>
```
PS C:\>Get-AzProviderFeature -FeatureName "AllowPreReleaseRegions" -ProviderNamespace "Microsoft.Compute"
```

<span data-ttu-id="7d8d5-113">Bu komut, belirtilen sağlayıcı için AllowPreReleaseRegions adlı özelliğin bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="7d8d5-113">This command gets information for the feature named AllowPreReleaseRegions for the specified provider.</span></span>

## <span data-ttu-id="7d8d5-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7d8d5-114">PARAMETERS</span></span>

### <span data-ttu-id="7d8d5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d8d5-115">-DefaultProfile</span></span>
<span data-ttu-id="7d8d5-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="7d8d5-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7d8d5-117">-FeatureName</span><span class="sxs-lookup"><span data-stu-id="7d8d5-117">-FeatureName</span></span>
<span data-ttu-id="7d8d5-118">Alınacak özelliğin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7d8d5-118">Specifies the name of the feature to get.</span></span>

```yaml
Type: System.String
Parameter Sets: GetFeature
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d8d5-119">-ListAvailable</span><span class="sxs-lookup"><span data-stu-id="7d8d5-119">-ListAvailable</span></span>
<span data-ttu-id="7d8d5-120">Bu cmdlet 'in tüm özellikleri aldığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7d8d5-120">Indicates that this cmdlet gets all features.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ListAvailableParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d8d5-121">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="7d8d5-121">-ProviderNamespace</span></span>
<span data-ttu-id="7d8d5-122">Bu cmdlet 'in sağlayıcı özelliklerini aldığı ad boşluğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="7d8d5-122">Specifies the namespace for which this cmdlet gets provider features.</span></span>

```yaml
Type: System.String
Parameter Sets: ListAvailableParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetFeature
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d8d5-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d8d5-123">CommonParameters</span></span>
<span data-ttu-id="7d8d5-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7d8d5-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d8d5-125">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="7d8d5-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d8d5-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7d8d5-126">INPUTS</span></span>

### <span data-ttu-id="7d8d5-127">System. String</span><span class="sxs-lookup"><span data-stu-id="7d8d5-127">System.String</span></span>

## <span data-ttu-id="7d8d5-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7d8d5-128">OUTPUTS</span></span>

### <span data-ttu-id="7d8d5-129">Microsoft. Azure. Commands. ResourceManager. cmdlet. Sdkmodeller. PSProviderFeature</span><span class="sxs-lookup"><span data-stu-id="7d8d5-129">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSProviderFeature</span></span>

## <span data-ttu-id="7d8d5-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7d8d5-130">NOTES</span></span>

## <span data-ttu-id="7d8d5-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7d8d5-131">RELATED LINKS</span></span>

[<span data-ttu-id="7d8d5-132">Register-AzProviderFeature</span><span class="sxs-lookup"><span data-stu-id="7d8d5-132">Register-AzProviderFeature</span></span>](./Register-AzProviderFeature.md)

