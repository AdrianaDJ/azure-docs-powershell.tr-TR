---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvpnclientconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientConfiguration.md
ms.openlocfilehash: c91b42620d98cae3ecc5dcbd1f8a769c96675ade
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93760452"
---
# <span data-ttu-id="23eb0-101">Get-AzVpnClientConfiguration</span><span class="sxs-lookup"><span data-stu-id="23eb0-101">Get-AzVpnClientConfiguration</span></span>

## <span data-ttu-id="23eb0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="23eb0-102">SYNOPSIS</span></span>
<span data-ttu-id="23eb0-103">Kullanıcıların New-AzVpnClientConfiguration commandme kullanılarak oluşturulan VPN profili paketini kolayca indirmesine olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="23eb0-103">Allows users to easily download the Vpn Profile package that was generated using the New-AzVpnClientConfiguration commandlet.</span></span>

## <span data-ttu-id="23eb0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="23eb0-104">SYNTAX</span></span>

```
Get-AzVpnClientConfiguration [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="23eb0-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="23eb0-105">DESCRIPTION</span></span>
<span data-ttu-id="23eb0-106">Get-AzVpnClientConfiguration, VPN istemcisinin indirileceği URL 'YI döndürür.</span><span class="sxs-lookup"><span data-stu-id="23eb0-106">The Get-AzVpnClientConfiguration returns the URL where the VPN client can be downloaded from.</span></span>

## <span data-ttu-id="23eb0-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="23eb0-107">EXAMPLES</span></span>

### <span data-ttu-id="23eb0-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="23eb0-108">Example 1</span></span>
```
PS C:\> New-AzVpnClientConfiguration -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup" -AuthenticationMethod "EAPTLS" -RadiusRootCert "C:\Users\Test\Desktop\VpnProfileRadiusCert.cer"

PS C:\> Get-AzVpnClientConfiguration -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup"
```

<span data-ttu-id="23eb0-109">Daha önce New-AzVpnClientConfiguration komutu kullanılarak oluşturulan bir VpnClient profilini indirmek için URL 'YI alır.</span><span class="sxs-lookup"><span data-stu-id="23eb0-109">Gets the URL to download a VpnClient profile that has been previously generated using the New-AzVpnClientConfiguration command.</span></span>

## <span data-ttu-id="23eb0-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="23eb0-110">PARAMETERS</span></span>

### <span data-ttu-id="23eb0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23eb0-111">-DefaultProfile</span></span>
<span data-ttu-id="23eb0-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="23eb0-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="23eb0-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="23eb0-113">-Name</span></span>
<span data-ttu-id="23eb0-114">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="23eb0-114">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23eb0-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23eb0-115">-ResourceGroupName</span></span>
<span data-ttu-id="23eb0-116">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="23eb0-116">The resource group name.</span></span>

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

### <span data-ttu-id="23eb0-117">-Onay</span><span class="sxs-lookup"><span data-stu-id="23eb0-117">-Confirm</span></span>
<span data-ttu-id="23eb0-118">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="23eb0-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="23eb0-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="23eb0-119">-WhatIf</span></span>
<span data-ttu-id="23eb0-120">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="23eb0-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="23eb0-121">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="23eb0-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="23eb0-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23eb0-122">CommonParameters</span></span>
<span data-ttu-id="23eb0-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="23eb0-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23eb0-124">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="23eb0-124">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23eb0-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="23eb0-125">INPUTS</span></span>

### <span data-ttu-id="23eb0-126">System. String</span><span class="sxs-lookup"><span data-stu-id="23eb0-126">System.String</span></span>

## <span data-ttu-id="23eb0-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="23eb0-127">OUTPUTS</span></span>

### <span data-ttu-id="23eb0-128">Microsoft. Azure. Commands. Network. model. PSVpnProfile</span><span class="sxs-lookup"><span data-stu-id="23eb0-128">Microsoft.Azure.Commands.Network.Models.PSVpnProfile</span></span>

## <span data-ttu-id="23eb0-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="23eb0-129">NOTES</span></span>

## <span data-ttu-id="23eb0-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="23eb0-130">RELATED LINKS</span></span>

[<span data-ttu-id="23eb0-131">Yeni-AzVpnClientConfiguration</span><span class="sxs-lookup"><span data-stu-id="23eb0-131">New-AzVpnClientConfiguration</span></span>](./New-AzVpnClientConfiguration.md)