---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 6AB09621-488B-4A16-92D9-9C47EB87DA95
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResourceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResourceProvider.md
ms.openlocfilehash: a7c30ee436f35bee72e786c1d219e114236248da
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592574"
---
# <span data-ttu-id="1aec8-101">Get-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="1aec8-101">Get-AzureRmResourceProvider</span></span>

## <span data-ttu-id="1aec8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1aec8-102">SYNOPSIS</span></span>
<span data-ttu-id="1aec8-103">Kaynak sağlayıcısını alır.</span><span class="sxs-lookup"><span data-stu-id="1aec8-103">Gets a resource provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1aec8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1aec8-104">SYNTAX</span></span>

### <span data-ttu-id="1aec8-105">ListAvailable (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="1aec8-105">ListAvailable (Default)</span></span>
```
Get-AzureRmResourceProvider [-Location <String>] [-ListAvailable] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1aec8-106">Kişiselleştiralsağlayıcı</span><span class="sxs-lookup"><span data-stu-id="1aec8-106">IndividualProvider</span></span>
```
Get-AzureRmResourceProvider -ProviderNamespace <String> [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1aec8-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="1aec8-107">DESCRIPTION</span></span>
<span data-ttu-id="1aec8-108">**Get-AzureRmResourceProvider** cmdlet 'ı bir Azure Kaynak sağlayıcısı alır.</span><span class="sxs-lookup"><span data-stu-id="1aec8-108">The **Get-AzureRmResourceProvider** cmdlet gets an Azure resource provider.</span></span>

## <span data-ttu-id="1aec8-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1aec8-109">EXAMPLES</span></span>

## <span data-ttu-id="1aec8-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1aec8-110">PARAMETERS</span></span>

### <span data-ttu-id="1aec8-111">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="1aec8-111">-ApiVersion</span></span>
<span data-ttu-id="1aec8-112">Kaynak sağlayıcısı tarafından desteklenen API sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="1aec8-112">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="1aec8-113">Varsayılan sürümden farklı bir sürüm belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1aec8-113">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="1aec8-114">-ListAvailable</span><span class="sxs-lookup"><span data-stu-id="1aec8-114">-ListAvailable</span></span>
<span data-ttu-id="1aec8-115">Bu işlemin kullanılabilir tüm kaynak sağlayıcılarını aldığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="1aec8-115">Indicates that this operation gets all available resource providers.</span></span>

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

### <span data-ttu-id="1aec8-116">-Konum</span><span class="sxs-lookup"><span data-stu-id="1aec8-116">-Location</span></span>
<span data-ttu-id="1aec8-117">Kaynak sağlayıcının konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="1aec8-117">Specifies the location of the resource provider.</span></span>

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

### <span data-ttu-id="1aec8-118">-Pre-</span><span class="sxs-lookup"><span data-stu-id="1aec8-118">-Pre</span></span>
<span data-ttu-id="1aec8-119">Bu cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlediği durumlarda sürüm API sürümlerini kabul ettiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="1aec8-119">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="1aec8-120">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="1aec8-120">-ProviderNamespace</span></span>
<span data-ttu-id="1aec8-121">Kaynak sağlayıcının ad boşluğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="1aec8-121">Specifies the namespace of the resource provider.</span></span>

```yaml
Type: System.String
Parameter Sets: IndividualProvider
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1aec8-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1aec8-122">-DefaultProfile</span></span>
<span data-ttu-id="1aec8-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1aec8-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1aec8-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1aec8-124">CommonParameters</span></span>
<span data-ttu-id="1aec8-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1aec8-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1aec8-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1aec8-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1aec8-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1aec8-127">INPUTS</span></span>

## <span data-ttu-id="1aec8-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1aec8-128">OUTPUTS</span></span>

### <span data-ttu-id="1aec8-129">Microsoft. Azure. Commands. ResourceManager. cmdlet. Sdkmodeller. PSResourceProvider</span><span class="sxs-lookup"><span data-stu-id="1aec8-129">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceProvider</span></span>

## <span data-ttu-id="1aec8-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1aec8-130">NOTES</span></span>

## <span data-ttu-id="1aec8-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1aec8-131">RELATED LINKS</span></span>

[<span data-ttu-id="1aec8-132">Register-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="1aec8-132">Register-AzureRmResourceProvider</span></span>](./Register-AzureRmResourceProvider.md)

[<span data-ttu-id="1aec8-133">Unregister-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="1aec8-133">Unregister-AzureRmResourceProvider</span></span>](./Unregister-AzureRmResourceProvider.md)


