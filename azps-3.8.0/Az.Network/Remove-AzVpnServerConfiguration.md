---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvpnserverconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnServerConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnServerConfiguration.md
ms.openlocfilehash: 5d4fa487210b732e0121a01f7cc5fa392ebfb68c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94103938"
---
# <span data-ttu-id="be221-101">Remove-AzVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="be221-101">Remove-AzVpnServerConfiguration</span></span>

## <span data-ttu-id="be221-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="be221-102">SYNOPSIS</span></span>
<span data-ttu-id="be221-103">Var olan bir Vpnserveryapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="be221-103">Removes an existing VpnServerConfiguration.</span></span>

## <span data-ttu-id="be221-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="be221-104">SYNTAX</span></span>

### <span data-ttu-id="be221-105">ByVpnServerConfigurationName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="be221-105">ByVpnServerConfigurationName (Default)</span></span>
```
Remove-AzVpnServerConfiguration -ResourceGroupName <String> -Name <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="be221-106">ByVpnServerConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="be221-106">ByVpnServerConfigurationObject</span></span>
```
Remove-AzVpnServerConfiguration -InputObject <PSVpnServerConfiguration> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="be221-107">Byvpnserverconfigurationresourceıd</span><span class="sxs-lookup"><span data-stu-id="be221-107">ByVpnServerConfigurationResourceId</span></span>
```
Remove-AzVpnServerConfiguration -ResourceId <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="be221-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="be221-108">DESCRIPTION</span></span>
<span data-ttu-id="be221-109">{{Açıklamayı doldurun}}</span><span class="sxs-lookup"><span data-stu-id="be221-109">{{Fill in the Description}}</span></span>

## <span data-ttu-id="be221-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="be221-110">EXAMPLES</span></span>

### <span data-ttu-id="be221-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="be221-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzVpnServerConfiguration -Name "test1config" -ResourceGroupName "P2SCortexGATesting" -Force -PassThru
```

<span data-ttu-id="be221-112">Yukarıdaki komut, var olan bir Vpnserveryapılandırmasını kaldıracak.</span><span class="sxs-lookup"><span data-stu-id="be221-112">The above command will remove an existing VpnServerConfiguration.</span></span>

## <span data-ttu-id="be221-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="be221-113">PARAMETERS</span></span>

### <span data-ttu-id="be221-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be221-114">-DefaultProfile</span></span>
<span data-ttu-id="be221-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="be221-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be221-116">-Force</span><span class="sxs-lookup"><span data-stu-id="be221-116">-Force</span></span>
<span data-ttu-id="be221-117">Onay sorma.</span><span class="sxs-lookup"><span data-stu-id="be221-117">Do not ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be221-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="be221-118">-InputObject</span></span>
<span data-ttu-id="be221-119">Silinecek vpnServerConfiguration nesnesi.</span><span class="sxs-lookup"><span data-stu-id="be221-119">The vpnServerConfiguration object to be deleted.</span></span>

```yaml
Type: PSVpnServerConfiguration
Parameter Sets: ByVpnServerConfigurationObject
Aliases: VpnServerConfiguration

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="be221-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="be221-120">-Name</span></span>
<span data-ttu-id="be221-121">VpnServerConfiguration adı.</span><span class="sxs-lookup"><span data-stu-id="be221-121">The vpnServerConfiguration name.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnServerConfigurationName
Aliases: ResourceName, VpnServerConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be221-122">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="be221-122">-PassThru</span></span>
<span data-ttu-id="be221-123">Bu işlemin gerçekleştirildiği öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="be221-123">Returns an object representing the item on which this operation is being performed.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be221-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="be221-124">-ResourceGroupName</span></span>
<span data-ttu-id="be221-125">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="be221-125">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnServerConfigurationName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be221-126">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="be221-126">-ResourceId</span></span>
<span data-ttu-id="be221-127">Silinecek vpnServerConfiguration için Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="be221-127">The Azure resource ID for the vpnServerConfiguration to be deleted.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnServerConfigurationResourceId
Aliases: VpnServerConfigurationId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be221-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="be221-128">-Confirm</span></span>
<span data-ttu-id="be221-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="be221-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="be221-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="be221-130">-WhatIf</span></span>
<span data-ttu-id="be221-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="be221-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="be221-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="be221-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="be221-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be221-133">CommonParameters</span></span>
<span data-ttu-id="be221-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="be221-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be221-135">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="be221-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be221-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="be221-136">INPUTS</span></span>

### <span data-ttu-id="be221-137">Microsoft. Azure. Commands. Network. model. PSVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="be221-137">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span></span>
<span data-ttu-id="be221-138">System. String</span><span class="sxs-lookup"><span data-stu-id="be221-138">System.String</span></span>

## <span data-ttu-id="be221-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="be221-139">OUTPUTS</span></span>

### <span data-ttu-id="be221-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="be221-140">System.Boolean</span></span>

## <span data-ttu-id="be221-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="be221-141">NOTES</span></span>

## <span data-ttu-id="be221-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="be221-142">RELATED LINKS</span></span>
