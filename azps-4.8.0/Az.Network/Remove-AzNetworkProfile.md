---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworkprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkProfile.md
ms.openlocfilehash: 3a83b7200f7634574fd457d2fa08f926a62b9a82
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94265937"
---
# <span data-ttu-id="ef4ca-101">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="ef4ca-101">Remove-AzNetworkProfile</span></span>

## <span data-ttu-id="ef4ca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ef4ca-102">SYNOPSIS</span></span>
<span data-ttu-id="ef4ca-103">Ağ profilini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="ef4ca-103">Removes a network profile.</span></span>

## <span data-ttu-id="ef4ca-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ef4ca-104">SYNTAX</span></span>

### <span data-ttu-id="ef4ca-105">RemoveByNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="ef4ca-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzNetworkProfile -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ef4ca-106">Removebyresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="ef4ca-106">RemoveByResourceIdParameterSet</span></span>
```
Remove-AzNetworkProfile -ResourceId <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ef4ca-107">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ef4ca-107">RemoveByInputObjectParameterSet</span></span>
```
Remove-AzNetworkProfile -InputObject <PSNetworkProfile> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ef4ca-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="ef4ca-108">DESCRIPTION</span></span>
<span data-ttu-id="ef4ca-109">**Remove-AzNetworkProfile** cmdlet 'i, kapsayıcı ağ arabirimleri yoksa (konteyner ağı arabirimi **yapılandırması** için uygun olan) oluşturulmuş bir ağ profilini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="ef4ca-109">The **Remove-AzNetworkProfile** cmdlet removes a network profile if no container network interfaces (as contrasted to a container network interface **configuration** ) have been created.</span></span>

## <span data-ttu-id="ef4ca-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ef4ca-110">EXAMPLES</span></span>

### <span data-ttu-id="ef4ca-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="ef4ca-111">Example 1</span></span>
```powershell
Remove-AzNetworkProfile -Name np1 -ResourceGroupName rg1
```

<span data-ttu-id="ef4ca-112">Bu, NP1 adındaki ağ profilini kaynak grubundan kaldırır.</span><span class="sxs-lookup"><span data-stu-id="ef4ca-112">This removes the network profile with name np1 from the resource group rg1.</span></span>

## <span data-ttu-id="ef4ca-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ef4ca-113">PARAMETERS</span></span>

### <span data-ttu-id="ef4ca-114">-Iş</span><span class="sxs-lookup"><span data-stu-id="ef4ca-114">-AsJob</span></span>
<span data-ttu-id="ef4ca-115">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="ef4ca-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ef4ca-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef4ca-116">-DefaultProfile</span></span>
<span data-ttu-id="ef4ca-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ef4ca-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ef4ca-118">-Force</span><span class="sxs-lookup"><span data-stu-id="ef4ca-118">-Force</span></span>
<span data-ttu-id="ef4ca-119">Kaynağı silmek istiyorsanız onay sorma</span><span class="sxs-lookup"><span data-stu-id="ef4ca-119">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="ef4ca-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ef4ca-120">-InputObject</span></span>
<span data-ttu-id="ef4ca-121">Ağ profili nesnesi.</span><span class="sxs-lookup"><span data-stu-id="ef4ca-121">Network profile object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkProfile
Parameter Sets: RemoveByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ef4ca-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="ef4ca-122">-Name</span></span>
<span data-ttu-id="ef4ca-123">Ağ profilinin adı.</span><span class="sxs-lookup"><span data-stu-id="ef4ca-123">The name of the network profile.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef4ca-124">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="ef4ca-124">-PassThru</span></span>
<span data-ttu-id="ef4ca-125">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="ef4ca-125">Returns an object representing the item with which you are working.</span></span>

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

### <span data-ttu-id="ef4ca-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef4ca-126">-ResourceGroupName</span></span>
<span data-ttu-id="ef4ca-127">Ağ profilinin kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="ef4ca-127">The resource group name of the network profile.</span></span>

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

### <span data-ttu-id="ef4ca-128">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="ef4ca-128">-ResourceId</span></span>
<span data-ttu-id="ef4ca-129">Ağ profilinin Azure Resource Manager kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="ef4ca-129">The Azure resource manager resource ID of the network profile.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef4ca-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="ef4ca-130">-Confirm</span></span>
<span data-ttu-id="ef4ca-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ef4ca-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ef4ca-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ef4ca-132">-WhatIf</span></span>
<span data-ttu-id="ef4ca-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ef4ca-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ef4ca-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ef4ca-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ef4ca-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef4ca-135">CommonParameters</span></span>
<span data-ttu-id="ef4ca-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ef4ca-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef4ca-137">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ef4ca-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef4ca-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ef4ca-138">INPUTS</span></span>

### <span data-ttu-id="ef4ca-139">System. String</span><span class="sxs-lookup"><span data-stu-id="ef4ca-139">System.String</span></span>

### <span data-ttu-id="ef4ca-140">Microsoft. Azure. Commands. Network. modeller. PSNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="ef4ca-140">Microsoft.Azure.Commands.Network.Models.PSNetworkProfile</span></span>

## <span data-ttu-id="ef4ca-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ef4ca-141">OUTPUTS</span></span>

### <span data-ttu-id="ef4ca-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ef4ca-142">System.Boolean</span></span>

## <span data-ttu-id="ef4ca-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ef4ca-143">NOTES</span></span>

## <span data-ttu-id="ef4ca-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ef4ca-144">RELATED LINKS</span></span>

[<span data-ttu-id="ef4ca-145">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="ef4ca-145">Get-AzNetworkProfile</span></span>](./Get-AzNetworkProfile.md)

[<span data-ttu-id="ef4ca-146">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="ef4ca-146">New-AzNetworkProfile</span></span>](./New-AzNetworkProfile.md)

[<span data-ttu-id="ef4ca-147">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="ef4ca-147">Set-AzNetworkProfile</span></span>](./Set-AzNetworkProfile.md)
