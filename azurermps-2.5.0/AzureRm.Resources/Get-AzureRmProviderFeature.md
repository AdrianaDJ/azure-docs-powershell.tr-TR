---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 2970E81E-A788-4829-B1FF-B522A91DE4B1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermproviderfeature
schema: 2.0.0
ms.openlocfilehash: 182accdabc368e72451a0c1d9a1d78f1cf561730
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939478"
---
# <span data-ttu-id="7a798-101">Get-AzureRmProviderFeature</span><span class="sxs-lookup"><span data-stu-id="7a798-101">Get-AzureRmProviderFeature</span></span>

## <span data-ttu-id="7a798-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7a798-102">SYNOPSIS</span></span>
<span data-ttu-id="7a798-103">Azure sağlayıcı özellikleri hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="7a798-103">Gets information about Azure provider features.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7a798-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7a798-104">SYNTAX</span></span>

### <span data-ttu-id="7a798-105">ListAvailableParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="7a798-105">ListAvailableParameterSet (Default)</span></span>
```
Get-AzureRmProviderFeature [-ProviderNamespace <String>] [-ListAvailable]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7a798-106">GetFeature</span><span class="sxs-lookup"><span data-stu-id="7a798-106">GetFeature</span></span>
```
Get-AzureRmProviderFeature -ProviderNamespace <String> -FeatureName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7a798-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="7a798-107">DESCRIPTION</span></span>
<span data-ttu-id="7a798-108">**Get-AzureRmProviderFeature** cmdlet 'i Azure sağlayıcı özelliklerinin özellik adını, sağlayıcı adını ve kayıt durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="7a798-108">The **Get-AzureRmProviderFeature** cmdlet gets the feature name, provider name, and registration status for Azure provider features.</span></span>

## <span data-ttu-id="7a798-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7a798-109">EXAMPLES</span></span>

### <span data-ttu-id="7a798-110">Örnek 1: kullanılabilir tüm özellikleri alma</span><span class="sxs-lookup"><span data-stu-id="7a798-110">Example 1: Get all available features</span></span>
```
PS C:\>Get-AzureRmProviderFeature -ListAvailable
```

<span data-ttu-id="7a798-111">Bu komut kullanılabilir tüm özellikleri alır.</span><span class="sxs-lookup"><span data-stu-id="7a798-111">This command gets all available features.</span></span>

### <span data-ttu-id="7a798-112">Örnek 2: belirli bir özellikle ilgili bilgileri alma</span><span class="sxs-lookup"><span data-stu-id="7a798-112">Example 2: Get information about a specific feature</span></span>
```
PS C:\>Get-AzureRmProviderFeature -FeatureName "AllowPreReleaseRegions" -ProviderNamespace "Microsoft.Compute"
```

<span data-ttu-id="7a798-113">Bu komut, belirtilen sağlayıcı için AllowPreReleaseRegions adlı özelliğin bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="7a798-113">This command gets information for the feature named AllowPreReleaseRegions for the specified provider.</span></span>

## <span data-ttu-id="7a798-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7a798-114">PARAMETERS</span></span>

### <span data-ttu-id="7a798-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a798-115">-DefaultProfile</span></span>
<span data-ttu-id="7a798-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="7a798-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7a798-117">-FeatureName</span><span class="sxs-lookup"><span data-stu-id="7a798-117">-FeatureName</span></span>
<span data-ttu-id="7a798-118">Alınacak özelliğin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7a798-118">Specifies the name of the feature to get.</span></span>

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

### <span data-ttu-id="7a798-119">-ListAvailable</span><span class="sxs-lookup"><span data-stu-id="7a798-119">-ListAvailable</span></span>
<span data-ttu-id="7a798-120">Bu cmdlet 'in tüm özellikleri aldığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7a798-120">Indicates that this cmdlet gets all features.</span></span>

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

### <span data-ttu-id="7a798-121">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="7a798-121">-ProviderNamespace</span></span>
<span data-ttu-id="7a798-122">Bu cmdlet 'in sağlayıcı özelliklerini aldığı ad boşluğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="7a798-122">Specifies the namespace for which this cmdlet gets provider features.</span></span>

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

### <span data-ttu-id="7a798-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a798-123">CommonParameters</span></span>
<span data-ttu-id="7a798-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7a798-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a798-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7a798-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a798-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7a798-126">INPUTS</span></span>

## <span data-ttu-id="7a798-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7a798-127">OUTPUTS</span></span>

## <span data-ttu-id="7a798-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7a798-128">NOTES</span></span>

## <span data-ttu-id="7a798-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7a798-129">RELATED LINKS</span></span>

[<span data-ttu-id="7a798-130">Register-AzureRmProviderFeature</span><span class="sxs-lookup"><span data-stu-id="7a798-130">Register-AzureRmProviderFeature</span></span>](./Register-AzureRmProviderFeature.md)

