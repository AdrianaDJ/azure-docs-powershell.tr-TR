---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkinterfacetapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkInterfaceTapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkInterfaceTapConfig.md
ms.openlocfilehash: d8e9eda6c6507974376dc35e80a30669bd940153
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93760541"
---
# <span data-ttu-id="b057f-101">Get-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="b057f-101">Get-AzNetworkInterfaceTapConfig</span></span>

## <span data-ttu-id="b057f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b057f-102">SYNOPSIS</span></span>
<span data-ttu-id="b057f-103">Bir dokunuş yapılandırma kaynağını alır.</span><span class="sxs-lookup"><span data-stu-id="b057f-103">Gets a Tap configuration resource.</span></span>

## <span data-ttu-id="b057f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b057f-104">SYNTAX</span></span>

### <span data-ttu-id="b057f-105">GetByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="b057f-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzNetworkInterfaceTapConfig -ResourceGroupName <String> -NetworkInterfaceName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b057f-106">Getbyresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="b057f-106">GetByResourceIdParameterSet</span></span>
```
Get-AzNetworkInterfaceTapConfig -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b057f-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="b057f-107">DESCRIPTION</span></span>
<span data-ttu-id="b057f-108">**Get-Aznetworkınterfacetapconfig** cmdlet 'i, belirli bir kaynak grubu Için bir Azure dokunma yapılandırması alır, bir kaynak grubunda ve ağ arabiriminde, yapılandırma adına veya dokunun yapılandırmasına dokunun.</span><span class="sxs-lookup"><span data-stu-id="b057f-108">The **Get-AzNetworkInterfaceTapConfig** cmdlet gets an Azure Tap Configuration for a given resource group, network interface and tap configuration name or list of tap configurations in a resource group and network interface.</span></span>

## <span data-ttu-id="b057f-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b057f-109">EXAMPLES</span></span>

### <span data-ttu-id="b057f-110">Örnek 1: belirli bir ağ arabiriminin tüm dokunma yapılandırmalarını alma</span><span class="sxs-lookup"><span data-stu-id="b057f-110">Example 1: Get all tap configurations for a given network interface</span></span>
```
PS C:\> Get-AzNetworkInterfaceTapConfig -ResourceGroupName "ResourceGroup1" -NetworkInterface "sourceNicName"
```

<span data-ttu-id="b057f-111">Bu komut, verilen ağ arabirimine eklenecek yapılandırmalara dokunun.</span><span class="sxs-lookup"><span data-stu-id="b057f-111">This command gets tap configurations added for the given network interface.</span></span>

### <span data-ttu-id="b057f-112">Örnek 2: belirli bir dokunma yapılandırmasını alma</span><span class="sxs-lookup"><span data-stu-id="b057f-112">Example 2: Get a given tap configuration</span></span>
```
PS C:\> Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -NetworkInterface "sourceNicName" -Name "tapconfigName"
```

<span data-ttu-id="b057f-113">Bu komut, belirli bir ağ arabirimine belirli dokunuş yapılandırmasını getirir.</span><span class="sxs-lookup"><span data-stu-id="b057f-113">This command gets specific tap configuration added for the given network interface.</span></span>

### <span data-ttu-id="b057f-114">Örnek 3: belirli bir dokunma yapılandırmasını alma</span><span class="sxs-lookup"><span data-stu-id="b057f-114">Example 3: Get a given tap configuration</span></span>
```
PS C:\> Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -NetworkInterface "sourceNicName" -Name "tapconfig*"
```

<span data-ttu-id="b057f-115">Bu komut, verilen ağ arabirimine "tapconfig" ile başlayan ad ile birlikte verilen yapılandırmalara dokunun.</span><span class="sxs-lookup"><span data-stu-id="b057f-115">This command gets tap configurations added for the given network interface with name starting with "tapconfig".</span></span>

## <span data-ttu-id="b057f-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b057f-116">PARAMETERS</span></span>

### <span data-ttu-id="b057f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b057f-117">-DefaultProfile</span></span>
<span data-ttu-id="b057f-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b057f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b057f-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="b057f-119">-Name</span></span>
<span data-ttu-id="b057f-120">Belirli dokunun yapılandırması adı.</span><span class="sxs-lookup"><span data-stu-id="b057f-120">Name of the specific tap configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="b057f-121">-Networkınterfacename</span><span class="sxs-lookup"><span data-stu-id="b057f-121">-NetworkInterfaceName</span></span>
<span data-ttu-id="b057f-122">Ağ arabirim adı.</span><span class="sxs-lookup"><span data-stu-id="b057f-122">The Network Interface name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b057f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b057f-123">-ResourceGroupName</span></span>
<span data-ttu-id="b057f-124">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="b057f-124">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b057f-125">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="b057f-125">-ResourceId</span></span>
<span data-ttu-id="b057f-126">TapConfiguration kaynağının RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="b057f-126">ResourceId of the TapConfiguration resource</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b057f-127">-Onay</span><span class="sxs-lookup"><span data-stu-id="b057f-127">-Confirm</span></span>
<span data-ttu-id="b057f-128">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b057f-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b057f-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b057f-129">-WhatIf</span></span>
<span data-ttu-id="b057f-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b057f-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b057f-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b057f-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b057f-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b057f-132">CommonParameters</span></span>
<span data-ttu-id="b057f-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b057f-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b057f-134">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="b057f-134">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b057f-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b057f-135">INPUTS</span></span>

### <span data-ttu-id="b057f-136">System. String</span><span class="sxs-lookup"><span data-stu-id="b057f-136">System.String</span></span>

## <span data-ttu-id="b057f-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b057f-137">OUTPUTS</span></span>

### <span data-ttu-id="b057f-138">Microsoft. Azure. Commands. Network. model. Psnetworkınterfacetapconfiguration</span><span class="sxs-lookup"><span data-stu-id="b057f-138">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceTapConfiguration</span></span>

## <span data-ttu-id="b057f-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b057f-139">NOTES</span></span>

## <span data-ttu-id="b057f-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b057f-140">RELATED LINKS</span></span>

[<span data-ttu-id="b057f-141">Add-Aznetworkınterfacetapconfig</span><span class="sxs-lookup"><span data-stu-id="b057f-141">Add-AzNetworkInterfaceTapConfig</span></span>](./Add-AzNetworkInterfaceTapConfig.md)

[<span data-ttu-id="b057f-142">Remove-Aznetworkınterfacetapconfig</span><span class="sxs-lookup"><span data-stu-id="b057f-142">Remove-AzNetworkInterfaceTapConfig</span></span>](./Remove-AzNetworkInterfaceTapConfig.md)

[<span data-ttu-id="b057f-143">Set-Aznetworkınterfacetapconfig</span><span class="sxs-lookup"><span data-stu-id="b057f-143">Set-AzNetworkInterfaceTapConfig</span></span>](./Set-AzNetworkInterfaceTapConfig.md)