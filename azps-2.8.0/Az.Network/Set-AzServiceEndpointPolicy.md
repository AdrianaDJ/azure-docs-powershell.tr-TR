---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azserviceendpointpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzServiceEndpointPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzServiceEndpointPolicy.md
ms.openlocfilehash: 75cf6bac1913a2baa55a28135ba2d59f5ceaa07f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93932742"
---
# <span data-ttu-id="23534-101">Set-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="23534-101">Set-AzServiceEndpointPolicy</span></span>

## <span data-ttu-id="23534-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="23534-102">SYNOPSIS</span></span>
<span data-ttu-id="23534-103">Hizmet uç noktası ilkesini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="23534-103">Updates a service endpoint policy.</span></span>

## <span data-ttu-id="23534-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="23534-104">SYNTAX</span></span>

```
Set-AzServiceEndpointPolicy -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="23534-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="23534-105">DESCRIPTION</span></span>
<span data-ttu-id="23534-106">**Set-AzServiceEndpointPolicy** cmdlet 'i bir hizmet uç noktası ilkesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="23534-106">The **Set-AzServiceEndpointPolicy** cmdlet create a service endpoint policy.</span></span>

## <span data-ttu-id="23534-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="23534-107">EXAMPLES</span></span>

### <span data-ttu-id="23534-108">Örnek 1: hizmet uç noktası ilkesini ayarlar</span><span class="sxs-lookup"><span data-stu-id="23534-108">Example 1: Sets a service endpoint policy</span></span>
```
$serviceEndpointPolicy = Set-AzServiceEndpointPolicy -Name "Policy1" -ServiceEndpointPolicy $serviceEndpointPolicy -ResourceGroup "resourcegroup1"
```

<span data-ttu-id="23534-109">Bu komut, nesne $serviceEndpointPolicy tanımlanan Policy1 adlı bir hizmet ana</span><span class="sxs-lookup"><span data-stu-id="23534-109">This command updates a service endpoint policy named Policy1 defined by the object $serviceEndpointPolicy belong to the resourcegroup "resourcegroup1".</span></span>

## <span data-ttu-id="23534-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="23534-110">PARAMETERS</span></span>

### <span data-ttu-id="23534-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23534-111">-DefaultProfile</span></span>
<span data-ttu-id="23534-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="23534-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="23534-113">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="23534-113">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="23534-114">ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="23534-114">The ServiceEndpointPolicy</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="23534-115">-Onay</span><span class="sxs-lookup"><span data-stu-id="23534-115">-Confirm</span></span>
<span data-ttu-id="23534-116">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="23534-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23534-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="23534-117">-WhatIf</span></span>
<span data-ttu-id="23534-118">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="23534-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="23534-119">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="23534-119">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23534-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23534-120">CommonParameters</span></span>
<span data-ttu-id="23534-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="23534-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23534-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="23534-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23534-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="23534-123">INPUTS</span></span>

### <span data-ttu-id="23534-124">Microsoft. Azure. Commands. Network. model. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="23534-124">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="23534-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="23534-125">OUTPUTS</span></span>

### <span data-ttu-id="23534-126">Microsoft. Azure. Commands. Network. model. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="23534-126">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="23534-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="23534-127">NOTES</span></span>

## <span data-ttu-id="23534-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="23534-128">RELATED LINKS</span></span>

[<span data-ttu-id="23534-129">Get-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="23534-129">Get-AzServiceEndpointPolicy</span></span>](./Get-AzServiceEndpointPolicy.md)

[<span data-ttu-id="23534-130">New-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="23534-130">New-AzServiceEndpointPolicy</span></span>](./New-AzServiceEndpointPolicy.md)

[<span data-ttu-id="23534-131">Remove-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="23534-131">Remove-AzServiceEndpointPolicy</span></span>](./Remove-AzServiceEndpointPolicy.md)
