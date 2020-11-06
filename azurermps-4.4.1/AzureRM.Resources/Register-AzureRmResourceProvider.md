---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: D5067FD8-2FB1-413C-9F59-84E83A74343E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Register-AzureRmResourceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Register-AzureRmResourceProvider.md
ms.openlocfilehash: 92d94950bc4bc90494482b22b81cbd918c8b6938
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592561"
---
# <span data-ttu-id="ad377-101">Register-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="ad377-101">Register-AzureRmResourceProvider</span></span>

## <span data-ttu-id="ad377-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ad377-102">SYNOPSIS</span></span>
<span data-ttu-id="ad377-103">Kaynak sağlayıcısını kaydeder.</span><span class="sxs-lookup"><span data-stu-id="ad377-103">Registers a resource provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ad377-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ad377-104">SYNTAX</span></span>

```
Register-AzureRmResourceProvider -ProviderNamespace <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ad377-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ad377-105">DESCRIPTION</span></span>
<span data-ttu-id="ad377-106">**Register-AzureRmResourceProvider** cmdlet 'ı bir Azure Kaynak sağlayıcısı kaydeder.</span><span class="sxs-lookup"><span data-stu-id="ad377-106">The **Register-AzureRmResourceProvider** cmdlet registers an Azure resource provider.</span></span>

## <span data-ttu-id="ad377-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ad377-107">EXAMPLES</span></span>

## <span data-ttu-id="ad377-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ad377-108">PARAMETERS</span></span>

### <span data-ttu-id="ad377-109">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="ad377-109">-ApiVersion</span></span>
<span data-ttu-id="ad377-110">Kaynak sağlayıcısı tarafından desteklenen API sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="ad377-110">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="ad377-111">Varsayılan sürümden farklı bir sürüm belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ad377-111">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="ad377-112">-Pre-</span><span class="sxs-lookup"><span data-stu-id="ad377-112">-Pre</span></span>
<span data-ttu-id="ad377-113">Bu cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlediği durumlarda sürüm API sürümlerini kabul ettiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="ad377-113">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="ad377-114">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="ad377-114">-ProviderNamespace</span></span>
<span data-ttu-id="ad377-115">Kaynak sağlayıcının ad boşluğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="ad377-115">Specifies the namespace of the resource provider.</span></span>

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

### <span data-ttu-id="ad377-116">-Onay</span><span class="sxs-lookup"><span data-stu-id="ad377-116">-Confirm</span></span>
<span data-ttu-id="ad377-117">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ad377-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ad377-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad377-118">-WhatIf</span></span>
<span data-ttu-id="ad377-119">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ad377-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ad377-120">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ad377-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ad377-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad377-121">-DefaultProfile</span></span>
<span data-ttu-id="ad377-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ad377-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ad377-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad377-123">CommonParameters</span></span>
<span data-ttu-id="ad377-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ad377-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad377-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad377-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad377-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ad377-126">INPUTS</span></span>

## <span data-ttu-id="ad377-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ad377-127">OUTPUTS</span></span>

### <span data-ttu-id="ad377-128">Microsoft. Azure. Commands. ResourceManager. cmdlet. Sdkmodeller. PSResourceProvider</span><span class="sxs-lookup"><span data-stu-id="ad377-128">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceProvider</span></span>

## <span data-ttu-id="ad377-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ad377-129">NOTES</span></span>

## <span data-ttu-id="ad377-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ad377-130">RELATED LINKS</span></span>

[<span data-ttu-id="ad377-131">Get-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="ad377-131">Get-AzureRmResourceProvider</span></span>](./Get-AzureRmResourceProvider.md)

[<span data-ttu-id="ad377-132">Unregister-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="ad377-132">Unregister-AzureRmResourceProvider</span></span>](./Unregister-AzureRmResourceProvider.md)


