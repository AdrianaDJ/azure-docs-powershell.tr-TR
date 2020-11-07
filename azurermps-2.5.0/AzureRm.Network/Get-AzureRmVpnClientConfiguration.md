---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvpnclientconfiguration
schema: 2.0.0
ms.openlocfilehash: 4d6e95534cdadd694fa2ed87d43d3f7387ec9b20
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939108"
---
# <span data-ttu-id="4cb89-101">Get-AzureRmVpnClientConfiguration</span><span class="sxs-lookup"><span data-stu-id="4cb89-101">Get-AzureRmVpnClientConfiguration</span></span>

## <span data-ttu-id="4cb89-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4cb89-102">SYNOPSIS</span></span>
<span data-ttu-id="4cb89-103">Kullanıcıların New-AzureRmVpnClientConfiguration commandme kullanılarak oluşturulan VPN profili paketini kolayca indirmesine olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="4cb89-103">Allows users to easily download the Vpn Profile package that was generated using the New-AzureRmVpnClientConfiguration commandlet.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4cb89-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4cb89-104">SYNTAX</span></span>

```
Get-AzureRmVpnClientConfiguration [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4cb89-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="4cb89-105">DESCRIPTION</span></span>
<span data-ttu-id="4cb89-106">{{Açıklamayı doldurun}}</span><span class="sxs-lookup"><span data-stu-id="4cb89-106">{{Fill in the Description}}</span></span>

## <span data-ttu-id="4cb89-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4cb89-107">EXAMPLES</span></span>

### <span data-ttu-id="4cb89-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="4cb89-108">Example 1</span></span>
```
PS C:\> New-AzureRmVpnClientConfiguration -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup" -AuthenticationMethod "EAPTLS" -RadiusRootCert "C:\Users\Test\Desktop\VpnProfileRadiusCert.cer"

PS C:\> Get-AzureRmVpnClientConfiguration -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup"
```

<span data-ttu-id="4cb89-109">Daha önce New-AzureRMVpnClientConfiguration komutu kullanılarak oluşturulan bir VpnClient profilini indirmek için URL 'YI alır.</span><span class="sxs-lookup"><span data-stu-id="4cb89-109">Gets the URL to download a VpnClient profile that has been previously generated using the New-AzureRMVpnClientConfiguration command.</span></span>

## <span data-ttu-id="4cb89-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4cb89-110">PARAMETERS</span></span>

### <span data-ttu-id="4cb89-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4cb89-111">-DefaultProfile</span></span>
<span data-ttu-id="4cb89-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4cb89-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4cb89-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="4cb89-113">-Name</span></span>
<span data-ttu-id="4cb89-114">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="4cb89-114">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4cb89-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4cb89-115">-ResourceGroupName</span></span>
<span data-ttu-id="4cb89-116">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="4cb89-116">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4cb89-117">-Onay</span><span class="sxs-lookup"><span data-stu-id="4cb89-117">-Confirm</span></span>
<span data-ttu-id="4cb89-118">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="4cb89-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4cb89-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4cb89-119">-WhatIf</span></span>
<span data-ttu-id="4cb89-120">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="4cb89-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4cb89-121">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="4cb89-121">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4cb89-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4cb89-122">CommonParameters</span></span>
<span data-ttu-id="4cb89-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4cb89-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4cb89-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4cb89-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4cb89-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4cb89-125">INPUTS</span></span>

### <span data-ttu-id="4cb89-126">System. String</span><span class="sxs-lookup"><span data-stu-id="4cb89-126">System.String</span></span>

## <span data-ttu-id="4cb89-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4cb89-127">OUTPUTS</span></span>

### <span data-ttu-id="4cb89-128">Microsoft. Azure. Commands. Network. model. PSVpnProfile</span><span class="sxs-lookup"><span data-stu-id="4cb89-128">Microsoft.Azure.Commands.Network.Models.PSVpnProfile</span></span>

## <span data-ttu-id="4cb89-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4cb89-129">NOTES</span></span>

## <span data-ttu-id="4cb89-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4cb89-130">RELATED LINKS</span></span>

