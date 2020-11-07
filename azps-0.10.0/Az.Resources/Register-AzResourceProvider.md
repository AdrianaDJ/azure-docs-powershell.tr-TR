---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: D5067FD8-2FB1-413C-9F59-84E83A74343E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/register-Azresourceprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Register-AzResourceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Register-AzResourceProvider.md
ms.openlocfilehash: 7f9a5089e48da7c49716abe2bdbe710c0cf30e3b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936372"
---
# <span data-ttu-id="01484-101">Register-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="01484-101">Register-AzResourceProvider</span></span>

## <span data-ttu-id="01484-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="01484-102">SYNOPSIS</span></span>
<span data-ttu-id="01484-103">Kaynak sağlayıcısını kaydeder.</span><span class="sxs-lookup"><span data-stu-id="01484-103">Registers a resource provider.</span></span>

## <span data-ttu-id="01484-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="01484-104">SYNTAX</span></span>

```
Register-AzResourceProvider -ProviderNamespace <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="01484-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="01484-105">DESCRIPTION</span></span>
<span data-ttu-id="01484-106">**Register-AzResourceProvider** cmdlet 'ı bir Azure Kaynak sağlayıcısı kaydeder.</span><span class="sxs-lookup"><span data-stu-id="01484-106">The **Register-AzResourceProvider** cmdlet registers an Azure resource provider.</span></span>

## <span data-ttu-id="01484-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="01484-107">EXAMPLES</span></span>

### <span data-ttu-id="01484-108">Örnek 1: sağlayıcıyı kaydettirme</span><span class="sxs-lookup"><span data-stu-id="01484-108">Example 1: Register a provider</span></span>
```
PS C:\>Register-AzResourceProvider -ProviderNamespace Microsoft.Network
```

<span data-ttu-id="01484-109">Bu, hesabınızın Microsoft. Network sağlayıcısını kaydeder.</span><span class="sxs-lookup"><span data-stu-id="01484-109">This registers the Microsoft.Network provider for your account.</span></span>

## <span data-ttu-id="01484-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="01484-110">PARAMETERS</span></span>

### <span data-ttu-id="01484-111">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="01484-111">-ApiVersion</span></span>
<span data-ttu-id="01484-112">Kaynak sağlayıcısı tarafından desteklenen API sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="01484-112">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="01484-113">Varsayılan sürümden farklı bir sürüm belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="01484-113">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="01484-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01484-114">-DefaultProfile</span></span>
<span data-ttu-id="01484-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="01484-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01484-116">-Pre-</span><span class="sxs-lookup"><span data-stu-id="01484-116">-Pre</span></span>
<span data-ttu-id="01484-117">Bu cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlediği durumlarda sürüm API sürümlerini kabul ettiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="01484-117">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="01484-118">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="01484-118">-ProviderNamespace</span></span>
<span data-ttu-id="01484-119">Kaynak sağlayıcının ad boşluğunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="01484-119">Specifies the namespace of the resource provider.</span></span>

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

### <span data-ttu-id="01484-120">-Onay</span><span class="sxs-lookup"><span data-stu-id="01484-120">-Confirm</span></span>
<span data-ttu-id="01484-121">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="01484-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="01484-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="01484-122">-WhatIf</span></span>
<span data-ttu-id="01484-123">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="01484-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="01484-124">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="01484-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="01484-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01484-125">CommonParameters</span></span>
<span data-ttu-id="01484-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="01484-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01484-127">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="01484-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01484-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="01484-128">INPUTS</span></span>

## <span data-ttu-id="01484-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="01484-129">OUTPUTS</span></span>

## <span data-ttu-id="01484-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="01484-130">NOTES</span></span>

## <span data-ttu-id="01484-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="01484-131">RELATED LINKS</span></span>

[<span data-ttu-id="01484-132">Get-Azkaynaksağlayıcı</span><span class="sxs-lookup"><span data-stu-id="01484-132">Get-AzResourceProvider</span></span>](./Get-AzResourceProvider.md)

[<span data-ttu-id="01484-133">Unregister-Azkaynaksağlayıcı</span><span class="sxs-lookup"><span data-stu-id="01484-133">Unregister-AzResourceProvider</span></span>](./Unregister-AzResourceProvider.md)


