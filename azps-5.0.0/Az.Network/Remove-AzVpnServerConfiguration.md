---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvpnserverconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnServerConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnServerConfiguration.md
ms.openlocfilehash: 5d4fa487210b732e0121a01f7cc5fa392ebfb68c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94278095"
---
# <span data-ttu-id="00f7a-101">Remove-AzVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="00f7a-101">Remove-AzVpnServerConfiguration</span></span>

## <span data-ttu-id="00f7a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="00f7a-102">SYNOPSIS</span></span>
<span data-ttu-id="00f7a-103">Var olan bir Vpnserveryapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="00f7a-103">Removes an existing VpnServerConfiguration.</span></span>

## <span data-ttu-id="00f7a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="00f7a-104">SYNTAX</span></span>

### <span data-ttu-id="00f7a-105">ByVpnServerConfigurationName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="00f7a-105">ByVpnServerConfigurationName (Default)</span></span>
```
Remove-AzVpnServerConfiguration -ResourceGroupName <String> -Name <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="00f7a-106">ByVpnServerConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="00f7a-106">ByVpnServerConfigurationObject</span></span>
```
Remove-AzVpnServerConfiguration -InputObject <PSVpnServerConfiguration> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="00f7a-107">Byvpnserverconfigurationresourceıd</span><span class="sxs-lookup"><span data-stu-id="00f7a-107">ByVpnServerConfigurationResourceId</span></span>
```
Remove-AzVpnServerConfiguration -ResourceId <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="00f7a-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="00f7a-108">DESCRIPTION</span></span>
<span data-ttu-id="00f7a-109">{{Açıklamayı doldurun}}</span><span class="sxs-lookup"><span data-stu-id="00f7a-109">{{Fill in the Description}}</span></span>

## <span data-ttu-id="00f7a-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="00f7a-110">EXAMPLES</span></span>

### <span data-ttu-id="00f7a-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="00f7a-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzVpnServerConfiguration -Name "test1config" -ResourceGroupName "P2SCortexGATesting" -Force -PassThru
```

<span data-ttu-id="00f7a-112">Yukarıdaki komut, var olan bir Vpnserveryapılandırmasını kaldıracak.</span><span class="sxs-lookup"><span data-stu-id="00f7a-112">The above command will remove an existing VpnServerConfiguration.</span></span>

## <span data-ttu-id="00f7a-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="00f7a-113">PARAMETERS</span></span>

### <span data-ttu-id="00f7a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00f7a-114">-DefaultProfile</span></span>
<span data-ttu-id="00f7a-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="00f7a-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="00f7a-116">-Force</span><span class="sxs-lookup"><span data-stu-id="00f7a-116">-Force</span></span>
<span data-ttu-id="00f7a-117">Onay sorma.</span><span class="sxs-lookup"><span data-stu-id="00f7a-117">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="00f7a-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="00f7a-118">-InputObject</span></span>
<span data-ttu-id="00f7a-119">Silinecek vpnServerConfiguration nesnesi.</span><span class="sxs-lookup"><span data-stu-id="00f7a-119">The vpnServerConfiguration object to be deleted.</span></span>

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

### <span data-ttu-id="00f7a-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="00f7a-120">-Name</span></span>
<span data-ttu-id="00f7a-121">VpnServerConfiguration adı.</span><span class="sxs-lookup"><span data-stu-id="00f7a-121">The vpnServerConfiguration name.</span></span>

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

### <span data-ttu-id="00f7a-122">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="00f7a-122">-PassThru</span></span>
<span data-ttu-id="00f7a-123">Bu işlemin gerçekleştirildiği öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="00f7a-123">Returns an object representing the item on which this operation is being performed.</span></span>

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

### <span data-ttu-id="00f7a-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="00f7a-124">-ResourceGroupName</span></span>
<span data-ttu-id="00f7a-125">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="00f7a-125">The resource group name.</span></span>

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

### <span data-ttu-id="00f7a-126">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="00f7a-126">-ResourceId</span></span>
<span data-ttu-id="00f7a-127">Silinecek vpnServerConfiguration için Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="00f7a-127">The Azure resource ID for the vpnServerConfiguration to be deleted.</span></span>

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

### <span data-ttu-id="00f7a-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="00f7a-128">-Confirm</span></span>
<span data-ttu-id="00f7a-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="00f7a-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="00f7a-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="00f7a-130">-WhatIf</span></span>
<span data-ttu-id="00f7a-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="00f7a-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="00f7a-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="00f7a-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="00f7a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00f7a-133">CommonParameters</span></span>
<span data-ttu-id="00f7a-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="00f7a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00f7a-135">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="00f7a-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00f7a-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="00f7a-136">INPUTS</span></span>

### <span data-ttu-id="00f7a-137">Microsoft. Azure. Commands. Network. model. PSVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="00f7a-137">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span></span>
<span data-ttu-id="00f7a-138">System. String</span><span class="sxs-lookup"><span data-stu-id="00f7a-138">System.String</span></span>

## <span data-ttu-id="00f7a-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="00f7a-139">OUTPUTS</span></span>

### <span data-ttu-id="00f7a-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="00f7a-140">System.Boolean</span></span>

## <span data-ttu-id="00f7a-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="00f7a-141">NOTES</span></span>

## <span data-ttu-id="00f7a-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="00f7a-142">RELATED LINKS</span></span>
