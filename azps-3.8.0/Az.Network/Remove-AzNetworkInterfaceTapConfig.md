---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/Remove-aznetworkinterfacetapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkInterfaceTapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkInterfaceTapConfig.md
ms.openlocfilehash: 52fc2a3c84c70d52c173bc256ca2b0d952307e91
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94104014"
---
# <span data-ttu-id="23a31-101">Remove-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="23a31-101">Remove-AzNetworkInterfaceTapConfig</span></span>

## <span data-ttu-id="23a31-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="23a31-102">SYNOPSIS</span></span>
<span data-ttu-id="23a31-103">Verilen ağ arabiriminden bir dokunma yapılandırmasını kaldırır</span><span class="sxs-lookup"><span data-stu-id="23a31-103">Removes a tap configuration from given network interface</span></span>

## <span data-ttu-id="23a31-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="23a31-104">SYNTAX</span></span>

### <span data-ttu-id="23a31-105">RemoveByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="23a31-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzNetworkInterfaceTapConfig -ResourceGroupName <String> -NetworkInterfaceName <String> -Name <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="23a31-106">Deletebyresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="23a31-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzNetworkInterfaceTapConfig -ResourceId <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="23a31-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="23a31-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzNetworkInterfaceTapConfig -InputObject <PSNetworkInterfaceTapConfiguration> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="23a31-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="23a31-108">DESCRIPTION</span></span>
<span data-ttu-id="23a31-109">**Remove-Aznetworkınterfacetapconfig** cmdlet 'i, bir Azure dokunma yapılandırmasını ağ arabirim listesinden kaldırır.</span><span class="sxs-lookup"><span data-stu-id="23a31-109">The **Remove-AzNetworkInterfaceTapConfig** cmdlet removes an Azure tap configuration from a network interface list.</span></span>

## <span data-ttu-id="23a31-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="23a31-110">EXAMPLES</span></span>

### <span data-ttu-id="23a31-111">Örnek 1: bir dokunma yapılandırmasını kaldırma</span><span class="sxs-lookup"><span data-stu-id="23a31-111">Example 1: Remove a tap configuration</span></span>
```
PS C:\>Remove-AzNetworkInterfaceTapConfig -Name "TapConfiguration" -NetworkInterfaceName "NetworkInterface1" -ResourceGroup "ResourceGroup1"
```

<span data-ttu-id="23a31-112">Bu komut, kaynak grubundaki NetworkInterface1 'den TapConfiguration 'ı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="23a31-112">This command removes the TapConfiguration from NetworkInterface1 in a resource group ResourceGroup1.</span></span>
<span data-ttu-id="23a31-113">*Force* parametresi kullanılmadığından, kullanıcıdan bu eylemi onaylaması istenir.</span><span class="sxs-lookup"><span data-stu-id="23a31-113">Because the *Force* parameter is not used, the user will be prompted to confirm this action.</span></span>

### <span data-ttu-id="23a31-114">Örnek 2: ağ arabirimini kaldırma</span><span class="sxs-lookup"><span data-stu-id="23a31-114">Example 2: Remove a network interface</span></span>
```
PS C:\>Get-AzNetworkInterfaceTapConfig -Name "TapConfiguration" -NetworkInterfaceName "NetworkInterface1" -ResourceGroup "ResourceGroup1" | Remove-AzNetworkInterfaceTapConfig -Force
```

<span data-ttu-id="23a31-115">Bu komut, kaynak grubundaki NetworkInterface1 'den TapConfiguration 'ı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="23a31-115">This command removes the TapConfiguration from NetworkInterface1 in a resource group ResourceGroup1.</span></span>
<span data-ttu-id="23a31-116">*Force* parametresi kullanıldığından, kullanıcıdan onay istenmez.</span><span class="sxs-lookup"><span data-stu-id="23a31-116">Because the *Force* parameter is used, the user is not prompted for confirmation.</span></span>

## <span data-ttu-id="23a31-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="23a31-117">PARAMETERS</span></span>

### <span data-ttu-id="23a31-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23a31-118">-DefaultProfile</span></span>
<span data-ttu-id="23a31-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="23a31-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="23a31-120">-Force</span><span class="sxs-lookup"><span data-stu-id="23a31-120">-Force</span></span>
<span data-ttu-id="23a31-121">Onay sorma.</span><span class="sxs-lookup"><span data-stu-id="23a31-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="23a31-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="23a31-122">-InputObject</span></span>
<span data-ttu-id="23a31-123">Networkınterfacetapconfig başvurusu.</span><span class="sxs-lookup"><span data-stu-id="23a31-123">Reference to NetworkInterfaceTapConfig.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceTapConfiguration
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="23a31-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="23a31-124">-Name</span></span>
<span data-ttu-id="23a31-125">Sanal ağ eşleme adı.</span><span class="sxs-lookup"><span data-stu-id="23a31-125">The virtual network peering name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23a31-126">-Networkınterfacename</span><span class="sxs-lookup"><span data-stu-id="23a31-126">-NetworkInterfaceName</span></span>
<span data-ttu-id="23a31-127">Sanal ağ adı.</span><span class="sxs-lookup"><span data-stu-id="23a31-127">The virtual network name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23a31-128">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="23a31-128">-PassThru</span></span>
<span data-ttu-id="23a31-129">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="23a31-129">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="23a31-130">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="23a31-130">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="23a31-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23a31-131">-ResourceGroupName</span></span>
<span data-ttu-id="23a31-132">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="23a31-132">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23a31-133">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="23a31-133">-ResourceId</span></span>
<span data-ttu-id="23a31-134">Networkınterfacetapconfig kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="23a31-134">NetworkInterfaceTapConfig resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23a31-135">-Onay</span><span class="sxs-lookup"><span data-stu-id="23a31-135">-Confirm</span></span>
<span data-ttu-id="23a31-136">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="23a31-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="23a31-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="23a31-137">-WhatIf</span></span>
<span data-ttu-id="23a31-138">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="23a31-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="23a31-139">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="23a31-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="23a31-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23a31-140">CommonParameters</span></span>
<span data-ttu-id="23a31-141">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="23a31-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23a31-142">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="23a31-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23a31-143">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="23a31-143">INPUTS</span></span>

### <span data-ttu-id="23a31-144">System. String</span><span class="sxs-lookup"><span data-stu-id="23a31-144">System.String</span></span>

### <span data-ttu-id="23a31-145">Microsoft. Azure. Commands. Network. model. Psnetworkınterfacetapconfiguration</span><span class="sxs-lookup"><span data-stu-id="23a31-145">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceTapConfiguration</span></span>

## <span data-ttu-id="23a31-146">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="23a31-146">OUTPUTS</span></span>

### <span data-ttu-id="23a31-147">Microsoft. Azure. Commands. Network. modeller. Psnetworkınterface</span><span class="sxs-lookup"><span data-stu-id="23a31-147">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="23a31-148">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="23a31-148">NOTES</span></span>

## <span data-ttu-id="23a31-149">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="23a31-149">RELATED LINKS</span></span>

[<span data-ttu-id="23a31-150">Add-Aznetworkınterfacetapconfig</span><span class="sxs-lookup"><span data-stu-id="23a31-150">Add-AzNetworkInterfaceTapConfig</span></span>](./Add-AzNetworkInterfaceTapConfig.md)

[<span data-ttu-id="23a31-151">Get-Aznetworkınterfacetapconfig</span><span class="sxs-lookup"><span data-stu-id="23a31-151">Get-AzNetworkInterfaceTapConfig</span></span>](./Get-AzNetworkInterfaceTapConfig.md)

[<span data-ttu-id="23a31-152">Set-Aznetworkınterfacetapconfig</span><span class="sxs-lookup"><span data-stu-id="23a31-152">Set-AzNetworkInterfaceTapConfig</span></span>](./Set-AzNetworkInterfaceTapConfig.md)
