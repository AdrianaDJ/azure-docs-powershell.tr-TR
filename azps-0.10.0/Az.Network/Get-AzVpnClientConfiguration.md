---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvpnclientconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVpnClientConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVpnClientConfiguration.md
ms.openlocfilehash: 63b044c4a9736aca72e9713cd8ec5833e7b056ab
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935465"
---
# <span data-ttu-id="18392-101">Get-AzVpnClientConfiguration</span><span class="sxs-lookup"><span data-stu-id="18392-101">Get-AzVpnClientConfiguration</span></span>

## <span data-ttu-id="18392-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="18392-102">SYNOPSIS</span></span>
<span data-ttu-id="18392-103">Kullanıcıların New-AzVpnClientConfiguration commandme kullanılarak oluşturulan VPN profili paketini kolayca indirmesine olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="18392-103">Allows users to easily download the Vpn Profile package that was generated using the New-AzVpnClientConfiguration commandlet.</span></span>

## <span data-ttu-id="18392-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="18392-104">SYNTAX</span></span>

```
Get-AzVpnClientConfiguration [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="18392-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="18392-105">DESCRIPTION</span></span>
<span data-ttu-id="18392-106">{{Açıklamayı doldurun}}</span><span class="sxs-lookup"><span data-stu-id="18392-106">{{Fill in the Description}}</span></span>

## <span data-ttu-id="18392-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="18392-107">EXAMPLES</span></span>

### <span data-ttu-id="18392-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="18392-108">Example 1</span></span>
```
PS C:\> New-AzVpnClientConfiguration -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup" -AuthenticationMethod "EAPTLS" -RadiusRootCert "C:\Users\Test\Desktop\VpnProfileRadiusCert.cer"

PS C:\> Get-AzVpnClientConfiguration -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup"
```

<span data-ttu-id="18392-109">Daha önce New-AzVpnClientConfiguration komutu kullanılarak oluşturulan bir VpnClient profilini indirmek için URL 'YI alır.</span><span class="sxs-lookup"><span data-stu-id="18392-109">Gets the URL to download a VpnClient profile that has been previously generated using the New-AzVpnClientConfiguration command.</span></span>

## <span data-ttu-id="18392-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="18392-110">PARAMETERS</span></span>

### <span data-ttu-id="18392-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18392-111">-DefaultProfile</span></span>
<span data-ttu-id="18392-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="18392-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
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

### <span data-ttu-id="18392-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="18392-113">-Name</span></span>
<span data-ttu-id="18392-114">Kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="18392-114">The resource name.</span></span>

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

### <span data-ttu-id="18392-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="18392-115">-ResourceGroupName</span></span>
<span data-ttu-id="18392-116">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="18392-116">The resource group name.</span></span>

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

### <span data-ttu-id="18392-117">-Onay</span><span class="sxs-lookup"><span data-stu-id="18392-117">-Confirm</span></span>
<span data-ttu-id="18392-118">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="18392-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="18392-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="18392-119">-WhatIf</span></span>
<span data-ttu-id="18392-120">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="18392-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="18392-121">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="18392-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="18392-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18392-122">CommonParameters</span></span>
<span data-ttu-id="18392-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="18392-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18392-124">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="18392-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18392-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="18392-125">INPUTS</span></span>

### <span data-ttu-id="18392-126">System. String</span><span class="sxs-lookup"><span data-stu-id="18392-126">System.String</span></span>

## <span data-ttu-id="18392-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="18392-127">OUTPUTS</span></span>

### <span data-ttu-id="18392-128">Microsoft. Azure. Commands. Network. model. PSVpnProfile</span><span class="sxs-lookup"><span data-stu-id="18392-128">Microsoft.Azure.Commands.Network.Models.PSVpnProfile</span></span>

## <span data-ttu-id="18392-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="18392-129">NOTES</span></span>

## <span data-ttu-id="18392-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="18392-130">RELATED LINKS</span></span>

