---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 6AB09621-488B-4A16-92D9-9C47EB87DA95
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azresourceprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceProvider.md
ms.openlocfilehash: 76a0164a5cf4c4d67ecb7f64667b9b87d9bc252c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93759413"
---
# <span data-ttu-id="a4bad-101">Get-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="a4bad-101">Get-AzResourceProvider</span></span>

## <span data-ttu-id="a4bad-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a4bad-102">SYNOPSIS</span></span>
<span data-ttu-id="a4bad-103">Kaynak sağlayıcısını alır.</span><span class="sxs-lookup"><span data-stu-id="a4bad-103">Gets a resource provider.</span></span>

## <span data-ttu-id="a4bad-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a4bad-104">SYNTAX</span></span>

### <span data-ttu-id="a4bad-105">ListAvailable (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="a4bad-105">ListAvailable (Default)</span></span>
```
Get-AzResourceProvider [-Location <String>] [-ListAvailable] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a4bad-106">Kişiselleştiralsağlayıcı</span><span class="sxs-lookup"><span data-stu-id="a4bad-106">IndividualProvider</span></span>
```
Get-AzResourceProvider -ProviderNamespace <String[]> [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a4bad-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="a4bad-107">DESCRIPTION</span></span>
<span data-ttu-id="a4bad-108">**Get-AzResourceProvider** cmdlet 'ı bir Azure Kaynak sağlayıcısı alır.</span><span class="sxs-lookup"><span data-stu-id="a4bad-108">The **Get-AzResourceProvider** cmdlet gets an Azure resource provider.</span></span>

## <span data-ttu-id="a4bad-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a4bad-109">EXAMPLES</span></span>

## <span data-ttu-id="a4bad-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a4bad-110">PARAMETERS</span></span>

### <span data-ttu-id="a4bad-111">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="a4bad-111">-ApiVersion</span></span>
<span data-ttu-id="a4bad-112">Kaynak sağlayıcısı tarafından desteklenen API sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="a4bad-112">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="a4bad-113">Varsayılan sürümden farklı bir sürüm belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a4bad-113">You can specify a different version than the default version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4bad-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4bad-114">-DefaultProfile</span></span>
<span data-ttu-id="a4bad-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="a4bad-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a4bad-116">-ListAvailable</span><span class="sxs-lookup"><span data-stu-id="a4bad-116">-ListAvailable</span></span>
<span data-ttu-id="a4bad-117">Bu işlemin kullanılabilir tüm kaynak sağlayıcılarını aldığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a4bad-117">Indicates that this operation gets all available resource providers.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ListAvailable
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4bad-118">-Konum</span><span class="sxs-lookup"><span data-stu-id="a4bad-118">-Location</span></span>
<span data-ttu-id="a4bad-119">Kaynak sağlayıcının konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="a4bad-119">Specifies the location of the resource provider.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4bad-120">-Pre-</span><span class="sxs-lookup"><span data-stu-id="a4bad-120">-Pre</span></span>
<span data-ttu-id="a4bad-121">Bu cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlediği durumlarda sürüm API sürümlerini kabul ettiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="a4bad-121">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4bad-122">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="a4bad-122">-ProviderNamespace</span></span>
<span data-ttu-id="a4bad-123">Kaynak sağlayıcının ad boşluğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="a4bad-123">Specifies the namespace of the resource provider.</span></span>

```yaml
Type: System.String[]
Parameter Sets: IndividualProvider
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4bad-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4bad-124">CommonParameters</span></span>
<span data-ttu-id="a4bad-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a4bad-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4bad-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a4bad-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4bad-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a4bad-127">INPUTS</span></span>

### <span data-ttu-id="a4bad-128">System. String []</span><span class="sxs-lookup"><span data-stu-id="a4bad-128">System.String[]</span></span>

## <span data-ttu-id="a4bad-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a4bad-129">OUTPUTS</span></span>

### <span data-ttu-id="a4bad-130">Microsoft. Azure. Commands. ResourceManager. cmdlet. Sdkmodeller. PSResourceProvider</span><span class="sxs-lookup"><span data-stu-id="a4bad-130">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceProvider</span></span>

## <span data-ttu-id="a4bad-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a4bad-131">NOTES</span></span>

## <span data-ttu-id="a4bad-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a4bad-132">RELATED LINKS</span></span>

[<span data-ttu-id="a4bad-133">Register-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="a4bad-133">Register-AzResourceProvider</span></span>](./Register-AzResourceProvider.md)

[<span data-ttu-id="a4bad-134">Unregister-Azkaynaksağlayıcı</span><span class="sxs-lookup"><span data-stu-id="a4bad-134">Unregister-AzResourceProvider</span></span>](./Unregister-AzResourceProvider.md)

