---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: D5126B7B-7FBB-4C72-B77E-13ADE2BE9B1B
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/unregister-azresourceprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Unregister-AzResourceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Unregister-AzResourceProvider.md
ms.openlocfilehash: be32315e62770de7075f89fc1390063d4c516211
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94097174"
---
# <span data-ttu-id="ce524-101">Unregister-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="ce524-101">Unregister-AzResourceProvider</span></span>

## <span data-ttu-id="ce524-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ce524-102">SYNOPSIS</span></span>
<span data-ttu-id="ce524-103">Kaynak sağlayıcının kaydını siler.</span><span class="sxs-lookup"><span data-stu-id="ce524-103">Unregisters a resource provider.</span></span>

## <span data-ttu-id="ce524-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ce524-104">SYNTAX</span></span>

```
Unregister-AzResourceProvider -ProviderNamespace <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ce524-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ce524-105">DESCRIPTION</span></span>
<span data-ttu-id="ce524-106">**Unregister-Azkaynaksağlayıcısı** cmdlet 'ı bir Azure Kaynak sağlayıcısının kaydını siler.</span><span class="sxs-lookup"><span data-stu-id="ce524-106">The **Unregister-AzResourceProvider** cmdlet unregisters an Azure resource provider.</span></span>

## <span data-ttu-id="ce524-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ce524-107">EXAMPLES</span></span>

### <span data-ttu-id="ce524-108">Örnek 1: ProviderNamespace ile kaynak sağlayıcısının kaydı siliniyor</span><span class="sxs-lookup"><span data-stu-id="ce524-108">Example 1: Unregister resource provider with ProviderNamespace</span></span>

```powershell
PS C:\>Unregister-AzResourceProvider -ProviderNamespace "Microsoft.support"
```

<span data-ttu-id="ce524-109">Bu komut, "Microsoft. support" kaynak sağlayıcısının kaydını siler.</span><span class="sxs-lookup"><span data-stu-id="ce524-109">This command unregisters the resource provider "Microsoft.support".</span></span>

## <span data-ttu-id="ce524-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ce524-110">PARAMETERS</span></span>

### <span data-ttu-id="ce524-111">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="ce524-111">-ApiVersion</span></span>
<span data-ttu-id="ce524-112">Kaynak sağlayıcısı tarafından desteklenen API sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="ce524-112">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="ce524-113">Varsayılan sürümden farklı bir sürüm belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ce524-113">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="ce524-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce524-114">-DefaultProfile</span></span>
<span data-ttu-id="ce524-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="ce524-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ce524-116">-Pre-</span><span class="sxs-lookup"><span data-stu-id="ce524-116">-Pre</span></span>
<span data-ttu-id="ce524-117">Bu cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlediği durumlarda sürüm API sürümlerini kabul ettiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="ce524-117">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="ce524-118">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="ce524-118">-ProviderNamespace</span></span>
<span data-ttu-id="ce524-119">Kaynak sağlayıcının ad boşluğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="ce524-119">Specifies the namespace of the resource provider.</span></span>

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

### <span data-ttu-id="ce524-120">-Onay</span><span class="sxs-lookup"><span data-stu-id="ce524-120">-Confirm</span></span>
<span data-ttu-id="ce524-121">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ce524-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ce524-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ce524-122">-WhatIf</span></span>
<span data-ttu-id="ce524-123">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ce524-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ce524-124">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ce524-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ce524-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce524-125">CommonParameters</span></span>
<span data-ttu-id="ce524-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ce524-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce524-127">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="ce524-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce524-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ce524-128">INPUTS</span></span>

### <span data-ttu-id="ce524-129">System. String</span><span class="sxs-lookup"><span data-stu-id="ce524-129">System.String</span></span>

## <span data-ttu-id="ce524-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ce524-130">OUTPUTS</span></span>

### <span data-ttu-id="ce524-131">Microsoft. Azure. Commands. ResourceManager. cmdlet. Sdkmodeller. PSResourceProvider</span><span class="sxs-lookup"><span data-stu-id="ce524-131">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceProvider</span></span>

## <span data-ttu-id="ce524-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ce524-132">NOTES</span></span>

## <span data-ttu-id="ce524-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ce524-133">RELATED LINKS</span></span>

[<span data-ttu-id="ce524-134">Get-Azkaynaksağlayıcı</span><span class="sxs-lookup"><span data-stu-id="ce524-134">Get-AzResourceProvider</span></span>](./Get-AzResourceProvider.md)

[<span data-ttu-id="ce524-135">Register-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="ce524-135">Register-AzResourceProvider</span></span>](./Register-AzResourceProvider.md)

