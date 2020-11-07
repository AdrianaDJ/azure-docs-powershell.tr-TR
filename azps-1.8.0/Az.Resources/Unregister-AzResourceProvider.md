---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: D5126B7B-7FBB-4C72-B77E-13ADE2BE9B1B
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/unregister-azresourceprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Unregister-AzResourceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Unregister-AzResourceProvider.md
ms.openlocfilehash: de2a213122f756d87255be6195759e467f64b428
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93759294"
---
# <span data-ttu-id="7b481-101">Unregister-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="7b481-101">Unregister-AzResourceProvider</span></span>

## <span data-ttu-id="7b481-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7b481-102">SYNOPSIS</span></span>
<span data-ttu-id="7b481-103">Kaynak sağlayıcının kaydını siler.</span><span class="sxs-lookup"><span data-stu-id="7b481-103">Unregisters a resource provider.</span></span>

## <span data-ttu-id="7b481-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7b481-104">SYNTAX</span></span>

```
Unregister-AzResourceProvider -ProviderNamespace <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7b481-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="7b481-105">DESCRIPTION</span></span>
<span data-ttu-id="7b481-106">**Unregister-Azkaynaksağlayıcısı** cmdlet 'ı bir Azure Kaynak sağlayıcısının kaydını siler.</span><span class="sxs-lookup"><span data-stu-id="7b481-106">The **Unregister-AzResourceProvider** cmdlet unregisters an Azure resource provider.</span></span>

## <span data-ttu-id="7b481-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7b481-107">EXAMPLES</span></span>

## <span data-ttu-id="7b481-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7b481-108">PARAMETERS</span></span>

### <span data-ttu-id="7b481-109">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="7b481-109">-ApiVersion</span></span>
<span data-ttu-id="7b481-110">Kaynak sağlayıcısı tarafından desteklenen API sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="7b481-110">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="7b481-111">Varsayılan sürümden farklı bir sürüm belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="7b481-111">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="7b481-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b481-112">-DefaultProfile</span></span>
<span data-ttu-id="7b481-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="7b481-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7b481-114">-Pre-</span><span class="sxs-lookup"><span data-stu-id="7b481-114">-Pre</span></span>
<span data-ttu-id="7b481-115">Bu cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlediği durumlarda sürüm API sürümlerini kabul ettiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="7b481-115">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="7b481-116">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="7b481-116">-ProviderNamespace</span></span>
<span data-ttu-id="7b481-117">Kaynak sağlayıcının ad boşluğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="7b481-117">Specifies the namespace of the resource provider.</span></span>

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

### <span data-ttu-id="7b481-118">-Onay</span><span class="sxs-lookup"><span data-stu-id="7b481-118">-Confirm</span></span>
<span data-ttu-id="7b481-119">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="7b481-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7b481-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7b481-120">-WhatIf</span></span>
<span data-ttu-id="7b481-121">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7b481-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7b481-122">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="7b481-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7b481-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b481-123">CommonParameters</span></span>
<span data-ttu-id="7b481-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7b481-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b481-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7b481-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b481-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7b481-126">INPUTS</span></span>

### <span data-ttu-id="7b481-127">System. String</span><span class="sxs-lookup"><span data-stu-id="7b481-127">System.String</span></span>

## <span data-ttu-id="7b481-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7b481-128">OUTPUTS</span></span>

### <span data-ttu-id="7b481-129">Microsoft. Azure. Commands. ResourceManager. cmdlet. Sdkmodeller. PSResourceProvider</span><span class="sxs-lookup"><span data-stu-id="7b481-129">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceProvider</span></span>

## <span data-ttu-id="7b481-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7b481-130">NOTES</span></span>

## <span data-ttu-id="7b481-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7b481-131">RELATED LINKS</span></span>

[<span data-ttu-id="7b481-132">Get-Azkaynaksağlayıcı</span><span class="sxs-lookup"><span data-stu-id="7b481-132">Get-AzResourceProvider</span></span>](./Get-AzResourceProvider.md)

[<span data-ttu-id="7b481-133">Register-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="7b481-133">Register-AzResourceProvider</span></span>](./Register-AzResourceProvider.md)

