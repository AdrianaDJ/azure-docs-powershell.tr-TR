---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 6AB09621-488B-4A16-92D9-9C47EB87DA95
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermresourceprovider
schema: 2.0.0
ms.openlocfilehash: ca4f9431a7b382166b99a33be5b9373871b610e8
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93938912"
---
# <span data-ttu-id="166ce-101">Get-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="166ce-101">Get-AzureRmResourceProvider</span></span>

## <span data-ttu-id="166ce-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="166ce-102">SYNOPSIS</span></span>
<span data-ttu-id="166ce-103">Kaynak sağlayıcısını alır.</span><span class="sxs-lookup"><span data-stu-id="166ce-103">Gets a resource provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="166ce-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="166ce-104">SYNTAX</span></span>

### <span data-ttu-id="166ce-105">ListAvailable (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="166ce-105">ListAvailable (Default)</span></span>
```
Get-AzureRmResourceProvider [-Location <String>] [-ListAvailable] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="166ce-106">Kişiselleştiralsağlayıcı</span><span class="sxs-lookup"><span data-stu-id="166ce-106">IndividualProvider</span></span>
```
Get-AzureRmResourceProvider -ProviderNamespace <String[]> [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="166ce-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="166ce-107">DESCRIPTION</span></span>
<span data-ttu-id="166ce-108">**Get-AzureRmResourceProvider** cmdlet 'ı bir Azure Kaynak sağlayıcısı alır.</span><span class="sxs-lookup"><span data-stu-id="166ce-108">The **Get-AzureRmResourceProvider** cmdlet gets an Azure resource provider.</span></span>

## <span data-ttu-id="166ce-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="166ce-109">EXAMPLES</span></span>

## <span data-ttu-id="166ce-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="166ce-110">PARAMETERS</span></span>

### <span data-ttu-id="166ce-111">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="166ce-111">-ApiVersion</span></span>
<span data-ttu-id="166ce-112">Kaynak sağlayıcısı tarafından desteklenen API sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="166ce-112">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="166ce-113">Varsayılan sürümden farklı bir sürüm belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="166ce-113">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="166ce-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="166ce-114">-DefaultProfile</span></span>
<span data-ttu-id="166ce-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="166ce-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="166ce-116">-ListAvailable</span><span class="sxs-lookup"><span data-stu-id="166ce-116">-ListAvailable</span></span>
<span data-ttu-id="166ce-117">Bu işlemin kullanılabilir tüm kaynak sağlayıcılarını aldığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="166ce-117">Indicates that this operation gets all available resource providers.</span></span>

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

### <span data-ttu-id="166ce-118">-Konum</span><span class="sxs-lookup"><span data-stu-id="166ce-118">-Location</span></span>
<span data-ttu-id="166ce-119">Kaynak sağlayıcının konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="166ce-119">Specifies the location of the resource provider.</span></span>

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

### <span data-ttu-id="166ce-120">-Pre-</span><span class="sxs-lookup"><span data-stu-id="166ce-120">-Pre</span></span>
<span data-ttu-id="166ce-121">Bu cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlediği durumlarda sürüm API sürümlerini kabul ettiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="166ce-121">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="166ce-122">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="166ce-122">-ProviderNamespace</span></span>
<span data-ttu-id="166ce-123">Kaynak sağlayıcının ad boşluğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="166ce-123">Specifies the namespace of the resource provider.</span></span>

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

### <span data-ttu-id="166ce-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="166ce-124">CommonParameters</span></span>
<span data-ttu-id="166ce-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="166ce-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="166ce-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="166ce-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="166ce-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="166ce-127">INPUTS</span></span>

## <span data-ttu-id="166ce-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="166ce-128">OUTPUTS</span></span>

## <span data-ttu-id="166ce-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="166ce-129">NOTES</span></span>

## <span data-ttu-id="166ce-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="166ce-130">RELATED LINKS</span></span>

[<span data-ttu-id="166ce-131">Register-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="166ce-131">Register-AzureRmResourceProvider</span></span>](./Register-AzureRmResourceProvider.md)

[<span data-ttu-id="166ce-132">Unregister-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="166ce-132">Unregister-AzureRmResourceProvider</span></span>](./Unregister-AzureRmResourceProvider.md)

