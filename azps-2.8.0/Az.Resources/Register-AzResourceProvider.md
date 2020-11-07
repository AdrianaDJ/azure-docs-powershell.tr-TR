---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: D5067FD8-2FB1-413C-9F59-84E83A74343E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/register-azresourceprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Register-AzResourceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Register-AzResourceProvider.md
ms.openlocfilehash: 11ff763dacc5a6969501dae925fbbc2382c871b3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93933328"
---
# <span data-ttu-id="be020-101">Register-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="be020-101">Register-AzResourceProvider</span></span>

## <span data-ttu-id="be020-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="be020-102">SYNOPSIS</span></span>
<span data-ttu-id="be020-103">Kaynak sağlayıcısını kaydeder.</span><span class="sxs-lookup"><span data-stu-id="be020-103">Registers a resource provider.</span></span>

## <span data-ttu-id="be020-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="be020-104">SYNTAX</span></span>

```
Register-AzResourceProvider -ProviderNamespace <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="be020-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="be020-105">DESCRIPTION</span></span>
<span data-ttu-id="be020-106">**Register-AzResourceProvider** cmdlet 'ı bir Azure Kaynak sağlayıcısı kaydeder.</span><span class="sxs-lookup"><span data-stu-id="be020-106">The **Register-AzResourceProvider** cmdlet registers an Azure resource provider.</span></span>

## <span data-ttu-id="be020-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="be020-107">EXAMPLES</span></span>

### <span data-ttu-id="be020-108">Örnek 1: sağlayıcıyı kaydettirme</span><span class="sxs-lookup"><span data-stu-id="be020-108">Example 1: Register a provider</span></span>
```
PS C:\>Register-AzResourceProvider -ProviderNamespace Microsoft.Network
```

<span data-ttu-id="be020-109">Bu, hesabınızın Microsoft. Network sağlayıcısını kaydeder.</span><span class="sxs-lookup"><span data-stu-id="be020-109">This registers the Microsoft.Network provider for your account.</span></span>

## <span data-ttu-id="be020-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="be020-110">PARAMETERS</span></span>

### <span data-ttu-id="be020-111">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="be020-111">-ApiVersion</span></span>
<span data-ttu-id="be020-112">Kaynak sağlayıcısı tarafından desteklenen API sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="be020-112">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="be020-113">Varsayılan sürümden farklı bir sürüm belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="be020-113">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="be020-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be020-114">-DefaultProfile</span></span>
<span data-ttu-id="be020-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="be020-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="be020-116">-Pre-</span><span class="sxs-lookup"><span data-stu-id="be020-116">-Pre</span></span>
<span data-ttu-id="be020-117">Bu cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlediği durumlarda sürüm API sürümlerini kabul ettiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="be020-117">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="be020-118">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="be020-118">-ProviderNamespace</span></span>
<span data-ttu-id="be020-119">Kaynak sağlayıcının ad boşluğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="be020-119">Specifies the namespace of the resource provider.</span></span>

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

### <span data-ttu-id="be020-120">-Onay</span><span class="sxs-lookup"><span data-stu-id="be020-120">-Confirm</span></span>
<span data-ttu-id="be020-121">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="be020-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="be020-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="be020-122">-WhatIf</span></span>
<span data-ttu-id="be020-123">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="be020-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="be020-124">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="be020-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="be020-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be020-125">CommonParameters</span></span>
<span data-ttu-id="be020-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="be020-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be020-127">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="be020-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be020-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="be020-128">INPUTS</span></span>

### <span data-ttu-id="be020-129">System. String</span><span class="sxs-lookup"><span data-stu-id="be020-129">System.String</span></span>

## <span data-ttu-id="be020-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="be020-130">OUTPUTS</span></span>

### <span data-ttu-id="be020-131">Microsoft. Azure. Commands. ResourceManager. cmdlet. Sdkmodeller. PSResourceProvider</span><span class="sxs-lookup"><span data-stu-id="be020-131">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceProvider</span></span>

## <span data-ttu-id="be020-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="be020-132">NOTES</span></span>

## <span data-ttu-id="be020-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="be020-133">RELATED LINKS</span></span>

[<span data-ttu-id="be020-134">Get-Azkaynaksağlayıcı</span><span class="sxs-lookup"><span data-stu-id="be020-134">Get-AzResourceProvider</span></span>](./Get-AzResourceProvider.md)

[<span data-ttu-id="be020-135">Unregister-Azkaynaksağlayıcı</span><span class="sxs-lookup"><span data-stu-id="be020-135">Unregister-AzResourceProvider</span></span>](./Unregister-AzResourceProvider.md)


