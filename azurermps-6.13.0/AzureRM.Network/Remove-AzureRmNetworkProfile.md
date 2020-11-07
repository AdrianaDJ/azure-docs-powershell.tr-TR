---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermnetworkprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkProfile.md
ms.openlocfilehash: ebf2a58530f1dabe0e320dd78a38c63c86565c73
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764336"
---
# <span data-ttu-id="02c2a-101">Remove-AzureRmNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="02c2a-101">Remove-AzureRmNetworkProfile</span></span>

## <span data-ttu-id="02c2a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="02c2a-102">SYNOPSIS</span></span>
<span data-ttu-id="02c2a-103">Ağ profilini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="02c2a-103">Removes a network profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="02c2a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="02c2a-104">SYNTAX</span></span>

### <span data-ttu-id="02c2a-105">RemoveByName</span><span class="sxs-lookup"><span data-stu-id="02c2a-105">RemoveByName</span></span>
```
Remove-AzureRmNetworkProfile -ResourceGroupName <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="02c2a-106">RemoveByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="02c2a-106">RemoveByNameParameterSet</span></span>
```
Remove-AzureRmNetworkProfile -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="02c2a-107">Removebyresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="02c2a-107">RemoveByResourceIdParameterSet</span></span>
```
Remove-AzureRmNetworkProfile -ResourceId <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="02c2a-108">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="02c2a-108">RemoveByInputObjectParameterSet</span></span>
```
Remove-AzureRmNetworkProfile -InputObject <PSNetworkProfile> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="02c2a-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="02c2a-109">DESCRIPTION</span></span>
<span data-ttu-id="02c2a-110">**Remove-AzureRmNetworkProfile** cmdlet 'i, bir ağ profilini (konteyner ağı arabirim **yapılandırmasına** uygun bir şekilde) oluşturduysa bir ağ profilini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="02c2a-110">The **Remove-AzureRmNetworkProfile** cmdlet removes a network profile if no container network interfaces (as contrasted to a container network interface **configuration** ) have been created.</span></span>

## <span data-ttu-id="02c2a-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="02c2a-111">EXAMPLES</span></span>

### <span data-ttu-id="02c2a-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="02c2a-112">Example 1</span></span>
```powershell
Remove-AzureRmNetworkProfile -Name np1 -ResourceGroupName rg1
```

<span data-ttu-id="02c2a-113">Bu, NP1 adındaki ağ profilini kaynak grubundan kaldırır.</span><span class="sxs-lookup"><span data-stu-id="02c2a-113">This removes the network profile with name np1 from the resource group rg1.</span></span>

## <span data-ttu-id="02c2a-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="02c2a-114">PARAMETERS</span></span>

### <span data-ttu-id="02c2a-115">-Iş</span><span class="sxs-lookup"><span data-stu-id="02c2a-115">-AsJob</span></span>
<span data-ttu-id="02c2a-116">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="02c2a-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="02c2a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02c2a-117">-DefaultProfile</span></span>
<span data-ttu-id="02c2a-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="02c2a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="02c2a-119">-Force</span><span class="sxs-lookup"><span data-stu-id="02c2a-119">-Force</span></span>
<span data-ttu-id="02c2a-120">Kaynağı silmek istiyorsanız onay sorma</span><span class="sxs-lookup"><span data-stu-id="02c2a-120">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="02c2a-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="02c2a-121">-InputObject</span></span>
<span data-ttu-id="02c2a-122">Ağ profili nesnesi.</span><span class="sxs-lookup"><span data-stu-id="02c2a-122">Network profile object.</span></span>

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

### <span data-ttu-id="02c2a-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="02c2a-123">-Name</span></span>
<span data-ttu-id="02c2a-124">Ağ profilinin adı.</span><span class="sxs-lookup"><span data-stu-id="02c2a-124">The name of the network profile.</span></span>

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

### <span data-ttu-id="02c2a-125">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="02c2a-125">-PassThru</span></span>
<span data-ttu-id="02c2a-126">{{Dolgu geçiş açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="02c2a-126">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="02c2a-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02c2a-127">-ResourceGroupName</span></span>
<span data-ttu-id="02c2a-128">Ağ profilinin kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="02c2a-128">The resource group name of the network profile.</span></span>

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

### <span data-ttu-id="02c2a-129">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="02c2a-129">-ResourceId</span></span>
<span data-ttu-id="02c2a-130">Ağ profilinin Azure Resource Manager kaynak KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="02c2a-130">The Azure resource manager resource ID of the network profile.</span></span>

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

### <span data-ttu-id="02c2a-131">-Onay</span><span class="sxs-lookup"><span data-stu-id="02c2a-131">-Confirm</span></span>
<span data-ttu-id="02c2a-132">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="02c2a-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="02c2a-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02c2a-133">-WhatIf</span></span>
<span data-ttu-id="02c2a-134">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="02c2a-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="02c2a-135">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="02c2a-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="02c2a-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02c2a-136">CommonParameters</span></span>
<span data-ttu-id="02c2a-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="02c2a-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02c2a-138">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="02c2a-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02c2a-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="02c2a-139">INPUTS</span></span>

### <span data-ttu-id="02c2a-140">System. String</span><span class="sxs-lookup"><span data-stu-id="02c2a-140">System.String</span></span>

## <span data-ttu-id="02c2a-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="02c2a-141">OUTPUTS</span></span>

### <span data-ttu-id="02c2a-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="02c2a-142">System.Boolean</span></span>

## <span data-ttu-id="02c2a-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="02c2a-143">NOTES</span></span>

## <span data-ttu-id="02c2a-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="02c2a-144">RELATED LINKS</span></span>
