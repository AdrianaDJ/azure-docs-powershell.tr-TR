---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 2970E81E-A788-4829-B1FF-B522A91DE4B1
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmProviderFeature.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmProviderFeature.md
ms.openlocfilehash: 5e4802aff3c887a76cc376cac001ac20d9a98eea
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592587"
---
# <span data-ttu-id="c163f-101">Get-AzureRmProviderFeature</span><span class="sxs-lookup"><span data-stu-id="c163f-101">Get-AzureRmProviderFeature</span></span>

## <span data-ttu-id="c163f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c163f-102">SYNOPSIS</span></span>
<span data-ttu-id="c163f-103">Azure sağlayıcı özellikleri hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="c163f-103">Gets information about Azure provider features.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c163f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c163f-104">SYNTAX</span></span>

### <span data-ttu-id="c163f-105">ListAvailableParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="c163f-105">ListAvailableParameterSet (Default)</span></span>
```
Get-AzureRmProviderFeature [-ProviderNamespace <String>] [-ListAvailable]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c163f-106">GetFeature</span><span class="sxs-lookup"><span data-stu-id="c163f-106">GetFeature</span></span>
```
Get-AzureRmProviderFeature -ProviderNamespace <String> -FeatureName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c163f-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="c163f-107">DESCRIPTION</span></span>
<span data-ttu-id="c163f-108">**Get-AzureRmProviderFeature** cmdlet 'i Azure sağlayıcı özelliklerinin özellik adını, sağlayıcı adını ve kayıt durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="c163f-108">The **Get-AzureRmProviderFeature** cmdlet gets the feature name, provider name, and registration status for Azure provider features.</span></span>

## <span data-ttu-id="c163f-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c163f-109">EXAMPLES</span></span>

### <span data-ttu-id="c163f-110">Örnek 1: kullanılabilir tüm özellikleri alma</span><span class="sxs-lookup"><span data-stu-id="c163f-110">Example 1: Get all available features</span></span>
```
PS C:\>Get-AzureRmProviderFeature -ListAvailable
```

<span data-ttu-id="c163f-111">Bu komut kullanılabilir tüm özellikleri alır.</span><span class="sxs-lookup"><span data-stu-id="c163f-111">This command gets all available features.</span></span>

### <span data-ttu-id="c163f-112">Örnek 2: belirli bir özellikle ilgili bilgileri alma</span><span class="sxs-lookup"><span data-stu-id="c163f-112">Example 2: Get information about a specific feature</span></span>
```
PS C:\>Get-AzureRmProviderFeature -FeatureName "AllowPreReleaseRegions" -ProviderNamespace "Microsoft.Compute"
```

<span data-ttu-id="c163f-113">Bu komut, belirtilen sağlayıcı için AllowPreReleaseRegions adlı özelliğin bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="c163f-113">This command gets information for the feature named AllowPreReleaseRegions for the specified provider.</span></span>

## <span data-ttu-id="c163f-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c163f-114">PARAMETERS</span></span>

### <span data-ttu-id="c163f-115">-FeatureName</span><span class="sxs-lookup"><span data-stu-id="c163f-115">-FeatureName</span></span>
<span data-ttu-id="c163f-116">Alınacak özelliğin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c163f-116">Specifies the name of the feature to get.</span></span>

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

### <span data-ttu-id="c163f-117">-ListAvailable</span><span class="sxs-lookup"><span data-stu-id="c163f-117">-ListAvailable</span></span>
<span data-ttu-id="c163f-118">Bu cmdlet 'in tüm özellikleri aldığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c163f-118">Indicates that this cmdlet gets all features.</span></span>

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

### <span data-ttu-id="c163f-119">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="c163f-119">-ProviderNamespace</span></span>
<span data-ttu-id="c163f-120">Bu cmdlet 'in sağlayıcı özelliklerini aldığı ad boşluğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="c163f-120">Specifies the namespace for which this cmdlet gets provider features.</span></span>

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

### <span data-ttu-id="c163f-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c163f-121">-DefaultProfile</span></span>
<span data-ttu-id="c163f-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c163f-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c163f-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c163f-123">CommonParameters</span></span>
<span data-ttu-id="c163f-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c163f-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c163f-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c163f-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c163f-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c163f-126">INPUTS</span></span>

## <span data-ttu-id="c163f-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c163f-127">OUTPUTS</span></span>

### <span data-ttu-id="c163f-128">System. Koleksiyonlar. Generic. LIST ' 1 [Microsoft. Azure. Commands. ResourceManager. cmdlet. Sdkmodeller. PSProviderFeature]</span><span class="sxs-lookup"><span data-stu-id="c163f-128">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSProviderFeature]</span></span>

## <span data-ttu-id="c163f-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c163f-129">NOTES</span></span>

## <span data-ttu-id="c163f-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c163f-130">RELATED LINKS</span></span>

[<span data-ttu-id="c163f-131">Register-AzureRmProviderFeature</span><span class="sxs-lookup"><span data-stu-id="c163f-131">Register-AzureRmProviderFeature</span></span>](./Register-AzureRmProviderFeature.md)


