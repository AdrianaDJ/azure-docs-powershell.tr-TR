---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 67AD15B0-94EB-486F-8C17-606EA5F702D3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermloadbalancerbackendaddresspoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancerBackendAddressPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancerBackendAddressPoolConfig.md
ms.openlocfilehash: 2819da4d49a116f451b3842c5e0eab1702d8c4ca
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590156"
---
# <span data-ttu-id="8e452-101">New-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="8e452-101">New-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>

## <span data-ttu-id="8e452-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8e452-102">SYNOPSIS</span></span>
<span data-ttu-id="8e452-103">Bir yük dengeleyici için arka uç adres havuzu yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8e452-103">Creates a backend address pool configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8e452-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8e452-104">SYNTAX</span></span>

```
New-AzureRmLoadBalancerBackendAddressPoolConfig -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8e452-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="8e452-105">DESCRIPTION</span></span>
<span data-ttu-id="8e452-106">**Yeni-AzureRmLoadBalancerBackendAddressPoolConfig** cmdlet 'i Azure Yük Dengeleyici için bir arka uç adres havuzu yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8e452-106">The **New-AzureRmLoadBalancerBackendAddressPoolConfig** cmdlet creates a backend address pool configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="8e452-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8e452-107">EXAMPLES</span></span>

### <span data-ttu-id="8e452-108">Örnek 1: yük dengeleyici için arka uç adres havuzu yapılandırması oluşturma</span><span class="sxs-lookup"><span data-stu-id="8e452-108">Example 1: Create a backend address pool configuration for a load balancer</span></span>
```
PS C:\>New-AzureRmLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool02"
```

<span data-ttu-id="8e452-109">Bu komut, BackendAddressPool02 adlı bir arka uç adres havuzu yapılandırması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8e452-109">This command creates a backend address pool configuration named BackendAddressPool02 for a load balancer.</span></span>

## <span data-ttu-id="8e452-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8e452-110">PARAMETERS</span></span>

### <span data-ttu-id="8e452-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e452-111">-DefaultProfile</span></span>
<span data-ttu-id="8e452-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8e452-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8e452-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="8e452-113">-Name</span></span>
<span data-ttu-id="8e452-114">Oluşturulacak adres havuzu yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="8e452-114">Specifies the name of the address pool configuration to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e452-115">-Onay</span><span class="sxs-lookup"><span data-stu-id="8e452-115">-Confirm</span></span>
<span data-ttu-id="8e452-116">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="8e452-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8e452-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8e452-117">-WhatIf</span></span>
<span data-ttu-id="8e452-118">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="8e452-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8e452-119">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="8e452-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8e452-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e452-120">CommonParameters</span></span>
<span data-ttu-id="8e452-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8e452-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e452-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8e452-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e452-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8e452-123">INPUTS</span></span>

### <span data-ttu-id="8e452-124">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="8e452-124">None</span></span>

## <span data-ttu-id="8e452-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8e452-125">OUTPUTS</span></span>

### <span data-ttu-id="8e452-126">Microsoft. Azure. Commands. Network. model. PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="8e452-126">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="8e452-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8e452-127">NOTES</span></span>

## <span data-ttu-id="8e452-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8e452-128">RELATED LINKS</span></span>

[<span data-ttu-id="8e452-129">Add-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="8e452-129">Add-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./Add-AzureRmLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="8e452-130">Get-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="8e452-130">Get-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./Get-AzureRmLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="8e452-131">Remove-AzureRmLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="8e452-131">Remove-AzureRmLoadBalancerBackendAddressPoolConfig</span></span>](./Remove-AzureRmLoadBalancerBackendAddressPoolConfig.md)


