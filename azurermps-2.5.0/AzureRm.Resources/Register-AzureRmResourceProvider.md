---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: D5067FD8-2FB1-413C-9F59-84E83A74343E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/register-azurermresourceprovider
schema: 2.0.0
ms.openlocfilehash: c3459a07eb6f92e4ec30b5018efc41ff13e1c41e
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939840"
---
# <span data-ttu-id="66ad0-101">Register-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="66ad0-101">Register-AzureRmResourceProvider</span></span>

## <span data-ttu-id="66ad0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="66ad0-102">SYNOPSIS</span></span>
<span data-ttu-id="66ad0-103">Kaynak sağlayıcısını kaydeder.</span><span class="sxs-lookup"><span data-stu-id="66ad0-103">Registers a resource provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="66ad0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="66ad0-104">SYNTAX</span></span>

```
Register-AzureRmResourceProvider -ProviderNamespace <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="66ad0-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="66ad0-105">DESCRIPTION</span></span>
<span data-ttu-id="66ad0-106">**Register-AzureRmResourceProvider** cmdlet 'ı bir Azure Kaynak sağlayıcısı kaydeder.</span><span class="sxs-lookup"><span data-stu-id="66ad0-106">The **Register-AzureRmResourceProvider** cmdlet registers an Azure resource provider.</span></span>

## <span data-ttu-id="66ad0-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="66ad0-107">EXAMPLES</span></span>

### <span data-ttu-id="66ad0-108">Örnek 1: sağlayıcıyı kaydettirme</span><span class="sxs-lookup"><span data-stu-id="66ad0-108">Example 1: Register a provider</span></span>
```
PS C:\>Register-AzureRmResourceProvider -ProviderNamespace Microsoft.Network
```

<span data-ttu-id="66ad0-109">Bu, hesabınızın Microsoft. Network sağlayıcısını kaydeder.</span><span class="sxs-lookup"><span data-stu-id="66ad0-109">This registers the Microsoft.Network provider for your account.</span></span>

## <span data-ttu-id="66ad0-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="66ad0-110">PARAMETERS</span></span>

### <span data-ttu-id="66ad0-111">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="66ad0-111">-ApiVersion</span></span>
<span data-ttu-id="66ad0-112">Kaynak sağlayıcısı tarafından desteklenen API sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="66ad0-112">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="66ad0-113">Varsayılan sürümden farklı bir sürüm belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="66ad0-113">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="66ad0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66ad0-114">-DefaultProfile</span></span>
<span data-ttu-id="66ad0-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="66ad0-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="66ad0-116">-Pre-</span><span class="sxs-lookup"><span data-stu-id="66ad0-116">-Pre</span></span>
<span data-ttu-id="66ad0-117">Bu cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlediği durumlarda sürüm API sürümlerini kabul ettiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="66ad0-117">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="66ad0-118">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="66ad0-118">-ProviderNamespace</span></span>
<span data-ttu-id="66ad0-119">Kaynak sağlayıcının ad boşluğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="66ad0-119">Specifies the namespace of the resource provider.</span></span>

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

### <span data-ttu-id="66ad0-120">-Onay</span><span class="sxs-lookup"><span data-stu-id="66ad0-120">-Confirm</span></span>
<span data-ttu-id="66ad0-121">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="66ad0-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="66ad0-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="66ad0-122">-WhatIf</span></span>
<span data-ttu-id="66ad0-123">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="66ad0-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="66ad0-124">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="66ad0-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="66ad0-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66ad0-125">CommonParameters</span></span>
<span data-ttu-id="66ad0-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="66ad0-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66ad0-127">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="66ad0-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66ad0-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="66ad0-128">INPUTS</span></span>

## <span data-ttu-id="66ad0-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="66ad0-129">OUTPUTS</span></span>

## <span data-ttu-id="66ad0-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="66ad0-130">NOTES</span></span>

## <span data-ttu-id="66ad0-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="66ad0-131">RELATED LINKS</span></span>

[<span data-ttu-id="66ad0-132">Get-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="66ad0-132">Get-AzureRmResourceProvider</span></span>](./Get-AzureRmResourceProvider.md)

[<span data-ttu-id="66ad0-133">Unregister-AzureRmResourceProvider</span><span class="sxs-lookup"><span data-stu-id="66ad0-133">Unregister-AzureRmResourceProvider</span></span>](./Unregister-AzureRmResourceProvider.md)


