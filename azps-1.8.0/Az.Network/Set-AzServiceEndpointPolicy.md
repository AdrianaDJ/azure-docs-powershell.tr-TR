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
ms.locfileid: "93759967"
---
# <span data-ttu-id="29bac-101">Set-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="29bac-101">Set-AzServiceEndpointPolicy</span></span>

## <span data-ttu-id="29bac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="29bac-102">SYNOPSIS</span></span>
<span data-ttu-id="29bac-103">Hizmet uç noktası ilkesini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="29bac-103">Updates a service endpoint policy.</span></span>

## <span data-ttu-id="29bac-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="29bac-104">SYNTAX</span></span>

```
Set-AzServiceEndpointPolicy -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="29bac-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="29bac-105">DESCRIPTION</span></span>
<span data-ttu-id="29bac-106">**Set-AzServiceEndpointPolicy** cmdlet 'i bir hizmet uç noktası ilkesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="29bac-106">The **Set-AzServiceEndpointPolicy** cmdlet create a service endpoint policy.</span></span>

## <span data-ttu-id="29bac-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="29bac-107">EXAMPLES</span></span>

### <span data-ttu-id="29bac-108">Örnek 1: hizmet uç noktası ilkesini ayarlar</span><span class="sxs-lookup"><span data-stu-id="29bac-108">Example 1: Sets a service endpoint policy</span></span>
```
$serviceEndpointPolicy = Set-AzServiceEndpointPolicy -Name "Policy1" -ServiceEndpointPolicy $serviceEndpointPolicy -ResourceGroup "resourcegroup1"
```

<span data-ttu-id="29bac-109">Bu komut, nesne $serviceEndpointPolicy tanımlanan Policy1 adlı bir hizmet ana</span><span class="sxs-lookup"><span data-stu-id="29bac-109">This command updates a service endpoint policy named Policy1 defined by the object $serviceEndpointPolicy belong to the resourcegroup "resourcegroup1".</span></span>

## <span data-ttu-id="29bac-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="29bac-110">PARAMETERS</span></span>

### <span data-ttu-id="29bac-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29bac-111">-DefaultProfile</span></span>
<span data-ttu-id="29bac-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="29bac-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="29bac-113">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="29bac-113">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="29bac-114">ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="29bac-114">The ServiceEndpointPolicy</span></span>

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

### <span data-ttu-id="29bac-115">-Onay</span><span class="sxs-lookup"><span data-stu-id="29bac-115">-Confirm</span></span>
<span data-ttu-id="29bac-116">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="29bac-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="29bac-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="29bac-117">-WhatIf</span></span>
<span data-ttu-id="29bac-118">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="29bac-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="29bac-119">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="29bac-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="29bac-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29bac-120">CommonParameters</span></span>
<span data-ttu-id="29bac-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="29bac-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29bac-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="29bac-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29bac-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="29bac-123">INPUTS</span></span>

### <span data-ttu-id="29bac-124">Microsoft. Azure. Commands. Network. model. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="29bac-124">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="29bac-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="29bac-125">OUTPUTS</span></span>

### <span data-ttu-id="29bac-126">Microsoft. Azure. Commands. Network. model. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="29bac-126">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="29bac-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="29bac-127">NOTES</span></span>

## <span data-ttu-id="29bac-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="29bac-128">RELATED LINKS</span></span>

[<span data-ttu-id="29bac-129">Get-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="29bac-129">Get-AzServiceEndpointPolicy</span></span>](./Get-AzServiceEndpointPolicy.md)

[<span data-ttu-id="29bac-130">New-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="29bac-130">New-AzServiceEndpointPolicy</span></span>](./New-AzServiceEndpointPolicy.md)

[<span data-ttu-id="29bac-131">Remove-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="29bac-131">Remove-AzServiceEndpointPolicy</span></span>](./Remove-AzServiceEndpointPolicy.md)
