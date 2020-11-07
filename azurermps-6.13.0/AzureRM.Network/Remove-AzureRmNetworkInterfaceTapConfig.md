---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/Remove-azurermnetworkinterfacetapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkInterfaceTapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkInterfaceTapConfig.md
ms.openlocfilehash: 9833a2e66eb6471efb9aed021af7ae07e8e520c5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764337"
---
# <span data-ttu-id="8f4a8-101">Remove-AzureRmNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="8f4a8-101">Remove-AzureRmNetworkInterfaceTapConfig</span></span>

## <span data-ttu-id="8f4a8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8f4a8-102">SYNOPSIS</span></span>
<span data-ttu-id="8f4a8-103">Verilen ağ arabiriminden bir dokunma yapılandırmasını kaldırır</span><span class="sxs-lookup"><span data-stu-id="8f4a8-103">Removes a tap configuration from given network interface</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8f4a8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8f4a8-104">SYNTAX</span></span>

### <span data-ttu-id="8f4a8-105">RemoveByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="8f4a8-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzureRmNetworkInterfaceTapConfig -ResourceGroupName <String> -NetworkInterfaceName <String>
 -Name <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8f4a8-106">Deletebyresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="8f4a8-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzureRmNetworkInterfaceTapConfig -ResourceId <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8f4a8-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8f4a8-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzureRmNetworkInterfaceTapConfig -InputObject <PSNetworkInterfaceTapConfiguration> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8f4a8-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="8f4a8-108">DESCRIPTION</span></span>
<span data-ttu-id="8f4a8-109">**Remove-Azurermnetworkınterfacetapconfig** cmdlet 'i, bir ağ arabirim listesinden Azure dokunma yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="8f4a8-109">The **Remove-AzureRmNetworkInterfaceTapConfig** cmdlet removes an Azure tap configuration from a network interface list.</span></span>

## <span data-ttu-id="8f4a8-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8f4a8-110">EXAMPLES</span></span>

### <span data-ttu-id="8f4a8-111">Örnek 1: bir dokunma yapılandırmasını kaldırma</span><span class="sxs-lookup"><span data-stu-id="8f4a8-111">Example 1: Remove a tap configuration</span></span>
```
PS C:\>Remove-AzureRmNetworkInterfaceTapConfig -Name "TapConfiguration" -NetworkInterfaceName "NetworkInterface1" -ResourceGroup "ResourceGroup1"
```

<span data-ttu-id="8f4a8-112">Bu komut, kaynak grubundaki NetworkInterface1 'den TapConfiguration 'ı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="8f4a8-112">This command removes the TapConfiguration from NetworkInterface1 in a resource group ResourceGroup1.</span></span>
<span data-ttu-id="8f4a8-113">*Force* parametresi kullanılmadığından, kullanıcıdan bu eylemi onaylaması istenir.</span><span class="sxs-lookup"><span data-stu-id="8f4a8-113">Because the *Force* parameter is not used, the user will be prompted to confirm this action.</span></span>

### <span data-ttu-id="8f4a8-114">Örnek 2: ağ arabirimini kaldırma</span><span class="sxs-lookup"><span data-stu-id="8f4a8-114">Example 2: Remove a network interface</span></span>
```
PS C:\>Get-AzureRmNetworkInterfaceTapConfig -Name "TapConfiguration" -NetworkInterfaceName "NetworkInterface1" -ResourceGroup "ResourceGroup1" | Remove-AzureRmNetworkInterfaceTapConfig -Force
```

<span data-ttu-id="8f4a8-115">Bu komut, kaynak grubundaki NetworkInterface1 'den TapConfiguration 'ı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="8f4a8-115">This command removes the TapConfiguration from NetworkInterface1 in a resource group ResourceGroup1.</span></span>
<span data-ttu-id="8f4a8-116">*Force* parametresi kullanıldığından, kullanıcıdan onay istenmez.</span><span class="sxs-lookup"><span data-stu-id="8f4a8-116">Because the *Force* parameter is used, the user is not prompted for confirmation.</span></span>

## <span data-ttu-id="8f4a8-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8f4a8-117">PARAMETERS</span></span>

### <span data-ttu-id="8f4a8-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f4a8-118">-DefaultProfile</span></span>
<span data-ttu-id="8f4a8-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8f4a8-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8f4a8-120">-Force</span><span class="sxs-lookup"><span data-stu-id="8f4a8-120">-Force</span></span>
<span data-ttu-id="8f4a8-121">Onay sorma.</span><span class="sxs-lookup"><span data-stu-id="8f4a8-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="8f4a8-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8f4a8-122">-InputObject</span></span>
<span data-ttu-id="8f4a8-123">Networkınterfacetapconfig başvurusu.</span><span class="sxs-lookup"><span data-stu-id="8f4a8-123">Reference to NetworkInterfaceTapConfig.</span></span>

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

### <span data-ttu-id="8f4a8-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="8f4a8-124">-Name</span></span>
<span data-ttu-id="8f4a8-125">Sanal ağ eşleme adı.</span><span class="sxs-lookup"><span data-stu-id="8f4a8-125">The virtual network peering name.</span></span>

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

### <span data-ttu-id="8f4a8-126">-Networkınterfacename</span><span class="sxs-lookup"><span data-stu-id="8f4a8-126">-NetworkInterfaceName</span></span>
<span data-ttu-id="8f4a8-127">Sanal ağ adı.</span><span class="sxs-lookup"><span data-stu-id="8f4a8-127">The virtual network name.</span></span>

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

### <span data-ttu-id="8f4a8-128">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="8f4a8-128">-PassThru</span></span>
<span data-ttu-id="8f4a8-129">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="8f4a8-129">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="8f4a8-130">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="8f4a8-130">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="8f4a8-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f4a8-131">-ResourceGroupName</span></span>
<span data-ttu-id="8f4a8-132">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="8f4a8-132">The resource group name.</span></span>

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

### <span data-ttu-id="8f4a8-133">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="8f4a8-133">-ResourceId</span></span>
<span data-ttu-id="8f4a8-134">Networkınterfacetapconfig kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="8f4a8-134">NetworkInterfaceTapConfig resource id.</span></span>

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

### <span data-ttu-id="8f4a8-135">-Onay</span><span class="sxs-lookup"><span data-stu-id="8f4a8-135">-Confirm</span></span>
<span data-ttu-id="8f4a8-136">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="8f4a8-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8f4a8-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8f4a8-137">-WhatIf</span></span>
<span data-ttu-id="8f4a8-138">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="8f4a8-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8f4a8-139">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="8f4a8-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8f4a8-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f4a8-140">CommonParameters</span></span>
<span data-ttu-id="8f4a8-141">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8f4a8-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f4a8-142">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8f4a8-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f4a8-143">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8f4a8-143">INPUTS</span></span>

### <span data-ttu-id="8f4a8-144">System. String</span><span class="sxs-lookup"><span data-stu-id="8f4a8-144">System.String</span></span>

## <span data-ttu-id="8f4a8-145">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8f4a8-145">OUTPUTS</span></span>

### <span data-ttu-id="8f4a8-146">Microsoft. Azure. Commands. Network. modeller. Psnetworkınterface</span><span class="sxs-lookup"><span data-stu-id="8f4a8-146">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="8f4a8-147">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8f4a8-147">NOTES</span></span>

## <span data-ttu-id="8f4a8-148">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8f4a8-148">RELATED LINKS</span></span>
